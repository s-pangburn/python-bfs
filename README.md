#Breadth-First Search Algorithm Implementation

*Pseudocode*

ALGORITHM   BFS(maze[0… n-1, 0… m-1], start, end)
	Input: A 2D array maze[0… n-1, 0… m-1] of characters and the starting/ending coordinates in that maze.
  Output: Shortest path from start to end

initialize a queue Q with start
initialize a set V tracking visited spaces

  while Q is not empty:
  	path = Q.pop()
  	last = last node in path

  	if last == end
      return path
   	else if last is not in V
    	for all spaces adjacent to last but not in V do
        newPath = array(path)
        newPath.append(adjacentSpace)
        add newPath to the queue

    	V.add(last)
  return null

1.	Input Size: n, m
2.	Basic operation: add newPath to the queue
3.	Efficiency Class: O(nm)
Worst case, outer while loop covers every available space in the n x m maze ((n-2)(m-2))
Σ(i = 1, (n-2)(m-2)) 4 = 4(n-2)(m-2) = 4(nm - 2m - 2n + 4) = 4nm - 8m - 8n + 16 nm grows fastest, therefore O(nm)
