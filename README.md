# Enhancing-Response-Generation-with-Refined-Vector-Search
> Our project aims to revolutionize response generation within the realm of natural language processing by leveraging Retrieval-Augmented Generation (RAG) and optimizing vector search techniques. By enhancing the search for vectors most similar to a given query within our Vector DataBase, we seek to elevate the quality and relevance of generated responses. To achieve this, we're employing a sophisticated blend of metaheuristic algorithms alongside graph-based and search algorithms. These methodologies enable us to refine the selection of vectors efficiently, ensuring that the responses generated by our system are not only accurate but also contextually appropriate. Through this innovative approach, we're pushing the boundaries of response generation, paving the way for more advanced and nuanced interactions between humans and AI systems.
![](https://miro.medium.com/v2/resize:fit:828/format:webp/0*WYv0_CaBmCTt7FXc)
# Navigable Small World Graphs
> This algorithm implements a random walk algorithm on a graph to find nodes that are most similar to a given query node based on cosine similarity of their embeddings. The function takes as input a graph representation and a query node. It conducts multiple random walks from different starting points in the graph, calculating cosine similarity between the embeddings of visited nodes and the query node. It iteratively explores neighboring nodes, updating the current node to the most similar neighbor if its similarity exceeds the current best similarity. The process continues until a stopping condition is met. Finally, it returns the top-k most similar nodes along with their similarity scores and the execution time of the algorithm.
![image.png](https://cdn.sanity.io/images/vr8gru94/production/5ca4fca27b2a9bf89b06748b39b7b6238fd4548c-1920x1080.png)
# HNSW
> This algorithm implements the Hierarchical Navigable Small World (HNSW) algorithm for approximate nearest neighbor search on a graph. It takes as input the graph representation, the embedding vector of the query, and parameters such as M (the number of bi-directional links created for every new element during construction) and ef_construction (the size of the dynamic list for the nearest neighbors).

> The function first extracts the embeddings of all nodes in the graph and initializes an HNSW index. It then adds these embeddings to the index and conducts a k-nearest neighbor search on the index using the embedding vector of the query. Finally, it returns the labels of the nearest neighbor nodes and the execution time of the algorithm.
![image.png](https://cdn.sanity.io/images/vr8gru94/production/d6e3a660654d9cb55f7ac137a736539e227296b6-1920x1080.png)
# the Simulated Annealing algorithm
> Simulated annealing is an optimization algorithm that iteratively explores and refines solutions to find the optimal solution to a problem. It starts with an initial solution and gradually improves it by making random changes and accepting them based on a probability determined by the current temperature and the difference in solution quality. As the algorithm progresses, the temperature decreases, leading to a more focused search for the optimal solution. Simulated annealing strikes a balance between exploration and exploitation, making it effective for a wide range of optimization tasks.
# Summary
## Performance Metrics

### With n_vectors = 743
| Algorithm                                 | Mean of similarity scores | Execution Time (seconds) |
|-------------------------------------------|---------------------------|--------------------------|
| Navigable Small World Graphs              | 0.458                     | 11.74                    |
| Hierarchical Navigable Small Worlds       | 0.474                     | 0.142                    |
| Simulated Annealing                       | 0.497                     | 57.8                     |

### With n_vectors = 1404
| Algorithm                                 | Mean of similarity scores | Execution Time (seconds) |
|-------------------------------------------|---------------------------|--------------------------|
| Navigable Small World Graphs              | 0.486                     | 18.29                    |
| Hierarchical Navigable Small Worlds       | 0.494                     | 0.22                     |
| Simulated Annealing                       | 0.51                      | 61.04                    |

### With n_vectors = 2175
| Algorithm                                 | Mean of similarity scores | Execution Time (seconds) |
|-------------------------------------------|---------------------------|--------------------------|
| Navigable Small World Graphs              | 0.497                     | 25.39                    |
| Hierarchical Navigable Small Worlds       | 0.499                     | 0.408                    |
| Simulated Annealing                       | 0.5258                    | 61.4                     |

 
