# GCD of more than two (or array) numbers


Given an array of numbers, find GCD of the array elements. In a previous post we find GCD of two number.

Examples:

Input  : arr[] = {1, 2, 3}
Output : 1

Input  : arr[] = {2, 4, 6, 8}
Output : 2


The GCD of three or more numbers equals the product of the prime factors common to all the numbers,
but it can also be calculated by repeatedly taking the GCDs of pairs of numbers.

gcd(a, b, c) = gcd(a, gcd(b, c)) 
             = gcd(gcd(a, b), c) 
             = gcd(gcd(a, c), b)
For an array of elements, we do following.



result = arr[0]
For i = 1 to n-1
   result = GCD(result, arr[i])
