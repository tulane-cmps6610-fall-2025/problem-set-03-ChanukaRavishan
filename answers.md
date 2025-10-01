# CMPS 6610 Problem Set 03
## Answers

**Name:** Chanuka Algama


Place all written answers from `problemset-03.md` here for easier grading.

Part 1

- **1a.** Implemented def isearch(L, x):

 output in "/problem-set-03-ChanukaRavishan/Screenshot 2025-09-30 at 7.45.59 PM.png"


- **1b.** 

    This is a sequential function. It makes a single recursive call with input reduced by just one element.

    **Work**: $W(n) = W(n-1) +1$;  Therefore its a balanced work.

    Therefore **Work: $O(n)$**

    **Span**: $S(n) = S(n-1) +1$; Therefore the span is balanced

    **Span: $O(n)$**


- **1c.** Implemented def rsearch(L, x):

output in "/problem-set-03-ChanukaRavishan/Screenshot 2025-09-30 at 8.29.13 PM.png"

- **1d.**


    Work: Each element gets compared once (e == x) → O(n). Then the reduce combines results in a tree of O(n) operations.

    Therefore, Work: **$W(n) = O(n) + O(n) = O(n)$**

    Span: Reduce builds a binary tree of height log n.

    Therefore, Span: **$S(n) = O(1) + O(logn) = O(logn)$**



- **1e.**

    Every element of a gets processed still once, plus the O(1) to combine work per call.

    So total **Work: $O(n)$**

    

Span: $S(n) = max(S(n/3), S(2n/3)) + O(1)$ = $S(2n/3) +O(1)$ Recurrnece stops after k steps when $(2/3)^k \cdot n =1$. $n=(3/2)^k$ $k = log_{3/2}(n)$

So **$S(n) = O(logn)$**



- **3b.**




- **3d.**





- **3f.**




- **4a.**




- **4b.**





- **4c.**




