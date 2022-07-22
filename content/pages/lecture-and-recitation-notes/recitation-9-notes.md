---
content_type: page
description: 'This contains the notes for recitation 9. '
learning_resource_types: []
ocw_type: CourseSection
parent_title: Lecture and Recitation Notes
parent_type: CourseSection
parent_uid: 9f4e8596-124d-1608-f9e6-b335a917765a
title: Recitation 9 Notes
uid: cc345d8d-6c56-e8b8-d5cb-038086ccf41b
---

Topics
------

*   Games with homogeneous externalities
*   Games with local network effects

Recall
------

Congestion games had simple sets of payoffs but complicated network structure. There are games that have complicated payoffs with simple network structure. 

Homogeneous Externalities
-------------------------

In classical economics, the demand curve is assumed decreasing and the supply curve increasing. The existence of network effects may create a weird shape of the demand curve. 

*   _N_ = \[0, 1\] continuum of players
*   _S_{{< sub "_i_" >}} \= {buy, not buy}
*   _u_{{< sub "_i_" >}}(_S_{{< sub "_i_" >}}, _S_{{< sub "_\-i_" >}}) = _u_{{< sub "_i_" >}}(_S_{{< sub "_i_" >}}, _x_) =  
    _v{{< sub "i" >}}x_ — _p_  if _S_{{< sub "_i_" >}} = buy  
    0           if _S_{{< sub "_i_" >}}\= not buy
*   _v_{{< sub "_i_" >}} ~ F(\[0, 1\])
*   _p_ > 0
*   Where _x_ is how many buy, _v_{{< sub "_i_" >}} is its value, and _p_ is price.

### _Example: Office suites, SNS, etc._ 

{{< resource 735c3dc4-69f4-26c4-a7c4-55839ab79bf3 >}}

*   _x_ = 1 — F(_v̅_) where _v̅_ is the lowest value of agents who buy.

Claim: If agent with _v_{{< sub "_i_" >}} = _v̅_ is better off buying, then any agent with _v_{{< sub "_j_" >}} > _v̅_ is also better off buying. 

Corollary: We may assume without loss of generality that _x_ (those who buy) have the highest values in equilibrium/socially optimal outcome. 

1.  Socially optimal outcome
    1.  Social welfare = _{{< sub "v̅" >}}_∫{{< sup "1" >}}\[_v_(1 — F(_v̅_)) — _p_\] dF(_v_)
    2.  Maximizing this with respect to _v̅_ yields the social best.
2.  Nash equilibrum
    1.  Pooling equilibrum:  
        If no one has the good (_x_ = 0) then no one has incentive to buy ( _v_{{< sub "_i_" >}} \* 0 — _p_ \< 0). Therefore, _x_{{< sup "_\*_" >}} = 0 is an equilibrium. 
    2.  Separating equilibrium:  
        If someone buys (_x_ > 0), then there exists the lowest type _v̅_ who buys. His incentive must balance _v̅x_ — _p_ = 0.

Note that everyone's strategy is summarized by _x_. So consider the aggregate best response function BR(_x_) = _x̂_. With _v̅x_ — _p_ = 0 and _x_ = 1 — F(_v̅_), we find:

*   BR(_x_) = 1 — F(_p_/_x_).
*   Its fixed point _x_{{< sup "_\*_" >}} is an equilibrium. 

Local Network Effects
---------------------

Some games have both complicated payoff structure and complicated network structure.

 {{< resource 09c2914f-edc0-70a5-d7f4-6caf72833219 >}}

*   _N_ = {1, 2, 3}.
*   _S_{{< sub "_i_" >}} = ℝ{{< sub "\+" >}} \= \[0, ∞).
*   _u_{{< sub "_i_" >}}(_x_{{< sub "_i_" >}}, _x_{{< sub "_\-i_" >}}, δ, _G_) =   
    {{< resource 8d7d1135-8ca6-47c1-6c66-0860dac6514f >}}

_i_'s best response satisfies

{{< resource 1c9f3f1d-a0a7-fc04-87d4-44b1d6f7d4e2 >}}

*   {{< resource 2719373e-98a6-f592-3bdf-233060d0a0fb >}}
*   BR(_x_) = max { 𝟘, 𝟙 — δ_G_𝕏}