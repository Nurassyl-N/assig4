# assig4
---

## Class Descriptions

### `Vertex<V>`
- **Fields**  
  - `V data` — the payload (e.g., a city name).  
  - `Map<Vertex<V>, Double> adjacent` — each neighbor vertex mapped to the weight of the connecting edge.
- **Key Methods**  
  - `addAdjacentVertex(Vertex<V> neighbor, double weight)`  
  - `getAdjacentVertices(): Map<Vertex<V>, Double>`  

### `WeightedGraph<V>`
- **Fields**  
  - `Set<Vertex<V>> vertices` — all vertices in the graph.  
  - `boolean directed` — whether the graph is directed.
- **Key Methods**  
  - `addVertex(Vertex<V> v)`  
  - `addEdge(Vertex<V> u, Vertex<V> v, double weight)`  
  - `addEdge(Vertex<V> u, Vertex<V> v)` — convenience overload with default weight = 1.0  
  - `getVertices(): Set<Vertex<V>>`  

### `Search<V>` (abstract)
- Holds a reference to a `WeightedGraph<V>`.
- Declares one method:  
  ```java
  List<Vertex<V>> search(Vertex<V> start, Vertex<V> goal);
