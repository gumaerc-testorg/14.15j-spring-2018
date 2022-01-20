---
content_type: page
parent_title: Lecture and Recitation Notes
parent_uid: 9f4e8596-124d-1608-f9e6-b335a917765a
title: Recitation 11 Notes
uid: b9f67b7e-3369-39ee-b99e-51aeba3035bb
---

Topics
------

*   Strategic substitutes
*   Strategic complements (local network effects, continued)
*   Subgame perfect equillibrium
*   Rubinstein's bargaining game

Strategic Substitutes
---------------------

If other players act _more_ aggressively, you have incentive to act _less_ aggressively, and vice versa.

Strategic Complements
---------------------

If other players act _more_ aggressively, you have incentive to act _more_ aggressively, and vice versa.

### _Example_: Playing Sports with Friends

![Diagram of relationship chart.]({{< resource_file 99a3b994-f74d-67d1-5aac-27008aeb3742 >}})

*   _N_ = {1, 2, 3}
*   _Si_ = ℝ+ = \[0, ∞)
*   _u__i_(_x__i_, _x__\-i_, δ, _G_) = _x__i_ — ½ _xi__2_ + δ∑(j≠i) _gij xi x__j_
    *   Where δ is the degree of complementarity (δ ≥ 0). 
*   Best response of player _i_:   
    ![Best response equation formula.]({{< resource_file badee777-e475-cbcf-2d0c-fd00b47a34fa >}})
*   Collectively, _BRi_(_x__\-i_) = 𝟙 + δ_G_𝕏.
*   The equilibrium (fixed point) is 𝕏\* = (_I_ — δ_G_)\-1𝟙.

Subgame Perfect Equilibrium
---------------------------

Nash equlibrium only requires mutual optimality:

*   Issue 1: In dynamic games, cannot change the strategy you have taken in the past.
    *   Subgame perfect equilibrium (SPE).
*   Issue 2: Some players may know what other players don't.
    *   (Perfect) Bayesian Nash equilibrium.

### _Example_: Battle of the Sexes

{{< tableopen >}}
{{< theadopen >}}
{{< tropen >}}
{{< thopen >}}
 
{{< thclose >}}
{{< thopen >}}
Shopping
{{< thclose >}}
{{< thopen >}}
 Football
{{< thclose >}}

{{< trclose >}}

{{< theadclose >}}
{{< tropen >}}
{{< thopen >}}
Shopping
{{< thclose >}}
{{< tdopen >}}
(3, 2)
{{< tdclose >}}
{{< tdopen >}}
(0, 0)
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< thopen >}}
Football
{{< thclose >}}
{{< tdopen >}}
(0, 0)
{{< tdclose >}}
{{< tdopen >}}
(2, 3)
{{< tdclose >}}

{{< trclose >}}

{{< tableclose >}}

*   Where (3, 2) and (2, 3) are the two Nash equalibirums.

Suppose the girl wakes up very early. Then, she can wait at Starbucks in the mall.

![Shopping vs football tree diagram.]({{< resource_file 252aa29c-40d5-4da6-d459-561f65ddbf80 >}})

Then, (3, 2) is the unique SPE. The guy claiming that he'll definitely go to football no matter what is an "empty threat."

Rubinstein's Bargaining Game
----------------------------

*   Seller (player 1) does not value the good: _v__1_ = 0.
*   Buyer (player 2) values the good: _v__2_ = 1.

_Question_: How is the price determined?  
_Answer_: Many models, e.g. take-it-or-leave-it-offer. Rubenstein's is important because it can generate price ≈ ½ without altruism.

Suppose they make alternating offers of prices until either accepts an offer. What is the SPE?

When traded at price _p_:

*   Player 1 receives payoff _p_.
*   Player 2 receives payoff _q_ := 1 — _p_.

Trick: Let ͟_p_ and _p̅_ be the minimum and maximum payoffs 1 can receive in his turn. Similarly, define ͟_q_ and _q̅_.

*   In 1's turn, since any offer above δ _q̅_ is accepted, _p_ ≥ 1 — δ_q̅_.
*   Since any offer below δ͟q is rejected, p̅ ≤ 1 — δ͟q.
*   Similarly, in 2's turn, we get ͟q ≥ 1 — δ p̅ and q̅ ≤ 1 — δ͟p.
*   Combining, we get:
    *   ͟_p_ ≥ 1 — δ_q̅_ ≥ 1 — δ(1 — δ͟_p_) ⇒ ͟_p_ ≥ (1 — δ)/(1 — δ2) = 1/(1 + δ).
    *   _p̅_ ≤ 1 — δ͟_q_ ≤ 1 — δ(1 — δ_p̅_) ⇒ _p̅_ ≤ (1 — δ)/(1 — δ2) = 1/(1 + δ).
*   Thus, ͟_p_ = _p̅_ = 1/(1 + δ) and ͟_q_ = _q̅_ = 1/(1 + δ).

Bottom line: If there is any SPE, 1's payoff at _t_\=odd should be 1/(1 + δ) and 2's payoff at _t_\=even be 1/(1 + δ).

Indeed, this equilibrium payoff profile is attainable if and only if they take the following strategies:

*   Player 1: At _t_\=odd, offer _p_ = 1(1 + δ)  
    and at _t_\=even, accept any offer above _p_ = δ/(1 + δ).
*   Player 2: At _t_\=odd, accept any offer above _q_ = δ/(1 + δ)   
    and at _t_\=even, offer _q_ = 1/(1 + δ).

On the equilibrium path, 1 offers _p_ = 1/(1 + δ) and 2 immediately accepts it; end of game.