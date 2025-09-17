when solving any problem , the first thing is to understand the problem because most of the problem usually fall into some of the known patterns of problem solving.

solving more problem brings more familiarity and access to more patters,
generally a lot can be understood when we see the constraints of the problem as a problem which can be solved in order of n2 is most likely going to be solved using sliding window/dp. depending on the problem.

most of the substring problems are ussually twopointer or sliding window problems, however, it might also be sovled with dp.

how to identify if a problem can be optimized using dp:
if that problem can be divided into muliple subproblems which might fall repeatedly in the recursive tree, then the problem is a dp problem.
so it is important to construct the recursive tree of a problem to understand if it can be optimized by memoization or not.

some problem related to number theory of numbers require knowledge of some basic mathmatics/ tricks like sieve of erasthothenes, can be solve with some experience. some of these problems might be surprisingly easiliy solved using bit mainipulation like the xor operator.

when it comes to graph problems, the more fundamental ones are the traversal problems, a problem can usually be solved using bfs if somewhere or somehow it depends on the node's neighbors, think rotten tomato, flood filling, etc, but other wise most problems can also be solved using dfs, which although makes use of auxillary stack space, does not use a queue directly like bfs.

all the tree problems require a good grip on recursion , usually creating a recursion tree helps in this scenarios.

a lot of problems related to top k elements are usually problems which can be solved using heaps, so which can be implemented using priority_queue's , moreover some of these might also require simple sorting.

when to use greedy algorithms. over dynamic programming / recursion: wheenver picking a local maxima/minima lead to picking /calculation of correct anser in that scenario we should prefer greedy algorithms.

most of the generic array/string problems can be solved with the help of hashing the characters, or using a set data structure.

a problem which is solved in order n2 usually has an implementation which might enable to solve it in logn or with On and On space like hashmap usage.