Java Code Challenges.

N = days of average home sale price data

K = a fixed window size

As we look at patterns across windows of certain sizes, we will need to efficiently track trends such as increasing and decreasing subranges.

For this problem, you are given N days of average home sale price data, and a fixed window size K . For each window of K days, from left to right, find the number of increasing subranges within the window minus the number of decreasing subranges within the window.

A window of days is defined as contiguous range of days. Thus, there are exactly N-K+1 windows where this metric needs to be computed. An increasing subrange is defined as a contiguous range of indices [a,b], a < b , where each element is larger than the previous element. A decreasing subrange is similarly defined, except each element is smaller than the next.

Constraints

1 ≤ N ≤ 50,000 days
1 ≤ K ≤ N days
Input Format

Line 1: Two integers, N and K.
Line 2: N positive integers of average home sale price, each less than 1,000,000.

Output Format

One integer for each window’s result, with each integer on a separate line.

Sample Input

5 3
188930 194123 201345 154243 154243

Sample Output

3
0
-1

Explanation

For the first window of [188930, 194123, 201345], there are 3 increasing subranges ([188930, 194123, 201345], [188930, 194123], and [194123, 201345]) and 0 decreasing, so the answer is 3. For the second window of [194123, 201345, 144500], there is 1 increasing subrange and 1 decreasing, so the answer is 0. For the third window of [201345, 154243, 154243], there is 1 decreasing subrange and 0 increasing, so the answer is -1.

Runtime

Your solution should run in less than 30 seconds with a valid input of any size (within the given constraints).
