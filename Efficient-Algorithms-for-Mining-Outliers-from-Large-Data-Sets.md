[Efficient Algorithms for Mining Outliers from Large Data Sets](https://webdocs.cs.ualberta.ca/~zaiane/pub/check/ramaswamy.pdf)

Idea:
- Data set of N points;
- for a point `p` compute the distance of its `k`th nearest neighbour, `d(p,k)`;
- rank the points by their distance `d(p,k)` and label outliers as the `n` points whose distance is the largest;
- assumption: `n << N` for the algorithm to work.

Notes:
- three parameters, `k`, `n` and the nature of the distance;
- intuitively, the higher the distance, the more isolated is a point; 
- `k` manages the size of a potential cluster (the first neighbours are not taken into account) while `n` manages the potential number of clusters;
- should the parameters scale with N? It's in fact the case for the [implementation in pyOD](https://pyod.readthedocs.io/en/latest/pyod.models.html#module-pyod.models.knn); 