Module: Toribrot
1. Base Surface: Complex Torus / Elliptic Curve
Fix a lattice (\Lambda = \langle \omega_1,\omega_2\rangle \subset \mathbb{C}) with (\Im(\omega_2/\omega_1) > 0).
Define the complex torus: [ T^2(\tau) = \mathbb{C} / \Lambda,\quad \tau = \omega_2/\omega_1. ]
By the uniformization theorem for elliptic curves, every complex torus (\mathbb{C}/\Lambda) admits the structure of a complex elliptic curve, unique up to isomorphism. Thus there exists a complex‑analytic isomorphism [ \phi: T^2(\tau) \xrightarrow{;\cong;} E(\mathbb{C}), ] where (E) is an elliptic curve in Weierstrass form. We identify (T^2(\tau)) with (E(\mathbb{C})) via (\phi) and equip it with the elliptic curve group law.

2. Intrinsic Torus Maps
Toribrot‑Geometric uses two families of intrinsic maps.

2.1. Elliptic Endomorphism with Translation (Affine Self‑Map)
Let (E(\mathbb{C})) be the elliptic curve corresponding to (T^2(\tau)).

For an integer (m), let [ [m]: E(\mathbb{C}) \to E(\mathbb{C}) ] be the elliptic curve endomorphism “multiplication by (m)” in the group law.

This is a finite holomorphic map of degree [ \deg([m]) = m^2. ]

Fix (|m|\ge 2).

For a point (P \in E(\mathbb{C})), define [ f_{P,m}: E(\mathbb{C}) \to E(\mathbb{C}),\quad f_{P,m}(Q) = [m]Q + P. ]

Each (f_{P,m}) is a holomorphic affine self‑map of the elliptic curve: it is the composition of the group endomorphism ([m]) with a translation by (P). It is a group endomorphism if and only if (P = 0); for (P\neq 0), it is not a group homomorphism but remains a finite holomorphic map of degree (m^2). Iterating (f_{P,m}) defines one class of Toribrot‑Geometric dynamics.

2.2. Hyperbolic Toral Automorphisms (SL(2,ℤ) Mode, Smooth Category)
To define the SL(2,ℤ) mode, use a real model of the torus:

Choose (v_1, v_2 \in \mathbb{C} \cong \mathbb{R}^2) such that [ \Lambda = \mathbb{Z} v_1 \oplus \mathbb{Z} v_2, ] and identify (T^2(\tau)) with (\mathbb{R}^2/\mathbb{Z}^2) using this basis.

Let (A \in SL(2,\mathbb{Z})) be a real (2\times 2) matrix with determinant 1.

Assume (A) is hyperbolic: its eigenvalues (\lambda,\lambda^{-1}) satisfy (|\lambda|>1); let (\lambda) denote the expanding eigenvalue.

Define [ F_A: T^2(\tau) \to T^2(\tau) ] as the map induced by (x \mapsto A x) on (\mathbb{R}^2) modulo (\mathbb{Z}^2) in the chosen basis.

The induced map (F_A) depends on the chosen identification of (T^2(\tau)) with (\mathbb{R}^2/\mathbb{Z}^2), but different choices correspond via conjugation by torus diffeomorphisms.

In this SL(2,ℤ) mode, we work in the smooth (C^\infty) category on the real torus. The map (F_A) is generally not holomorphic with respect to the complex structure on (T^2(\tau)), unless (A) happens to respect that complex structure (which is exceptional).

Iterating (F_A) defines another class of Toribrot‑Geometric dynamics.

3. Pants Decomposition and Composition
3.1. Topological Pants on the Torus
A pair of pants is a compact surface homeomorphic to a sphere with three disjoint open disks removed; equivalently, a genus‑0 surface with three boundary components.

We consider:

Open subsets (U \subset T^2(\tau)),
Embeddings [ i: P \hookrightarrow U \subset T^2(\tau), ] where (P) is a pair of pants and the boundary components of (P) map to simple closed curves in (T^2(\tau)).
These pants domains are local domains for operations.

3.2. Pants Units (Local Operations)
A pants unit consists of:

A pair‑of‑pants domain (P \subset T^2(\tau)),
A map (\Phi: P \to T^2(\tau)), typically the restriction of one of the intrinsic maps (holomorphic (f_{P,m}) or smooth (F_A)) to (P) or a subdomain thereof.
The three boundary components of (P) act as interfaces. Depending on the direction of composition, two boundaries may be treated as inputs and one as output, or vice versa.

3.3. Functional Composition on Open Sets
Global Toribrot‑Geometric structures are formed by gluing pants units along boundary components and composing their maps.

Let ({(P_i, \Phi_i)}) be pants units with (P_i \subset T^2(\tau)).
Suppose boundary components of (P_i) and (P_j) are identified (glued) along a common simple closed curve (C \subset T^2(\tau)), forming a larger domain (U \subset T^2(\tau)).
Compatibility condition:
On each glued boundary component (C), the corresponding maps must satisfy:

Either (\Phi_i|_C = \Phi_j|_C), or
(\Phi_i|_C) and (\Phi_j|_C) differ by a diffeomorphism of (C) that extends to a diffeomorphism of a collar neighborhood of (C) in (T^2(\tau)).
Under this condition, one can define combined maps on unions of pants domains and extend by functional composition on overlapping open sets.

3.4. Pants Composition Graph
Each pants unit ((P_i,\Phi_i)) is represented as a node in a directed graph.
Directed edges represent the flow from input boundaries to output boundaries under gluing and composition.
The pants composition graph is required to be:

Directed, and
Acyclic, unless one explicitly constructs periodic dynamical structures—in which case directed cycles may be deliberately introduced to represent periodicity.
This graph encodes a decomposition with potentially unbounded depth and local branching constrained by the three‑boundary structure of pants.

4. Metric and Texture Fields
Let (g_0) be an initial Riemannian metric on (T^2(\tau)).

Under a hyperbolic toral automorphism (F_A) with expanding eigenvalue (\lambda), define a sequence of metrics by pullback‑renormalization: [ g_{n+1} = \lambda^{-2} (F_A)^* g_n. ]

Interpretation:

Since (\det A = 1), the toral automorphism (F_A) preserves total area on (T^2(\tau)).
The pullback ((F_A)^* g_n) expands lengths by (\lambda) along the unstable direction and contracts by (\lambda^{-1}) along the stable direction (in the linear model).
The renormalization factor (\lambda^{-2}) is introduced to normalize the growth along the unstable direction under iteration, helping to keep the metric bounded in that direction; it is not required for area preservation (which holds already because (\det A = 1)).
Derived scalar fields (e.g., norms, distortion measures, curvature proxies) obtained from ({g_n}) can be defined on open sets and restricted to pants domains. These fields are carried along and updated under the dynamics.
