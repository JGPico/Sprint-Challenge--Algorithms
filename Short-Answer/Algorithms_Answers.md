#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)
O(n)
As n increases, the function potentially loops through n^3 times, except that a is increased n^2 times every loop. n^3 / n^2 comes out as just n, so O(n)

b)
O(n log n)
This one is interesting. the initial loop is O(n), but loops through again half as many times, so O(log n). This gives us O(n) * O(log n). 

c)
O(n)
Recursion. Normally recursion gives exponential run time complexity(c^n), with n increasing for every call of the function inside the function. This time, there is only one call of the function inside the function, so we get c^1. c^1 is linear though, because c^1 == c. Or is it constant? surley not. My gut tells me linear, because we are recursively executing the function n times, once for each bunny in this case. 

## Exercise II

Sounds like a binary search tree.
def broken_egg(n):
Input is n-story.
-- probably round nearest floor throughout

  if n / 2 is broken:
    We are still to high, loop through again, using recursion
    broken_egg(n / 2) 

  else: n / 2 is not broken:
    if n + 1 is broken: this means that (n/2) doesn't break, but (n/2) + 1 does break. 
      return n
    else: 
      we are too low, and need to test the next half-way point, but up. 
      broken_egg(something, maybe (3n/4)?)

This solution runs through one recursion every time it is called, similar to the bunny problem, so I'm gonna say O(n). . . except that we are halving the input most of the time, so O(log n), actually.  