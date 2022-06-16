---
content_type: page
description: 'This page contains the notes for recitation 7. '
draft: false
parent_uid: 9f4e8596-124d-1608-f9e6-b335a917765a
title: Recitation 7 Notes
uid: 95bc71b6-56b3-a07b-95c4-63f5d2768559
---
## Topics

- What is a game?
- Normal form games
- Equilibria

## Games

Why game theory? Games on networks!

Ex. congestion, international trade, Amazon's new office location, peer effects in school learning, deciding state taxes.         
A game is a representation of strategic interaction. 

### Example: Prisoner's Dilemma

{{< tableopen >}}{{< theadopen >}}{{< tropen >}}{{< thopen >}}
 
{{< thclose >}}{{< thopen >}}
2 Silent 
{{< thclose >}}{{< thopen >}}
 2 Confess
{{< thclose >}}{{< trclose >}}{{< theadclose >}}{{< tbodyopen >}}{{< tropen >}}{{< thopen >}}
1 Silent
{{< thclose >}}{{< tdopen >}}
\-2, -2
{{< tdclose >}}{{< tdopen >}}
\-20, 0
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< thopen >}}
1 Confess
{{< thclose >}}{{< tdopen >}}
0, -20
{{< tdclose >}}{{< tdopen >}}
\-10, -10
{{< tdclose >}}{{< trclose >}}{{< tbodyclose >}}{{< tableclose >}}

### Example: Cournot Competition

How many iPhones should Apple produce?

- Apple produces *q*{{< sub "1" >}} iPhones at marginal cost $500.
- Samsung produces *q*{{< sub "2" >}} Galaxies at marginal cost $500.
- Price given by inverse demand *P* = 2000 — *Q*, *Q* = *q*{{< sub "1" >}} + *q*{{< sub "2." >}}
- Apple's profit given by *Pq*{{< sub "1" >}} *—* $500 \* *q*{{< sub "1." >}}
- Samsung's profit given by *Pq*{{< sub "2" >}} — $500 \* *q*{{< sub "2." >}}

## Normal Form Games

Formally, a game consists of 3 elements:

1. The set of players *N.*
2. The sets of strategies {*Si*}i∈*N.*
3. The sets of payoffs {*ui*: *S* → ℝ }i∈*N.*

### Example: Prisoner's Dilemma

- *N* = {1, 2} 
- *S*{{< sub "1" >}} = {silent, confess}, *S*{{< sub "2" >}} = {silent, confess}
- *u*{{< sub "1" >}} : *S*{{< sub "1" >}} \* *S*{{< sub "2" >}} → ℝ and *u*{{< sub "2" >}} : *S*{{< sub "1" >}} \* *S*{{< sub "2" >}}  → ℝ are given by the table, where *u*{{< sub "1" >}} is red and *u*{{< sub "2" >}} is blue.

{{< tableopen >}}{{< theadopen >}}{{< tropen >}}{{< thopen >}}
 
{{< thclose >}}{{< thopen >}}
2 Silent 
{{< thclose >}}{{< thopen >}}
 2 Confess
{{< thclose >}}{{< trclose >}}{{< theadclose >}}{{< tbodyopen >}}{{< tropen >}}{{< thopen >}}
1 Silent
{{< thclose >}}{{< tdopen >}}
\-2, -2
{{< tdclose >}}{{< tdopen >}}
\-20, 0
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< thopen >}}
1 Confess
{{< thclose >}}{{< tdopen >}}
0, -20
{{< tdclose >}}{{< tdopen >}}
\-10, -10
{{< tdclose >}}{{< trclose >}}{{< tbodyclose >}}{{< tableclose >}}

### Example: Cournot Competition

- *N* = {1, 2}
- *S*{{< sub "1" >}} = \[0, ∞), *S*{{< sub "2" >}} {{< sub "=" >}} \[0, ∞)
    - We ignore that *q* must be integers.
- *u*{{< sub "1" >}} : *S* → ℝ and *u*{{< sub "2" >}}: *S* → ℝ given by         
    *u*{{< sub "i" >}} (*q*{{< sub "1" >}}, *q*{{< sub "2" >}}) = (*P —* $500)*q*{{< sub "1" >}} = ($2000 — *q*{{< sub "_1_" >}} — *q*{{< sub "2" >}} — $500)*q*{{< sub "i" >}}

In many cases, the sets of strategies have some structure:

1. Simultaneous games (penalty kicks in soccer).
2. Repeated games (Libor rate manipulation scandal).
3. Sequential games (how should US respond to china's tariffs?).

What happens when there is a game-like situation?          
There are many variations…

- Weak prediction: "Dominated strategies are never played."
- Strong prediction: "Mutually optimal strategies are played."

Elimination of strictly dominated strategies

### Example: Prisoner's Dilemma

 

{{< resource uuid="07721ce8-3fd5-061e-7ea6-90c057a512fd" >}}

 

### Example: Battle of the Sexes

{{< resource uuid="4e7c8ce1-167c-f78b-7bc9-f5fa2f5ef603" >}}

No elimination needed.

## Equilibria

Nash equilibrium - A state with no incentive to deviate that can be sustained.

Given the opponents' strategies, what would you do?         
"Best response correspondence" B{{< sub "i" >}} : *S*{{< sub "\-i" >}} → *S*{{< sub "i" >}}

- B{{< sub "girl" >}}(musical) = {musical}
- B{{< sub "girl" >}}(soccer) = {soccer}
- B{{< sub "boy" >}}(musical) = {musical}
- B{{< sub "boy" >}}(soccer) = {soccer}

⇒ (M,M) and (S,S) are mutually optimal; "nash equilibria."

When the best response correspondence only has one element, we may instead use the best response function (B{{< sub "girl" >}}(musical) = musical).

### Example: Cournot Competition

Given Samsung's production *q*{{< sub "2" >}}, Apple wants to maximize its profits

 

*u*{{< sub "1" >}}(*q*{{< sub "1" >}}, *q*{{< sub "2" >}})=(1500 — *q*{{< sub "_1_" >}} — *q*{{< sub "2" >}})*q*{{< sub "1." >}}{{< sub "  \n<section data-uuid="14ba4c14-e898-b3fb-eec1-ed322084c597"></section>  \n" >}}

That is, B{{< sub "1" >}}(*q*{{< sub "2" >}}) = ½(1500 — *q*{{< sub "2" >}}). Similarly, B{{< sub "2" >}}(*q*{{< sub "1" >}})= ½(1500 — *q*{{< sub "2" >}}).

Nash equilibrium is the fixed point:

{{< resource uuid="241c946b-6516-3f21-731f-69964da1b242" >}}