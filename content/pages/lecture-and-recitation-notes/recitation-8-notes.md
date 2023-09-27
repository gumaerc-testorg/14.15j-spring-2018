---
content_type: page
description: 'This contains the notes for recitation 8. '
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: Lecture and Recitation Notes
parent_type: CourseSection
parent_uid: 9f4e8596-124d-1608-f9e6-b335a917765a
title: Recitation 8 Notes
uid: a27d11ad-71e0-3bed-8734-14bb67acd0f7
---
## Topics

- Review
- Congestion Games
- Potential Games

## Recap from Last Week

A game consists of 3 elements:

1. Set of players *N*
2. Sets of strategies {*S<sub>i</sub>*}<sub>i∈N</sub>
3. Sets of payoffs {*u<sub>i</sub>*}<sub>i∈N</sub>

Given a game, what do we do?

1. Maximize the sum of everyone's payoff.
    - Socially optimal outcome (what we want to happen).
2. Maximize individual's payoff conditional on everyone else's strategy and find a fixed point.
    - Nash equilibrium (what we think will happen).

1 & 2 are often different because there are strategic interactions and individual incentives are unaligned. 

Some games have useful structures, which impose useful restrictions on {*S<sub>i</sub>*} and {*u<sub>i</sub>*}.

- Dynamic games
- Games on networks

## Congestion Games

Paths are labeled (edge, traffic, cost/duration):

{{< resource uuid="8b8ce358-1ee5-1d9f-a952-ff7b9d51a045" >}}

- Directed network (*J*, *E*) = ({*A*, *B*, *C*}, {1, 2, 3, 4}).
- Set of paths *P* = {*p<sub>1</sub>*, *p<sub>2</sub>*, *p<sub>3</sub>*} = {(1), (2,3), (2,4)}.
- Traffic on paths {*x<sub>p1</sub>*, *x<sub>p2</sub>*, *x<sub>p3</sub>*} = {*x<sub>1</sub>*, *x<sub>3</sub>*, *x<sub>4</sub>*}.
- Total (social) cost: *x<sub>1</sub>*\*L<sub>1</sub>(*x<sub>1</sub>*) + *x<sub>2</sub>*\*L<sub>2</sub>(*x<sub>2</sub>*) + *x<sub>3</sub>*\*L<sub>3</sub>(*x<sub>3</sub>*) + *x<sub>4</sub>*\*L<sub>4</sub>(*x<sub>4</sub>*).
    - Minimizing this with respect to *x*{{< sub "_1_" >}}, … *x*{{< sub "_4_" >}} gives socially optimal traffic.

As a game, this can be written:

- *N* = \[0, 1\]
- *S<sub>i</sub>* = {*p<sub>1</sub>*, *p<sub>2</sub>*, *p<sub>3</sub>*}
- *u<sub>i</sub>*(*P<sub>i</sub>*, everyone else's strategy) = *u<sub>i</sub>*(*P<sub>i</sub>*, *x<sub>1</sub>*…*x<sub>4</sub>*)

However, each individual driver incurs:

- L{{< sub "1" >}}(*x*{{< sub "_1_" >}}) if he takes *p*{{< sub "_1._" >}}
- L{{< sub "2" >}}(*x*{{< sub "_2_" >}}) + L{{< sub "3" >}}(*x*{{< sub "_3_" >}}) if he takes *p*{{< sub "2." >}}
- L{{< sub "2" >}}(*x*{{< sub "_2_" >}}) + L{{< sub "4" >}}(*x*{{< sub "_4_" >}}) if he takes *p*{{< sub "_3._" >}}

So, his best response correspondence is to choose a path that gives minimum individual cost.

- In equilibrium, we must have L{{< sub "1" >}}(*x*{{< sub "_1_" >}}) = L{{< sub "2" >}}(*x*{{< sub "_2_" >}}) + L{{< sub "3" >}}(*x*{{< sub "_3_" >}}) = L{{< sub "2" >}}(*x*{{< sub "_2_" >}}) + L{{< sub "4" >}}(*x*{{< sub "_4_" >}}).

### *Example:*

Paths are labeled (edge/path, traffic, individual cost):

{{< resource uuid="9a415541-da92-a035-9c9f-e3fb90f215fb" >}}

- Model constraint: *x*{{< sub "_1_" >}} + *x*{{< sub "_2_" >}} = 1.
- Total cost: *x*{{< sub "_1_" >}}\*L{{< sub "1" >}}(*x*{{< sub "_1_" >}}) + *x*{{< sub "_2_" >}}\*L{{< sub "2" >}}(*x*{{< sub "_2_" >}}) = *x*{{< sub "_1_" >}}{{< sup "2" >}} + *x*{{< sub "_2_" >}} = *x*{{< sub "_1_" >}}{{< sup "2" >}} + (1 — *x*{{< sub "_1_" >}}) = (*x*{{< sub "1" >}} — ½){{< sup "2" >}} + ¾.
- Socially optimal traffic: (*x<sub>1</sub><sup>S</sup>*, *x<sub>2</sub><sup>S</sup>*) = (½ , ½).

Each individual choose path with lower cost, so in equilibrium:

- L<sub>1</sub>(*x<sub>1</sub><sup>E</sup>*) = L<sub>2</sub>(*x<sub>2</sub><sup>E</sup>*), so (*x<sub>1</sub><sup>E</sup>*, *x<sub>2</sub><sup>E</sup>*) = (1, 0).
- Equilibrium total cost is *x<sub>1</sub><sup>E</sup>*\*L<sub>1</sub>(*x<sub>1</sub><sup>E</sup>*) + *x<sub>2</sub><sup>E</sup>*\*L<sub>2</sub>(*x<sub>2</sub><sup>E</sup>*) = 1 ≥ ¾.

How to solve this? 

1. Impose toll *C* on *p<sub>1</sub>*.
2. Then, *u<sub>i</sub>*(*p<sub>1</sub>*, *x<sub>1</sub>*, *x<sub>2</sub>*) = *x<sub>1</sub>* + *C*.
3. We want L<sub>1</sub>(*x<sub>1S</sub>*) + *C* = L<sub>2</sub>(*x<sub>2</sub><sup>S</sup>*).
4. *C* = ½.

## Potential Games

In physics, particles move along the unique potential field.

{{< resource uuid="770315e0-e12b-e93d-df13-24991317bfce" >}}

In society, people move along their own incentives.

{{< resource uuid="c4284b00-43ea-befd-7d88-fd6dc2a0704f" >}}

However, there are cases where people's incentives are so similar that they move as if there is a unique potential field.

### *Example: Traffic Congestion*

Definition: A game is an exact potential game if there is exists Φ (unique potential field) such that:

- *u<sub>i</sub>*(*S<sub>i</sub>*, *S<sub>\-i</sub>*) — *u<sub>i</sub>*(*S<sub>i</sub>*', *S<sub>\-i</sub>*) = Φ(*S<sub>i</sub>*, *S<sub>\-i</sub>*) — Φ(*S<sub>i</sub>*', *S<sub>i</sub>*).
- That is, *i*'s incentive matches the potential's gradient.