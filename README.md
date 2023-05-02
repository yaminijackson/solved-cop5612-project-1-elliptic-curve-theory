Download Link: https://assignmentchef.com/product/solved-cop5612-project-1-elliptic-curve-theory
<br>
<h1>1           Problem definition</h1>

An interesting problem in arithmetic with deep implications to <em>elliptic curve theory </em>is the problem of finding <em>perfect squares that are sums of consecutive squares</em>. A classic example is the Pythagorean identity:

3<sup>2 </sup>+ 4<sup>2 </sup>= 5<sup>2                                                                                           </sup>(1)

that reveals that the sum of squares of 3<em>,</em>4 is itself a square. A more interesting example is Lucas‘ <em>Square Pyramid</em>:

1<sup>2 </sup>+ 2<sup>2 </sup>+ <em>… </em>+ 24<sup>2 </sup>= 70<sup>2                                                                            </sup>(2)

In both of these examples, sums of squares of consecutive integers form the square of another integer.

The goal of this first project is to use F# and the actor model to build a good solution to this problem that runs well on multi-core machines.

<h1>2           Requirements</h1>

<strong>Input: </strong>The input provided (as command line to your program, e.g. my app) will be two numbers: <em>N </em>and <em>k</em>. The overall goal of your program is to find all <em>k </em>consecutive numbers starting at 1 and up to <em>N</em>, such that the sum of squares is itself a perfect square (square of an integer).

1

<strong>Output: </strong>Print, on independent lines, the first number in the sequence for each solution.

Example 1:

dotnet fsi proj1.fsx 3 2

3 indicates that sequences of length 2 with start point between 1 and 3 contain 3,4 as a solution since 3<sup>2 </sup>+ 4<sup>2 </sup>= 5<sup>2</sup>. Example 1:

dotnet fsi proj1.fsx 40 24

1 indicates that sequences of length 24 with start point between 1 and 40 contain 1,2,…,24 as a solution since 1<sup>2 </sup>+ 2<sup>2 </sup>+ <em>… </em>+ 24<sup>2 </sup>= 70<sup>2</sup>.

<strong>Actor modeling: </strong>In this project you have to use exclusively the actor facility in F# (<strong>projects that do not use multiple actors or use any other form of parallelism will receive no credit</strong>). A model similar to the one indicated in class for the problem of adding up a lot of numbers can be used here, in particular define <em>worker </em>actors that are given a range of problems to solve and a <em>boss </em>that keeps track of all the problems and perform the job assignment.

<strong>README file       </strong>In the README file you have to include the following material:

<ul>

 <li>Size of the <em>work unit </em>that you determined results in best performance for your implementation and an explanation on how you determined it. Size of the work unit refers to the number of sub-problems that a worker gets in a single request from the boss.</li>

 <li>The result of running your program for dotnet fsi proj1.fsx 1000000 4</li>

 <li>The running time for the above as reported by time for the above, i.e. run time scala project1.scala 1000000 4 and report the time. The ratio of CPU time to REAL TIME tells you how many cores were effectively used in the computation. If your are close to 1 you have almost no parallelism (points will be subtracted).</li>

 <li>The largest problem you managed to solve.</li>

</ul>

<h1>3           BONUS</h1>

Use remote actors and run you program on 2+ machines. Use your solution to solve a really large instance such as: dotnet fsi proj1.fsx 100000000 20. To get the bonus points you have to give a demo to the instructor and explain your solution.

2