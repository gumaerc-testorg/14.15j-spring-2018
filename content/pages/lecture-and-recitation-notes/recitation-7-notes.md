---
content_type: page
parent_title: Lecture and Recitation Notes
parent_uid: 9f4e8596-124d-1608-f9e6-b335a917765a
title: Recitation 7 Notes
uid: 95bc71b6-56b3-a07b-95c4-63f5d2768559
---

Topics
------

*   What is a game?
*   Normal form games
*   Equilibria

Games
-----

Why game theory? Games on networks!

Ex. congestion, international trade, Amazon's new office location, peer effects in school learning, deciding state taxes.  
A game is a representation of strategic interaction. 

### Example: Prisoner's Dilemma

{{< tableopen >}}
{{< theadopen >}}
{{< tropen >}}
{{< thopen >}}
 
{{< thclose >}}
{{< thopen >}}
2 Silent 
{{< thclose >}}
{{< thopen >}}
 2 Confess
{{< thclose >}}

{{< trclose >}}

{{< theadclose >}}
{{< tropen >}}
{{< thopen >}}
1 Silent
{{< thclose >}}
{{< tdopen >}}
\-2, -2
{{< tdclose >}}
{{< tdopen >}}
\-20, 0
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< thopen >}}
1 Confess
{{< thclose >}}
{{< tdopen >}}
0, -20
{{< tdclose >}}
{{< tdopen >}}
\-10, -10
{{< tdclose >}}

{{< trclose >}}

{{< tableclose >}}

### Example: Cournot Competition

How many iPhones should Apple produce?

*   Apple produces _q1_ iPhones at marginal cost $500.
*   Samsung produces _q2_ Galaxies at marginal cost $500.
*   Price given by inverse demand _P_ \= 2000 — _Q_, _Q_ \= _q1_ + _q2._
*   Apple's profit given by _Pq1 —_ $500 \* _q1._
*   Samsung's profit given by _Pq2_ — $500 \* _q2._

Normal Form Games
-----------------

Formally, a game consists of 3 elements:

1.  The set of players _N._
2.  The sets of strategies {_Si_}i∈_N._
3.  The sets of payoffs {_ui_: _S_ → ℝ }i∈_N._

### Example: Prisoner's Dilemma

*   _N_ = {1, 2}
*   _S1_ = {silent, confess}, _S2_ = {silent, confess}
*   _u1_ : _S1_ \* _S2_ → ℝ and _u2_ : _S1_ \* _S2_  → ℝ are given by the table, where _u1_ is red and _u2_ is blue.

{{< tableopen >}}
{{< theadopen >}}
{{< tropen >}}
{{< thopen >}}
 
{{< thclose >}}
{{< thopen >}}
2 Silent 
{{< thclose >}}
{{< thopen >}}
 2 Confess
{{< thclose >}}

{{< trclose >}}

{{< theadclose >}}
{{< tropen >}}
{{< thopen >}}
1 Silent
{{< thclose >}}
{{< tdopen >}}
\-2, \-2
{{< tdclose >}}
{{< tdopen >}}
\-20, 0
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< thopen >}}
1 Confess
{{< thclose >}}
{{< tdopen >}}
0, \-20
{{< tdclose >}}
{{< tdopen >}}
\-10, \-10
{{< tdclose >}}

{{< trclose >}}

{{< tableclose >}}

### Example: Cournot Competition

*   _N_ = {1, 2}
*   _S1_ = \[0, ∞), _S2_ = \[0, ∞)
    *   We ignore that _q_ must be integers.
*   _u1_ : _S_ → ℝ and _u2_: _S_ → ℝ given by  
    _ui_ (_q1_, _q2_) = (_P —_ $500)_q1_ = ($2000 — _q__1_ — _q2_ — $500)_qi_

In many cases, the sets of strategies have some structure:

1.  Simultaneous games (penalty kicks in soccer).
2.  Repeated games (Libor rate manipulation scandal).
3.  Sequential games (how should US respond to china's tariffs?).

What happens when there is a game-like situation?   
There are many variations...

*   Weak prediction: "Dominated strategies are never played."
*   Strong prediction: "Mutually optimal strategies are played."

Elimination of strictly dominated strategies

### Example: Prisoner's Dilemma

 ![2 by 2 table with three options crossed out.]({{< resource_file 07721ce8-3fd5-061e-7ea6-90c057a512fd >}})

### Example: Battle of the Sexes

![2 by 2 table with two options circled.]({{< resource_file 4e7c8ce1-167c-f78b-7bc9-f5fa2f5ef603 >}})  
No elimination needed.

Equilibria
----------

Nash equilibrium - A state with no incentive to deviate that can be sustained.

Given the opponents' strategies, what would you do?  
"Best response correspondence" Bi : _S\-i_ → _Si_

*   Bgirl(musical) = {musical}
*   Bgirl(soccer) = {soccer}
*   Bboy(musical) = {musical}
*   Bboy(soccer) = {soccer}

⇒ (M,M) and (S,S) are mutually optimal; "nash equilibria."

When the best response correspondence only has one element, we may instead use the best response function (Bgirl(musical) = musical).

### Example: Cournot Competition

Given Samsung's production _q2_, Apple wants to maximize its profits _u1_(_q1_, _q2_)=(1500 — _q__1_ — _q2_)_q1._  
![Mathematical equation.]({{< resource_file 14ba4c14-e898-b3fb-eec1-ed322084c597 >}})  

That is, B1(_q2_) = ½(1500 — _q2_). Similarly, B2(_q1_)= ½(1500 — _q2_).

Nash equilibrium is the fixed point:

![Mathematical equation.]({{< resource_file 241c946b-6516-3f21-731f-69964da1b242 >}})