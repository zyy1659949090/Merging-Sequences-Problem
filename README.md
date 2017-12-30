# Merging-Sequences-Problem

Merging Sequences Problem

Description

Let S be a sequence of n integers, where S[k] with 1 <= k <= n denotes the k-th number of S. The maximum prefix sum of S, denoted h(S), is defined to be 
h(S) = max0<=j<=n∑1<=k<=jS[k].

(Note that the range for j starting from 0 is to ensure h(S) >= 0, because ∑1<=k<=0S[k]=0.) For example, if 
W = −2, 1,−3; 

X = 1, 2, 4, 3,−1,−5, 2, 0,−1, 3,−2; 
Y = −1, 2, 0, 1, 3,−5, 3, 2, 4,−2,−1, 
then h(W) = 0, h(X) = 1+2+4+3 = 10 and h(Y) = −1+2+0+1+3−5+3+2+4 = 9. 
For each i = 1, 2, . . . , l, let Si be a sequence of ni integers. We say that a sequence S of n numbers is a merged sequence of S1, S2, . . . , Sl if the following conditions hold. 
1. n = n1 + n2 + ... + nl. 
2. There is a 1-1 mapping f from {1, 2, . . . , n} to {(i, j) | 1 <= i <= l and 1 <= j <= ni} such that if f(t) = (i, j) then S[t] = Si[j]. 

3. If t < t', f(t) = (i, j) and f(t') = (i, j'), then j < j'. 
For example, if we have 
S1 = 1, 3,−5, 2,−2; 
S2 = 2, 4,−1; 
S3 = −1, 0, 3, 
then both X and Y above are merged sequences of S1, S2, S3. The following sequence,however, is not a merged sequence of S1, S2, S3. 
Z = 1, 3,−5, 2,−2, 2, 4,−1,−1, 3, 0. 

(Clearly, if the last two numbers 3 and 0 in Z are exchanged, then the resulting sequence is a merged sequence of S1, S2, S3.) 
Your job is to produce a merged sequence S of S1, S2, . . . , Sl with minimum h(S*). 
For instance, the following sequence is a merged sequence for the above S1, S2, S3 whose maximum prefix sum is minimized: 
S* = −1, 1, 0, 3,−5, 2,−2, 2, 4,−1, 3. 
One can verify that h(S) = −1 + 1 + 0 + 3 − 5 + 2 − 2 + 2 + 4 − 1 + 3 = 6. 

Input

The first line contains a number m with 1 <= m <= 10 indicating the number of test cases. Each of the next m lines lists a test case. Each test case lists those l (1 <= l <= 5) input sequences separated by numbers 9999. Each test case ends with a number −9999. Two consecutive numbers in a sequence are separated by at least one single space. You may assume that each input sequence consists of at most 100 integers, each of which is between −100 and 100.

Output

For each test case S1, S2, . . . , Sl, output its h(S*) in a single line.

Sample Input

3
1 3 -5 2 -2 9999 2 4 -1 9999 -1 0 3 -9999
5 1 1 9999 -2 -2 -2 9999 10 -20 -9999
-2 1 -3 -9999

Sample Output

6
4
0
