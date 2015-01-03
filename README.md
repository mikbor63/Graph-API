Graph-API
=========

A standard API that provides methods for Graphs.

### Documentation

   This package represents a general unlabeled graph whose vertices are denoted by positive integers.  A graph may be directed or undirected.  For an undirected graph, outgoing and incoming edges are the same. Graphs may have self edges, but no multi-edges (edges with the same end points). Edges in a Graph are ordered by the sequence in which they were added.
   
   1. vertexSize() - Returns the number of vertices in me.
   2. maxVertex()  - Returns my maximum vertex number, or 0 if I am empty.
   3. edgeSize()   - Returns the number of edges in me.
   4. isDirected() - Returns true iff I am a directed graph.
   5. outDegree(int v) - Returns the number of outgoing edges incident to V, or 0 if V is not one of my vertices.
   6. inDegree(int v) - Returns the number of incoming edges incident to V, or 0 if V is not one of my vertices.
   7. degree(int v) - Returns outDegree(V). This is simply a synonym, intended for use in undirected graphs.
   8. contains(int u) - Returns true iff U is one of my vertices.
   9. contains(int u, int v) - Returns true iff U and V are my vertices and I have an edge (U, V).
   10. add() - Returns a new vertex and adds it to me with no incident edges. The vertex number is always the smallest                     integer >= 1 that is not currently one of my vertex numbers. 
   11. add(int u, int v) - Add an edge incident on U and V. If I am directed, the edge is directed (leaves U and enters V).                Assumes U and V are my vertices.  Has no effect if there is already an edge from U to V.  Returns U.
   12. remove(int v) - Remove V, if present, and all adjacent edges.
   13. remove(int u, int v) - Remove edge (U, V) from me, if present.
   14. vertices() - Returns an Iteration over all vertices in numerical order.
   15. successor(int v, int k) - Return successor K of V, numbering from 0, or 0 if there is no such successor (or V is not                a vertex).
   16. predecessor(int v, int k) - Return predecessor K of V, numbering from 0, or 0 if there is no such predecessor.                      Assumes V is one of my vertices.
   17. neighbor(int v, int k) - Return neighbor K of V, numbering from 0, or 0 if there is no such neighbor.  Assumes V is                 one of my vertices. This is a synonym for successor(v, k).
   18. successors(int v) - Returns an iteration over all successors of V in the order the edges to them were added.  Empty                 if V is not my vertex.
   19. predecessors(int v) - Returns an iteration over all predecessors of V in the order the edges to them were added.                    Empty if V is not my vertex.
   20. neighbors(int v) - Returns successors(V).  This is a synonym typically used on undirected graphs.
   
   
