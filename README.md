# Breadth-First Maze Navigation Algorithm

Implemented in Python 3.3

## Pseudocode

**ALGORITHM**   *BFS(maze[0… n-1, 0… m-1], start, end)*
<br>&nbsp;&nbsp;&nbsp;&nbsp;**Input:** A 2D array maze[0… n-1, 0… m-1] of characters and the starting/ending coordinates in that maze.
<br>&nbsp;&nbsp;&nbsp;&nbsp;**Output**: Shortest path from start to end
```
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
```
1.	Input Size: n, m
2.	Basic operation: add newPath to the queue
3.	Efficiency Class: O(nm)
