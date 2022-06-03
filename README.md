# Clustering-on-Movies-and-Actors

* Given data of Actor and movies in which actor acted, We wanted to **group similar movies together** and **group similar Actors together**
* We will form this as a **graph problem**, We will build **[bipartite Graph](https://en.wikipedia.org/wiki/Bipartite_graph)** from **sets of actors and sets of movies**, and use graph algorithms to form implicit embeddings  for every node ( movies and actors )
* We will then user **clustering** methods to **cluster similar movies and actors**


## Solution Approach

1.  Formulate problem as graph problem, we have two different sets of nodes. one for movies and second for actors, so we will use **bipartite graph**

2. Generate Node Embedding using [Representation Learning](https://stellargraph.readthedocs.io/en/stable/demos/embeddings/metapath2vec-embeddings.html?highlight=UniformRandomMetaPathWalk)
  * We will use  random walks to get embeddings for all the movies and actors
  * Two possible Random Walk Model 
      1. [ Movie, Actor, Movie ]
      2. [ Actor, Movie, Actor ]
  * We will do **100 random walks** and use randomwalks to **generate embedding using genism** 
