Download Link: https://assignmentchef.com/product/solved-cs440-homework-2
<br>
<table width="323">

 <tbody>

  <tr>

   <td>Use the generic graph search method covered in class. carry out BFS, DFS, uniform-cost, and A* over the graph and the heuristic function given in the figure. The start state is <em>xI = </em>A and the goal state is <em>xG </em>= <em>F. </em>For a given state, its neighbors appear in the ad­jacency list in an alphabetical order. For example,</td>

  </tr>

 </tbody>

</table>

<table>

 <tbody>

  <tr>

   <td width="53"><em>x</em></td>

   <td width="53"><em>h(x)</em></td>

  </tr>

  <tr>

   <td width="53">A</td>

   <td width="53">6</td>

  </tr>

  <tr>

   <td width="53"><em>B</em></td>

   <td width="53">4</td>

  </tr>

  <tr>

   <td width="53"><em>C</em></td>

   <td width="53">3</td>

  </tr>

  <tr>

   <td width="53"><em>D</em></td>

   <td width="53">4</td>

  </tr>

  <tr>

   <td width="53"><em>E</em></td>

   <td width="53"><em>1</em></td>

  </tr>

  <tr>

   <td width="53"><em>F</em></td>

   <td width="53"><em>0</em></td>

  </tr>

 </tbody>

</table>




it simpler to write down the solution, du­plicate nodes may be removed from the queue (without changing the behavior of the algorithm). Your answer should start with the initial queue followed by the status of the search after each <em>while </em>loop. Search status should be given as the node that gets expanded followed by the current queue. For each search, you only need to provide the complete list of statuses. For uniform-cost and A*, the entries in the queue should be accompanied by the value of the evaluation function; use alphabetical order for breaking ties. As an example, the first two entries of the answer for uniform-cost search should be:

<ol>

 <li><em>q= </em>[A(0)]</li>

 <li><em>A, q = [B(3), D(4), C(5)]</em></li>

</ol>

Problem 2 [20 points]. Consider the graphs on

the right, which we denote as a cycle and an in-

finite diamond strip (IDS). The cycle has n nodes

v<sub>1</sub>,      , v<sub>71</sub> = v<sub>o</sub> that are consecutively ordered, i.e.. v<sub>i</sub> has v<sub>1</sub>_<sub>1</sub> and <em>Vi±i </em>mod n as its two neigh-

bors. with vi_i before v<sub>i+1</sub> mod n• The IDS extends infinitely to both left and right. For any node in the IDS, assume that in its adjacency list, the neighbors on the left appear before the neighbors on the right. Now consider running BFS and DFS tree and graph searches on these two graphs. For the cycle graph, suppose the start node is <em>xI = </em>v1 and the goal node is <em>xG </em>= <em>xk. </em>1 &lt; <em>k &lt; </em>n. For the diamond strip, the distance between <em>xi </em>(i.e., the green node) and <em>xG </em>(i.e., the red node) is 2m. For each of the eight search combinations, provide your estimate (i.e., in big <em>OH </em>notation) of the number of nodes that has been added to the queue when the search is complete. If you think that the search does not end, the answer should be infinity. Briefly justify your answer.

Problem 3 Prove that consistent heuristics are always admissible. That is, for a heuristics function <em>h(x) </em>and transition cost <em>c(x, </em>a, <em>x’), </em>from the assumption <em>h(x) </em>&lt; <em>c(x, </em>a, <em>x’) 144 </em>and <em>h(xG) = </em>0, prove that <em>h(x) </em>&lt; Cl; where Cl; is the optimal cost from <em>x </em>to <em>xG. </em>You may assume that all costs <em>c(x, </em>a, <em>x’) </em>are non-negative.

Problem 4. Which of the following are admissible. given admissible heuristics h1. h<sub>2</sub>? Which of the following are consistent, given consistent heuristics h<sub>1</sub>, h<sub>2</sub>? For your justification. prove starting with definitions of admissible heuristics and consistent heuristics.




<ul>

 <li>h<sub>m</sub>i<sub>n</sub>(n) = mint/4(n), h2(n)},</li>

 <li><em>hmax (n) </em>= <em>max fh<sub>i</sub>(n) , h<sub>2</sub>(n)} ,</em></li>

 <li>hu<sub>m</sub>(n) = whi (n) + (1 — <em>w)h<sub>2</sub>(n), </em>0 &lt; w &lt; 1.</li>

</ul>

Problem 5. Consider an informed, best-first search algorithm in which the evaluation function is <em>f (n) = </em>(2 <em>— w)g (n) +wh(n), </em>0 &lt; w &lt; 2. For what values of w is this algorithm guaranteed to be optimal when <em>h </em>is admissible (consider the case of TREE-SEARCH)? What kind of search does this perform when w = 0? When w = 1? When w = 2? In your proof, you may assume that if the heuristic in a standard A* search is inadmissible, then optimality cannot be guaranteed. Note that <em>f </em>(n) here does not always directly correspond to the evaluation function in a standard A* search.

Problem 6 . 4 Queens problem. Consider the 4-queens setup given in the figure. Apply hill-climbing to the problem until no more moves are possible. The objective function value of a given setup is equal to the number of pairs of attacking queens (without considering blocking). Each queen is allowed to move in the column she belongs. For breaking ties, if there are multiple choices for moving the queens, first use the left most column with the best move and then favor the least number of blocks moved. If there are still ties. move up instead of down. You need to show at each iteration the objective function value for all 16 positions and the move that you will make.

Problem 7 [. Consider the 8-puzzle problem and the two heuristics h1 and h2 from class. Recall that h1 counts the number of misplaced tiles and h2 counts the total Manhattan distance of the tiles to their target locations. Prove that both heuristics are admissible.

Problem 8. For h1 and h2 in the previous problem, show that they are consistent. Note that if you are sure you can prove consistency, you answer also works for the previous problem.