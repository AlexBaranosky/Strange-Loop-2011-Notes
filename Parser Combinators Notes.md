why use parser combinators?

hwow to use parser combinators?

write your own

category theory!

Doh
===

formal grammars have a large upfront tax

LL, LR, LALR

project integration

yacc, ANTLR

parser generators aren't in-language => not simple, not out of the box, just more to manage

the anti-DSL

DSL == small, specific (new) language

...

modular, TDD-friendly

user-friendly default error messages => SWEET

natural parsing and processing => parsing looks not too different from calling a normal function

BUT...............

it is incredibly fine-grained

use of closures borders on the pathological.


JParsec for Java ... also for many other languages, origianly haskell I think

First Principles
================

Consumed

Empty

...

Ok

Error

[ cok  eok  ]
[ cerr eerr ]


;; cok
(defn alwways [x]
  (fn [state cok err eok eerr]
    (cok x state)))

;; eerr
(defn never []
  (fn [state cok err eok eerr]
    (eerr (UnknownError. (:pos state)))))

(defn token []
  (fn [{} jeys code missing]
    (if-let [tok (first input)]
      (cok tok (InputState. (rest input) (inc pos)))
      (eerr (UnexpectedError. "End of input" pos)))))

P >> Q
======

moon language for 'next'

what should p >> q return?

what if q depends on the value of p?

(defn next [p q]
  (fn [state cok cerr eok eerr]
    (letfn [(pcok [item state]
             (q state cok cerr cok cerr))
            (peok [item state]
              (q state cok cerr eok eerr))]
     (p state pcok cerr peok eerr))))

p <|> q  ;; call that 'either'

what should p<|> q return ?

error mesage if both fail?

Parsatron
=========
