---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: Lecture and Recitation Notes
parent_type: CourseSection
parent_uid: 9f4e8596-124d-1608-f9e6-b335a917765a
title: Recitation 10 Notes
uid: c12605b9-6f3b-3003-c15f-17c54b313a4c
---

Topics
------

*   Repeated games
*   Infinitely repeated prisoner's dilemma
*   Finitely repeated prisoner's dilemma 

Repeated Games (A Special Case of Dynamic Games)
------------------------------------------------

In the real world, strategic interactions continue over a period of time. Dynamic games incorporate time structure into sets of strategies and sets of payoffs. 

Recall the Prisoner's Dilemma:

{{< tableopen >}}
{{< theadopen >}}
{{< tropen >}}
{{< thopen >}}
 
{{< thclose >}}
{{< thopen >}}
C
{{< thclose >}}
{{< thopen >}}
 D
{{< thclose >}}

{{< trclose >}}

{{< theadclose >}}
{{< tropen >}}
{{< thopen >}}
C
{{< thclose >}}
{{< tdopen >}}
(1, 1)
{{< tdclose >}}
{{< tdopen >}}
(-1, 2)
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< thopen >}}
D
{{< thclose >}}
{{< tdopen >}}
(2, -1)
{{< tdclose >}}
{{< tdopen >}}
(0, 0)
{{< tdclose >}}

{{< trclose >}}

{{< tableclose >}}

Both cooperate (1,1): Cooperative outcome (against individual's incentives?).  
Both defect (0,0): Nash equilibrium outcome.

_Question_: When can "cooperative outcome" be sustained?  
Example: Unilever and P&G price fixing in 2011 or a lysine cartel in the 1990's.

_Answer:_ When the game is played repeatedly, "cooperative outcomes" can be sustained as an equilibrium! This means no incentive to deviate!

Infinitely Repeated Prisoner's Dilemma
--------------------------------------

_Folk Theorem_: (C, C) → (C, C) → ... can be a equilibrum outcome if players are patient enough. 

{{< tableopen >}}
{{< tropen >}}
{{< tdopen >}}
 
{{< tdclose >}}
{{< thopen >}}
C 
{{< thclose >}}
{{< thopen >}}
D 
{{< thclose >}}
{{< tdopen >}}
 
{{< tdclose >}}
{{< tdopen >}}
 
{{< tdclose >}}
{{< tdopen >}}
 
{{< tdclose >}}
{{< tdopen >}}
 
{{< tdclose >}}
{{< thopen >}}
C
{{< thclose >}}
{{< thopen >}}
D 
{{< thclose >}}

{{< trclose >}}
{{< tropen >}}
{{< thopen >}}
C 
{{< thclose >}}
{{< tdopen >}}
(1, 1)
{{< tdclose >}}
{{< tdopen >}}
(-1, 2)
{{< tdclose >}}
{{< tdopen >}}
 
{{< tdclose >}}
{{< tdopen >}}
→
{{< tdclose >}}
{{< tdopen >}}
 
{{< tdclose >}}
{{< thopen >}}
C
{{< thclose >}}
{{< tdopen >}}
(1, 1)
{{< tdclose >}}
{{< tdopen >}}
(-1, 2)
{{< tdclose >}}
{{< tdopen >}}
→  ...
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< thopen >}}
D
{{< thclose >}}
{{< tdopen >}}
(2, -1)
{{< tdclose >}}
{{< tdopen >}}
(0, 0)
{{< tdclose >}}
{{< tdopen >}}
 
{{< tdclose >}}
{{< tdopen >}}
 
{{< tdclose >}}
{{< tdopen >}}
 
{{< tdclose >}}
{{< thopen >}}
D
{{< thclose >}}
{{< tdopen >}}
(2, -1)
{{< tdclose >}}
{{< tdopen >}}
(0, 0)
{{< tdclose >}}

{{< trclose >}}

{{< tableclose >}}

_Proof_:

Consider the following strategy for player 1:

*   _t_ = 1: Play C.
*   _t_ ≥ 2: If player 2 has been playing C up to period _t_, play C; otherwise, play D.

Consider the same strategy for player 2. 

Let's check that this is an equilibrium:

1.  At period _t_, suppose they have been playing (C, C).  
    By sticking to C, one obtains 1 + 𝛿 + 𝛿{{< sup "2" >}} + ... = 1/(1-𝛿 ).  
    By deviating to D, one obtains 2 + 0 + 0 + ... = 2.  
    → If 𝛿 ≥ ½, no incentive to deviate.
2.  At period _t_, suppose either has deviated to D.  
    By sticking to D, one obtains 0 + 0 + ... = 0.  
    By deviating to C, one obtains -1 + 0 + ... = -1  
    → No incentive to deviate. 

Thus, this pair of strategies constitutes an equilibrium. Intuiton: Players can punish opponents' deviation in future periods. 

Finitely Repeated Prisoner's Dilemma
------------------------------------

What if players can only play for a fixed _T_ times? Cooperation is not sustainable.

_Proof:_

1.  Consider similar strategies and suppose they have coopperated until _T-1_. At period _T_:  
    By sticking to C, one obtains 1.  
    By deviating to D, one obtains 2.   
    → Incentive to deviate.
2.  Consider similar stategies except for playing D at _T_. At _T-1_:  
    By playing C, one obtains 1 + 0 = 1.  
    By deviating to D, one obtains 2 + 0 = 2.  
    → Incentive to deviate.

By induction, they have incentives to deviate unless they play (D, D) in all periods.