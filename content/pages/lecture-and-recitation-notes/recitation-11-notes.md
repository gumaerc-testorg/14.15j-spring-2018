---
content_type: page
description: 'Notes for recitation 11. '
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: Lecture and Recitation Notes
parent_type: CourseSection
parent_uid: 9f4e8596-124d-1608-f9e6-b335a917765a
title: Recitation 11 Notes
uid: b9f67b7e-3369-39ee-b99e-51aeba3035bb
---
## Topics

- Strategic substitutes
- Strategic complements (local network effects, continued)
- Subgame perfect equillibrium
- Rubinstein's bargaining game

## Strategic Substitutes

If other players act *more* aggressively, you have incentive to act *less* aggressively, and vice versa.

## Strategic Complements

If other players act *more* aggressively, you have incentive to act *more* aggressively, and vice versa.

### *Example*: Playing Sports with Friends

{{< resource uuid="99a3b994-f74d-67d1-5aac-27008aeb3742" >}}

- *N* = {1, 2, 3}
- *S*{{< sub "i" >}} = ℝ{{< sub "\+" >}} = \[0, ∞)
- *u<sub>i</sub>*(*x<sub>i</sub>*, *x<sub>\-i</sub>*, δ, *G*) = *x<sub>i</sub>* — ½ *x<sub>i</sub><sup>2</sup>* + δ∑<sub>(j≠i)</sub> *g<sub>ij</sub> x<sub>i</sub> x<sub>j</sub>*
    - Where δ is the degree of complementarity (δ ≥ 0). 
- Best response of player *i*: 

{{< resource uuid="badee777-e475-cbcf-2d0c-fd00b47a34fa" >}}

- Collectively, *BR<sub>i</sub>*(*x<sub>\-i</sub>*) = 𝟙 + δ*G*𝕏.
- The equilibrium (fixed point) is 𝕏<sup>\*</sup> = (*I* — δ*G*)<sup>\-1</sup>𝟙.

## Subgame Perfect Equilibrium

Nash equlibrium only requires mutual optimality:

- Issue 1: In dynamic games, cannot change the strategy you have taken in the past.
    - Subgame perfect equilibrium (SPE).
- Issue 2: Some players may know what other players don't.
    - (Perfect) Bayesian Nash equilibrium.

### *Example*: Battle of the Sexes

{{< tableopen >}}{{< theadopen >}}{{< tropen >}}{{< thopen >}}
 
{{< thclose >}}{{< thopen >}}
Shopping
{{< thclose >}}{{< thopen >}}
 Football
{{< thclose >}}{{< trclose >}}{{< theadclose >}}{{< tbodyopen >}}{{< tropen >}}{{< thopen >}}
Shopping
{{< thclose >}}{{< tdopen >}}
(3, 2)
{{< tdclose >}}{{< tdopen >}}
(0, 0)
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< thopen >}}
Football
{{< thclose >}}{{< tdopen >}}
(0, 0)
{{< tdclose >}}{{< tdopen >}}
(2, 3)
{{< tdclose >}}{{< trclose >}}{{< tbodyclose >}}{{< tableclose >}}

- Where (3, 2) and (2, 3) are the two Nash equalibirums.

Suppose the girl wakes up very early. Then, she can wait at Starbucks in the mall.

{{< resource uuid="252aa29c-40d5-4da6-d459-561f65ddbf80" >}}

Then, (3, 2) is the unique SPE. The guy claiming that he'll definitely go to football no matter what is an "empty threat."

## Rubinstein's Bargaining Game

- Seller (player 1) does not value the good: *v<sub>1</sub>* = 0.
- Buyer (player 2) values the good: *v<sub>2</sub>* = 1.

*Question*: How is the price determined?   
*Answer*: Many models, e.g. take-it-or-leave-it-offer. Rubenstein's is important because it can generate price ≈ ½ without altruism.

Suppose they make alternating offers of prices until either accepts an offer. What is the SPE?

When traded at price *p*:

- Player 1 receives payoff *p*.
- Player 2 receives payoff *q* := 1 — *p*.

Trick: Let ͟*p* and *p̅* be the minimum and maximum payoffs 1 can receive in his turn. Similarly, define ͟*q* and *q̅*.

- In 1's turn, since any offer above δ *q̅* is accepted, *p* ≥ 1 — δ*q̅*.
- Since any offer below δ͟q is rejected, p̅ ≤ 1 — δ͟q.
- Similarly, in 2's turn, we get ͟q ≥ 1 — δ p̅ and q̅ ≤ 1 — δ͟p.
- Combining, we get:
    - *p* ≥ 1 — δ*q̅* ≥ 1 — δ(1 — δ͟*p*) ⇒ ͟*p* ≥ (1 — δ)/(1 — δ<sup>2</sup>) = 1/(1 + δ).
    - *p̅* ≤ 1 — δ͟*q* ≤ 1 — δ(1 — δ*p̅*) ⇒ *p̅* ≤ (1 — δ)/(1 — δ<sup>2</sup>) = 1/(1 + δ).
- Thus, *p* = *p̅* = 1/(1 + δ) and ͟*q* = *q̅* = 1/(1 + δ).

Bottom line: If there is any SPE, 1's payoff at *t*\=odd should be 1/(1 + δ) and 2's payoff at *t*\=even be 1/(1 + δ).

Indeed, this equilibrium payoff profile is attainable if and only if they take the following strategies:

- Player 1: At *t*\=odd, offer *p* = 1(1 + δ)   
    and at *t*\=even, accept any offer above *p* = δ/(1 + δ).
- Player 2: At *t*\=odd, accept any offer above *q* = δ/(1 + δ)    
    and at *t*\=even, offer *q* = 1/(1 + δ).

On the equilibrium path, 1 offers *p* = 1/(1 + δ) and 2 immediately accepts it; end of game.