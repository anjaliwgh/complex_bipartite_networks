Code accompanying A gauge-invariant clustering coefficient for complex-weighted bipartite networks.


Code_Complex_Bipartite_Networks.ipynb contains the computations behind Theorem 11, Corollary 12 and Lemma A.1, and the four checks reported in Appendix C.3:

1. the covariances $\kappa_1$ and $\kappa_2$, by direct sampling of the link phases;

2. the counts $\tilde m_u$, $P^{(1)}_u$, $P^{(2)}_u$, against brute-force enumeration of all pairs of squares, on lattices and on rewired networks, for nodes of both classes;

3. Corollary 12 against simulation on the regular lattice, across $\Delta$ and degree;

4. Eq. (18) node by node on fixed rewired topologies.


Running:

pip install -r requirements.txt


jupyter lab resolution.ipynb


The seed is fixed, so the stored outputs are reproducible.


## Contents

| Function | Description |
|---|---|
| `ring_lattice`, `rewire`, `random_phases` | The bipartite Watts–Strogatz ensemble of Section 3.5 |
| `phase_factor` | $Q_u$ for every node, from the sparse matrix form of Proposition 8 |
| `moments` | $\sigma^2$, $\kappa_1$, $\kappa_2$ of Eq. (19) |
| `square_pair_counts` | The $O(nk^2)$ counts of overlapping pairs of squares |
| `square_pair_counts_bruteforce` | Direct enumeration, for validation |
| `ring_counts` | The closed forms of Corollary 12 |
| `var_Q`, `var_Q_independent` | Eq. (18) and the estimate $2\sigma^2/m_u$ |

Quantities for nodes of $\mathcal{V}$ are obtained by passing the transpose of the biadjacency matrix.
