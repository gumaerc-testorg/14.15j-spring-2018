---
content_type: page
description: 'This is the recitation 12 notes on networks. '
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: Lecture and Recitation Notes
parent_type: CourseSection
parent_uid: 9f4e8596-124d-1608-f9e6-b335a917765a
title: Recitation 12 Notes
uid: 2ec1c32b-4e76-eb2c-1162-a12d99c0d41e
---
## Topics

- Bargaining on Networks
- Contagion Models
- Mean-Field Approximation

## Recall

- Take-it-or-leave-it offer:
    - One party makes an offer.   
        Then, the other party accepts or rejects it.   
        Game end.
    - The proposer takes all the surplus. 
- Rubinstein's bargaining:
    - One party makes an offer.   
        The other party accepts or rejects.   
        If rejected, he makes a counter offer.   
        Continue until a party accepts.
    - The first proposer takes *1/(1 + δ)*. The offeree takes *δ/(1 + δ)*.

## Bargaining on Networks

What if there are two sellers?

- Take-it-or-leave-it offer:
    - If *S*{{< sub "1" >}} offers *p*, *S*{{< sub "2" >}} has incentive to offer *p — ε*.
    - Even if sellers make (simultaneous) offers, they receive 0. The buyer receives 1.
- Rubinstein's bargaining:
    - If *S<sub>1</sub>* offers *1/(1 + δ)*, *S<sub>2</sub>* has incentive to offer *1/(1 + δ) — ε*.
    - Again, the sellers receive 0, the buyer takes it all. 

## Contagion Models

Recall games with externalities

- *N* = \[0, 1\]
- *S*{{< sub "i" >}} = {Adopt, Not Adopt}

{{< resource uuid="4a315788-e2ae-30ae-e7e7-76502c0e6ccc" >}}

- Where *X* is the share of adoption. 

This has externalities, but network structure doesn't matter. In reality, you may register for Instagram not only because it is popular, but also because your friends have it. 

Consider undirected graph (*V*, *E*), *N*(*i*) ⊂ *V*   
Where *V* are vertices, *E* are edges, and *N* is the set of neighbors of vertex *i* ∈ *V*.

- *N* = *V*
- *S*{{< sub "i" >}} = {Adopt, Not Adopt} = {1, 0}.

{{< resource uuid="ebe54f2e-003b-b4f7-f555-c8a6162e47ba" >}}

### *Example*

{{< resource uuid="730cf581-98bc-3524-7301-325c83d4c238" >}}

- Too complicated to solve (many-body problem).
- Nor do we care about particular solution on particular networks. Often concerned with particular degree distribution, but not finer details.
- Mean-field approximation to solve for stationary equation. 

To solve:

1. Consider random graph with the degree distribution and fix some neighbor adoption probability *X*. 
2. Obtain best response strategy given *X* and compute adoption share *X̂*.
3. Derive fixed point. 

### *Example*

Let *N* = *V* = \[0, 1\] and 

 

{{< resource uuid="bb8b417c-8721-9fb7-8a79-2637521a92c1" >}}

 

- Agents are heterogeneous *c*{{< sub "i" >}} ~ *F*(0, 1).
- Degree distribution *d<sub>i</sub>* ~ *D*.

To solve:

1. Fix some *X*. Pick agent *i* randomly.
2. *i* with *c<sub>i</sub>* and *d<sub>i</sub>* would adopt if

{{< resource uuid="bdba4e6e-80f6-4c4d-ca15-c2562a751350" >}}

1. Since *c<sub>i</sub>* ~ *F*\[0, 1\], the probability that a random person with degree *d<sub>i</sub>* (but unknown *c<sub>i</sub>*) adopts is *F*(*V*(*d<sub>i</sub>*, *X*)). Since *d<sub>i</sub>* ~ *D*, we have the share of adoption 𝔼<sub>D</sub>\[*F*(*V*(*d<sub>i</sub>*, *X*))\] . From here, we can compute the neighbor adoption share *X̂*.