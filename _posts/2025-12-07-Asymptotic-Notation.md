---
title: Asymptotic Notation
date: 2025-12-07 00:00:00 +0000
categories: [Programming, DSA]
tags: [algorithms]     # TAG names should always be lowercase
---


### Notes:

##### Big O:
- Gives the tight upper bound of the given function
- O(g(n)) = f(n)
- eg:- f(n) = n⁴ + 100n² + 10n + 50
	 g(n) = n⁴, is the upper bound
- g(n) gives the maximum rate of growth for f(n)

##### Guidelines for analysis:
1. ***Loops***:
	- for(i=0; i<=n; i++) //executes n times
	  m=m+2               //constant time
	- total time = c*n = cn = O(n)
2. ***Nested loop***:
	- for(i=1; i<=n; i++)     //executes n times
		for(j=1; j<=n; j++)  //executes n times
			k = k+1;        //constant time
	- total time = c*n*n = cn^2 = O(n^2)
3. ***Consecutive statements***:
	- Add the time complexities of each statement
4. ***If-else***:
	- the if-condition + either the *then* part or *else* part.
	- if(length == 0)  ==//condtion: constant==
	  return false     ==//then: constant==
	  else               ==//else part: (const+const)*n==
	  for(i:1->n)       ==//n times==
      if(condition)   ==//constant==
	    return false  ===//constant==
	- total time = c0 + c1 + (c2+c3)*n = O(n)
5. ***Logarithmic***:
	- for(i=1->n; i=i*2)
	- i is doubling every step so lets assume the loop is executing k times. 2^k = n; take log both sides
	  = log(2^k) = logn
	  = klog2 = logn
	  = ***k = logn***
	- Similarly if i=i/2 then it would still be log(n)\

##### Some common formulae:
![[Pasted image 20251207153544.png]]

##### Master Theorem:
- Used to find the time complexity of divide and conquer algorithms or the algorithms where we have a recurrence relation given.
- If the recurrence is in the form:
  ![[Pasted image 20251207153747.png]]
- The time complexity is given as:
  ![[Pasted image 20251207153843.png]]
-
### References:
