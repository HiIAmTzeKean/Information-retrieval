---
tags:
  - 🌱
date: 25--Dec--2023
alias: 
modified: 25--Dec--2023
---
# Vector space model
## Properties
- Terms act as the axes of the space
- Documents are the [[Vector]] in the space
- Typically a high dimensional space
- Very sparse
## Query
Queries are seen as a vector in space. Then, vector proximity from a query to another vector in the space can be used for ranking. Scoring can thus be formalised as
$$score = \frac{1}{distance}$$
Where the inverse of the distance is used. (The smaller the distance, the higher the score)
### Calculating distance
### Using [[Euclidean distance]]
- Distance cannot capture how the query could be in the same direction as another vector
- Suppose a the query is a unit vector, and there exist another vector $w$ twice the length of the query, let that distance be $d$
- Then, it is possible to create 2 other vectors that are [[Orthogonal]] to the query with the same distance $d$
- Vector $w$ would be more relevant to the query, but on ranking it would perform as well as the other 2 vectors
### Utilising angle [[Cosine similarity]]
- Using angle of [[Unit vector]] such that long and short documents have comparable weights
$$\cos(q,d)= \overrightarrow q \cdot \overrightarrow d $$

---
Links: [[Vector space]] - [[Query processing]]
