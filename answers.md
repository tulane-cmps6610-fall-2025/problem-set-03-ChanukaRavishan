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


- **2a.**

### python implementation
    '''
    def dedup(A):
        S = empty_set()
        out = []
        for a in A:
            if a not in S:
                S.add(a)
                out.append(a)
        return out

    '''

### Sparc implementation

    '''
    dedup(A):
    // input is a sequence A of length n
    // output is a sequence B of elements from A, should preserve order of A and cannot have duplicates

    spec:
    - For each element a in A:
        if 
            (a occurs earlier in A, should ignore it)
        else 
            (append it to B)
    
    - Return B

    '''

    **Work: $O(n)$** since performing n number of lookups with O(1) work
    
    **Span: $O(n)$** since performing n number of operations


- **2b.**

    Now that we have A_0, ........, A_m lists, each list having n elements.

    Important hint from the question: "In the distributed setting all we care about is identifying the unique elements, without regard to the order in which they appear in the input lists" So we can do parallelization
    
    '''
    multi-dedup(A0, A1, ..., Am):

        // input is a m number of lists of length n
        // output is a sequence containing each distinct element of A0∪...∪Am

        spec:
        - ∀ element x in A_0...Am, x appear in B iff x is in atleast on A_i
        - return B (order does not matter)

    ''' 

    **Work: $O(n)$** 
    
    **Span: $O(logn)$**

- **2c.**

    In dedup where we did order preserving sequential operations didnt help much.

    But in Multi-dedup Sequence operations such as like flatten and reduce are useful.

- **3b.**


    $W(n) = W(n-1) + O(1)$ 
    
    The work is balanced. and Since a constant work is done at every step work: $O(n)$.

    $S(n) = S(n-1) + O(1)$ = $O(n)$


- **3d.**

    $W(n) = W(n/2) + cn$. 
    
    This work is root dominated
    
    Therefore, $W(n) = O(n)$

    $S(n) = S(n/2) + 1$ : $S(n) = O(logn)$


- **3f.**

    $W(n) = 2W(n/2) + O(1)$. 
    
    This is leaf dominated as work of first level is one while the second level is two
    
    Number of leaves is $n^{log_2(2)}$ = n. 
    
    Therefore **$W(n) = O(n)$**


    $S(n) = S(n/2) + O(1)$ 
    
    Therefore **$S(n) = O(logn)$**.


- **4a.**




- **4b.**





- **4c.**




