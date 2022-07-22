---
content_type: page
description: 'This contains the notes for recitation 8. '
learning_resource_types: []
ocw_type: CourseSection
parent_title: Lecture and Recitation Notes
parent_type: CourseSection
parent_uid: 9f4e8596-124d-1608-f9e6-b335a917765a
title: Recitation 8 Notes
uid: a27d11ad-71e0-3bed-8734-14bb67acd0f7
---

Topics
------

*   Review
*   Congestion Games
*   Potential Games

Recap from Last Week
--------------------

A game consists of 3 elements:

1.  Set of players _N_
2.  Sets of strategies {_S_{{< sub "_i_" >}}}{{< sub "i∈N" >}}
3.  Sets of payoffs {_u_{{< sub "_i_" >}}}{{< sub "i∈N" >}}

Given a game, what do we do?

1.  Maximize the sum of everyone's payoff.
    *   Socially optimal outcome (what we want to happen).
2.  Maximize individual's payoff conditional on everyone else's strategy and find a fixed point.
    *   Nash equilibrium (what we think will happen).

1 & 2 are often different because there are strategic interactions and individual incentives are unaligned. 

Some games have useful structures, which impose useful restrictions on {_S_{{< sub "_i_" >}}} and {_u_{{< sub "_i_" >}}}.

*   Dynamic games
*   Games on networks

Congestion Games
----------------

Paths are labeled (edge, traffic, cost/duration):

{{< resource 8b8ce358-1ee5-1d9f-a952-ff7b9d51a045 >}}

*   Directed network (_J_, _E_) = ({_A_, _B_, _C_}, {1, 2, 3, 4}).
*   Set of paths _P_ = {_p_{{< sub "_1_" >}}, _p_{{< sub "_2_" >}}, _p_{{< sub "_3_" >}}} = {(1), (2,3), (2,4)}.
*   Traffic on paths {_x_{{< sub "_p1_" >}}, _x_{{< sub "_p2_" >}}, _x_{{< sub "_p3_" >}}} = {_x_{{< sub "_1_" >}}, _x_{{< sub "_3_" >}}, _x_{{< sub "_4_" >}}}.
*   Total (social) cost: _x_{{< sub "_1_" >}}\*L{{< sub "1" >}}(_x_{{< sub "_1_" >}}) + _x_{{< sub "_2_" >}}\*L{{< sub "2" >}}(_x_{{< sub "_2_" >}}) + _x_{{< sub "_3_" >}}\*L{{< sub "3" >}}(_x_{{< sub "_3_" >}}) + _x_{{< sub "_4_" >}}\*L{{< sub "4" >}}(_x_{{< sub "_4_" >}}).
    *   Minimizing this with respect to _x_{{< sub "_1_" >}}, ... _x_{{< sub "_4_" >}} gives socially optimal traffic.

As a game, this can be written:

*   _N_ = \[0, 1\]
*   _S_{{< sub "_i_" >}} = {_p_{{< sub "_1_" >}}, _p_{{< sub "_2_" >}}, _p_{{< sub "_3_" >}}}
*   _u_{{< sub "_i_" >}}(_P_{{< sub "_i_" >}}, everyone else's strategy) = _u_{{< sub "_i_" >}}(_P_{{< sub "_i_" >}}, _x_{{< sub "_1_" >}}..._x_{{< sub "_4_" >}})

However, each individual driver incurs:

*   L{{< sub "1" >}}(_x_{{< sub "_1_" >}}) if he takes _p_{{< sub "_1._" >}}
*   L{{< sub "2" >}}(_x_{{< sub "_2_" >}}) + L{{< sub "3" >}}(_x_{{< sub "_3_" >}}) if he takes _p{{< sub "2." >}}_
*   L{{< sub "2" >}}(_x_{{< sub "_2_" >}}) + L{{< sub "4" >}}(_x_{{< sub "_4_" >}}) if he takes _p_{{< sub "_3._" >}}

So, his best response correspondence is to choose a path that gives minimum individual cost.

*   In equilibrium, we must have L{{< sub "1" >}}(_x_{{< sub "_1_" >}}) = L{{< sub "2" >}}(_x_{{< sub "_2_" >}}) + L{{< sub "3" >}}(_x_{{< sub "_3_" >}}) = L{{< sub "2" >}}(_x_{{< sub "_2_" >}}) + L{{< sub "4" >}}(_x_{{< sub "_4_" >}}).

### _Example:_

Paths are labeled (edge/path, traffic, individual cost):

{{< resource 9a415541-da92-a035-9c9f-e3fb90f215fb >}}

*   Model constraint: _x_{{< sub "_1_" >}} + _x_{{< sub "_2_" >}} = 1.
*   Total cost: _x_{{< sub "_1_" >}}\*L{{< sub "1" >}}(_x_{{< sub "_1_" >}}) + _x_{{< sub "_2_" >}}\*L{{< sub "2" >}}(_x_{{< sub "_2_" >}}) = _x_{{< sub "_1_" >}}{{< sup "2" >}} + _x_{{< sub "_2_" >}} = _x_{{< sub "_1_" >}}{{< sup "2" >}} + (1 — _x_{{< sub "_1_" >}}) = (_x{{< sub "1" >}}_ — ½){{< sup "2" >}} \+ ¾.
*   Socially optimal traffic: (_x_{{< sub "_1_" >}}{{< sup "_S_" >}}, _x__{{< sub "2" >}}_{{< sup "_S_" >}}) = (½ , ½).

Each individual choose path with lower cost, so in equilibrium:

*   L{{< sub "1" >}}(_x{{< sub "1" >}}_{{< sup "_E_" >}}) = L{{< sub "2" >}}(_x_{{< sub "_2_" >}}{{< sup "_E_" >}}), so (_x{{< sub "1" >}}_{{< sup "_E_" >}}, _x{{< sub "2" >}}_{{< sup "_E_" >}}) = (1, 0).
*   Equilibrium total cost is _x{{< sub "1" >}}_{{< sup "_E_" >}}\*L{{< sub "1" >}}(_x{{< sub "1" >}}_{{< sup "_E_" >}}) + _x{{< sub "2" >}}_{{< sup "_E_" >}}\*L{{< sub "2" >}}(_x{{< sub "2" >}}_{{< sup "_E_" >}}) = 1 ≥ ¾.

How to solve this? 

1.  Impose toll _C_ on _p_{{< sub "_1_" >}}.
2.  Then, _u_{{< sub "_i_" >}}(_p_{{< sub "_1_" >}}, _x_{{< sub "_1_" >}}, _x_{{< sub "_2_" >}}) = _x_{{< sub "_1_" >}} + _C_.
3.  We want L{{< sub "1" >}}(_x{{< sub "1" >}}_{{< sup "{{< sub \"_S_\" >}}" >}}) + _C_ = L{{< sub "2" >}}(_x{{< sub "2" >}}_{{< sup "_S_" >}}).
4.  _C_ = ½.

Potential Games
---------------

In physics, particles move along the unique potential field.

{{< resource 770315e0-e12b-e93d-df13-24991317bfce >}}

In society, people move along their own incentives.

{{< resource c4284b00-43ea-befd-7d88-fd6dc2a0704f >}}

However, there are cases where people's incentives are so similar that they move as if there is a unique potential field.

### _Example: Traffic Congestion_

Definition: A game is an exact potential game if there is exists Φ (unique potential field) such that:

*   _u_{{< sub "_i_" >}}(_S_{{< sub "_i_" >}}, _S_{{< sub "_\-i_" >}}) — _u_{{< sub "_i_" >}}(_S_{{< sub "_i_" >}}', _S_{{< sub "_\-i_" >}}) = Φ(_S_{{< sub "_i_" >}}, _S_{{< sub "_\-i_" >}}) — Φ(_S_{{< sub "_i_" >}}', _S_{{< sub "_i_" >}}).
*   That is, _i_'s incentive matches the potential's gradient.