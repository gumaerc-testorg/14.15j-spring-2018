---
content_type: page
parent_title: Lecture and Recitation Notes
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
2.  Sets of strategies {_S__i_}i∈N
3.  Sets of payoffs {_u__i_}i∈N

Given a game, what do we do?

1.  Maximize the sum of everyone's payoff.
    *   Socially optimal outcome (what we want to happen).
2.  Maximize individual's payoff conditional on everyone else's strategy and find a fixed point.
    *   Nash equilibrium (what we think will happen).

1 & 2 are often different because there are strategic interactions and individual incentives are unaligned. 

Some games have useful structures, which impose useful restrictions on {_S__i_} and {_u__i_}.

*   Dynamic games
*   Games on networks

Congestion Games
----------------

Paths are labeled (edge, traffic, cost/duration):

![Congestion game diagram]({{< resource_file 8b8ce358-1ee5-1d9f-a952-ff7b9d51a045 >}})

*   Directed network (_J_, _E_) = ({_A_, _B_, _C_}, {1, 2, 3, 4}).
*   Set of paths _P_ = {_p__1_, _p__2_, _p__3_} = {(1), (2,3), (2,4)}.
*   Traffic on paths {_x__p1_, _x__p2_, _x__p3_} = {_x__1_, _x__3_, _x__4_}.
*   Total (social) cost: _x__1_\*L1(_x__1_) + _x__2_\*L2(_x__2_) + _x__3_\*L3(_x__3_) + _x__4_\*L4(_x__4_).
    *   Minimizing this with respect to _x__1_, ... _x__4_ gives socially optimal traffic.

As a game, this can be written:

*   _N_ = \[0, 1\]
*   _S__i_ = {_p__1_, _p__2_, _p__3_}
*   _u__i_(_P__i_, everyone else's strategy) = _u__i_(_P__i_, _x__1_..._x__4_)

However, each individual driver incurs:

*   L1(_x__1_) if he takes _p__1._
*   L2(_x__2_) + L3(_x__3_) if he takes _p2._
*   L2(_x__2_) + L4(_x__4_) if he takes _p__3._

So, his best response correspondence is to choose a path that gives minimum individual cost.

*   In equilibrium, we must have L1(_x__1_) = L2(_x__2_) + L3(_x__3_) = L2(_x__2_) + L4(_x__4_).

### _Example:_

Paths are labeled (edge/path, traffic, individual cost):

![Equilibrium congestion game diagram.]({{< resource_file 9a415541-da92-a035-9c9f-e3fb90f215fb >}})

*   Model constraint: _x__1_ + _x__2_ = 1.
*   Total cost: _x__1_\*L1(_x__1_) + _x__2_\*L2(_x__2_) = _x__1_2 + _x__2_ = _x__1_2 + (1 — _x__1_) = (_x1_ — ½)2 \+ ¾.
*   Socially optimal traffic: (_x__1__S_, _x__2__S_) = (½ , ½).

Each individual choose path with lower cost, so in equilibrium:

*   L1(_x1__E_) = L2(_x__2__E_), so (_x1__E_, _x2__E_) = (1, 0).
*   Equilibrium total cost is _x1__E_\*L1(_x1__E_) + _x2__E_\*L2(_x2__E_) = 1 ≥ ¾.

How to solve this? 

1.  Impose toll _C_ on _p__1_.
2.  Then, _u__i_(_p__1_, _x__1_, _x__2_) = _x__1_ + _C_.
3.  We want L1(_x1__S_) + _C_ = L2(_x2__S_).
4.  _C_ = ½.

Potential Games
---------------

In physics, particles move along the unique potential field.

![Particles moving along unique potential fields.]({{< resource_file 770315e0-e12b-e93d-df13-24991317bfce >}})

In society, people move along their own incentives.

![Diagram of people moving along their own incentives.]({{< resource_file c4284b00-43ea-befd-7d88-fd6dc2a0704f >}})

However, there are cases where people's incentives are so similar that they move as if there is a unique potential field.

### _Example: Traffic Congestion_

Definition: A game is an exact potential game if there is exists Φ (unique potential field) such that:

*   _u__i_(_S__i_, _S__\-i_) — _u__i_(_S__i_', _S__\-i_) = Φ(_S__i_, _S__\-i_) — Φ(_S__i_', _S__i_).
*   That is, _i_'s incentive matches the potential's gradient.