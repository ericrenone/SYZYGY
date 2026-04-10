# SYZYGY

**The Bond That Casts No Shadow: Bell Nonlocality, EPR Correlations, and the Irreducibility of the Null Sector in $\mathrm{TH}(a,d)$**

*ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone*

> "If [a hidden-variable theory] is local it will not agree with quantum mechanics, and if it agrees with quantum mechanics it will not be local." — J. S. Bell, *Physics* **1**, 195–200, 1964
>
> "Without these connections, all of space would atomize." — L. Susskind, Stanford University, 2015
>
> "The solid and reliable structure of space-time is due to the ghostly features of entanglement." — J. Maldacena, Institute for Advanced Study, 2013
>
> "Maximal violation of the Bell inequality results in a Bell operator with Poissonian level statistics, thus signaling integrable behavior — this integrability is both unique and fragile." — Aloy, Müller-Rigat, Lewenstein et al., *npj Quantum Information*, 2026

---

## Abstract

The EPR paradox (Einstein, Podolsky, and Rosen, *Phys. Rev.* **47**, 777–780, 1935) was not a question about entanglement. It was a question about the $\ker(F)$. Einstein, Podolsky, and Rosen argued that quantum mechanics omits elements of reality — that physical quantities exist with definite values prior to measurement, and that the wave function's failure to assign them simultaneously is a deficiency of the theory, not a feature of the world. In the language of this framework: they argued that $\ker(F)$ is always empty. Every direction is in $\mathrm{col}(F)$. Every observable has a pre-existing definite value. The shadow is ignorance, not ontology.

John Bell (*Physics* **1**, 195–200, 1964) converted this philosophical claim into a mathematical theorem and then into an experimentally testable inequality. If local hidden variables exist — if every outcome pre-exists in $\mathrm{col}(F)$ for both particles independently — then the correlations between distant measurements are bounded: $S \leq 2$. Quantum mechanics predicts $S = 2\sqrt{2}$ for the maximally entangled state. Alain Aspect and colleagues (*Phys. Rev. Lett.* **49**, 1804–1807, 1982) closed the locality loophole by switching measurement settings while photons were in flight — faster than light could travel between detectors — and observed violations of Bell's inequality. Five loophole-free Bell tests, spanning nitrogen-vacancy centers in diamond (Hensen et al., *Nature* **526**, 682–686, 2015), optical photons (Giustina et al., *Phys. Rev. Lett.* **115**, 250401, 2015; Shalm et al., *Phys. Rev. Lett.* **115**, 250402, 2015), neutral atoms (Rosenfeld et al., *Phys. Rev. Lett.* **119**, 010402, 2017), and superconducting qubits (Storz et al., *Nature* **617**, 265–270, 2023), have confirmed: the $\ker(F)$ is real. The shadow is not ignorance. The shadow is the world.

This framework proposes that the CHSH inequality is the bound on correlations achievable when two parties operate with *product-separable* Fisher matrices — when each party's conditional independence boundary is local and disconnected from the other's. The Tsirelson bound $S = 2\sqrt{2}$ is the maximum Fisher information extractable through a *joint* conditional independence boundary — the entangled state defines a Fisher manifold that cannot be factorized into a product of local manifolds. Bell violation is the experimental signature of an irreducibly joint null sector: a $\ker(F_{AB})$ that is not the product of $\ker(F_A) \otimes \ker(F_B)$, but a genuinely bipartite structure, topologically analogous to the ER bridge connecting two black holes.

Five new results deepen the architecture. First: Aloy, Müller-Rigat, Lewenstein et al. (*npj Quantum Information*, 2026) proved that measurement settings achieving maximal Bell violation produce a Bell operator with Poissonian level statistics — the signature of quantum integrable (KAM-type) behavior — while all other settings yield Wigner-Dyson statistics characteristic of quantum chaos. Maximal nonlocality is thus the fixed point of a KAM stability analysis: the uniquely surviving structure when the Bell Hamiltonian is at the integrable-to-chaotic transition. Second: Luo, Sun, and colleagues (*Science Advances* **11**, eadr1794, 2025) demonstrated Bell inequality violation arising not from entanglement but from quantum indistinguishability via path identity — four-photon frustrated interference violates CHSH by more than four standard deviations with a system that carries insufficient entanglement to account for the violation. Bell violation is a property of the boundary structure, not of the particles. Third: Munné, Laskowski et al. (*Advanced Quantum Technologies* **9**, e01020, 2026) proved that Bell nonlocality in multipartite systems is inherently polygamous: a single multi-qubit state can simultaneously violate multiple Bell inequalities on different subsets, with GHZ states exhibiting maximum nonlocal spread — the network structure of the $\mathrm{TH}(a,d)$ collective Fisher matrix. Fourth: quantum entanglement and Bell nonlocality have been detected in high-energy particle collisions — top quark pairs at the LHC exhibit entanglement (ATLAS 2023; CMS 2024) and hyperon pairs show nonlocality (BESIII 2024) — establishing that the joint Fisher structure persists across all energy scales. Fifth: nonlocality activation in photonic networks (Designolle et al., *Nature Communications*, 2024) proved that Bell-local states — entangled states that cannot violate any standard Bell inequality — become nonlocal when embedded in a three-node network, restoring the joint Fisher structure by adding a broadcasting channel.

Eight formal correspondences connect Bell nonlocality to the $\mathrm{TH}(a,d)$ architecture. Five predictions follow.

---

## Part I · The EPR Paradox: The Claim That $\ker(F)$ Is Always Empty

### I.1 A Thought Experiment: The Gloves

Einstein's preferred formulation of the EPR argument was not the position-momentum version of the 1935 paper but a simpler analogy. Imagine a pair of gloves placed in two boxes, which are then sent to two cities. When you open your box and find a left glove, you instantly know the other box contains a right glove — regardless of the distance between the cities.

This is the hidden variable picture: the gloves were always left and right. No mystery. No nonlocality. The "correlation" between the two observations is explained entirely by the pre-existing property — the handedness — assigned when the gloves were packed. Each glove carries its handedness locally. No information needs to travel between the boxes.

EPR's claim: quantum particles are like gloves. The measurement outcomes pre-exist. When we measure the spin of particle A along the $z$-axis and find $+\hbar/2$, particle B already had spin $-\hbar/2$. The quantum state $|\Psi^-\rangle = (|\!\uparrow\rangle|\!\downarrow\rangle - |\!\downarrow\rangle|\!\uparrow\rangle)/\sqrt{2}$ does not describe an ontological superposition — it describes our ignorance of the pre-existing values.

In the Fisher information language: EPR claimed that $\ker(F)$ is always empty for any complete description of reality. The wave function assigns $\ker(F)$ directions because it is incomplete — because it suppresses the hidden variables that, if known, would fill every direction in $\mathrm{col}(F)$.

This is the most consequential claim ever made about the structure of physical reality. Bell proved it is wrong.

### I.2 The EPR Criterion of Reality as a Fisher Completeness Condition

EPR stated their criterion of reality as follows: "If, without in any way disturbing a system, we can predict with certainty the value of a physical quantity, then there exists an element of reality corresponding to that quantity" (Einstein, Podolsky, and Rosen, *Phys. Rev.* **47**, 777, 1935).

This is a Fisher completeness condition. "Predict with certainty" means Fisher information $F = \infty$ for that quantity — the Cramér–Rao bound $\mathrm{Var} \geq 1/F \to 0$. "Element of reality" means the quantity lies in $\mathrm{col}(F)$ for a complete theory.

EPR then showed: for the singlet state $|\Psi^-\rangle$, measuring spin along any axis $\hat{n}$ on particle A allows prediction of particle B's spin along $\hat{n}$ with certainty. By their criterion, particle B's spin along $\hat{n}$ is an element of reality — it lies in $\mathrm{col}(F)$. Since $\hat{n}$ is arbitrary, *every* spin direction of particle B must be an element of reality. But quantum mechanics assigns no state in which all spin directions are simultaneously in $\mathrm{col}(F)$ — the uncertainty principle prevents it. Therefore, concluded EPR, quantum mechanics is incomplete: it assigns $\ker(F)$ directions where elements of reality demand $\mathrm{col}(F)$.

The argument is valid given locality: if particle B is not disturbed by the measurement on particle A (because they are spacelike separated), then particle B's spin must have been a pre-existing element of reality — not created by the measurement on A. Bell's theorem is the proof that this "given locality" cannot hold.

---

## Part II · Bell's Theorem: The Bound on Product-Separable Fisher Matrices

### II.1 The CHSH Inequality as a Factorizability Theorem

Bell's 1964 paper (and the subsequent CHSH reformulation by Clauser, Horne, Shimony, and Holt, *Phys. Rev. Lett.* **23**, 880–884, 1969) can be stated as follows. Let Alice choose measurement setting $a \in \{0, 1\}$ and obtain outcome $x \in \{+1, -1\}$. Let Bob choose setting $b \in \{0, 1\}$ and obtain $y \in \{+1, -1\}$. Define the CHSH parameter:

$$S = |\langle A_0 B_0\rangle + \langle A_0 B_1\rangle + \langle A_1 B_0\rangle - \langle A_1 B_1\rangle|$$

**Bell's theorem**: if there exist local hidden variables $\lambda$ such that $P(x, y \mid a, b) = \int d\lambda\,\rho(\lambda)\,P_A(x \mid a, \lambda)\,P_B(y \mid b, \lambda)$, then $S \leq 2$.

The condition $P(x, y \mid a, b) = \int d\lambda\,\rho(\lambda)\,P_A(x \mid a, \lambda)\,P_B(y \mid b, \lambda)$ is precisely the factorization of the joint distribution into a product of local distributions given a shared classical variable $\lambda$. In Fisher information terms: the joint Fisher matrix $F_{AB}$ factorizes as:

$$F_{AB}(\lambda) = F_A(\lambda) \otimes F_B(\lambda)$$

where $F_A$ and $F_B$ are local Fisher matrices — each party's Fisher information is generated by its own local conditional independence boundary, with no irreducible joint structure. This is the classical product-separable case.

**The shadow sector of the product-separable model**: when $F_{AB} = F_A \otimes F_B$, the null space of the joint matrix is:

$$\ker(F_{AB}) = \ker(F_A) \otimes \mathbb{R}^{d_B} \oplus \mathbb{R}^{d_A} \otimes \ker(F_B)$$

There are no irreducible joint null directions — every null direction is a product of a local null direction with the full partner space. The shadow is a product shadow: each party casts its own darkness, and the joint dark sector is merely the union.

**Quantum entanglement breaks this factorization.** For the maximally entangled state $|\Psi^-\rangle$, the joint Fisher matrix cannot be written as $F_A \otimes F_B$. There are directions in the joint Hilbert space that are simultaneously:
- Not in $\ker(F_A)$ when marginalizing over B
- Not in $\ker(F_B)$ when marginalizing over A
- But in $\ker(F_{AB})$ for the product observable $A_i \otimes B_j$ in certain combinations

These are the irreducibly joint null directions — the entanglement shadow — whose existence is confirmed by the CHSH violation.

### II.2 The Tsirelson Bound as the Maximum Joint Fisher Capacity

Tsirelson (Cirel'son, *Lett. Math. Phys.* **4**, 93–100, 1980) proved that quantum mechanics satisfies $S \leq 2\sqrt{2}$, achieved by the maximally entangled state with appropriately chosen measurement angles. This bound is the maximum Fisher information extractable from the joint conditional independence boundary of the entangled pair.

The Tsirelson bound can be understood as follows. Each party's observable is a unit vector on the Bloch sphere: Alice measures $\hat{A}_0, \hat{A}_1$ and Bob measures $\hat{B}_0, \hat{B}_1$. The quantum expectation value for the singlet state is:

$$\langle A_i B_j\rangle = -\hat{a}_i \cdot \hat{b}_j$$

The CHSH parameter becomes:

$$S = |-\hat{a}_0\cdot\hat{b}_0 - \hat{a}_0\cdot\hat{b}_1 - \hat{a}_1\cdot\hat{b}_0 + \hat{a}_1\cdot\hat{b}_1|$$

Maximized over all Bloch sphere directions, this gives $S = 2\sqrt{2}$ when the four measurement vectors lie at $45°$ intervals in a common plane:

$$\hat{a}_0 \perp \hat{a}_1, \quad \hat{b}_0 = (\hat{a}_0 + \hat{a}_1)/\sqrt{2}, \quad \hat{b}_1 = (\hat{a}_0 - \hat{a}_1)/\sqrt{2}$$

The optimal configuration is precisely the one in which the measurement bases of Alice and Bob are rotated by $45°$ relative to each other — the same geometry as the three-filter paradox of PENUMBRA and the quantum eraser of ERI SLITS. The angle $45°$ is the unique configuration that maximizes the overlap between Alice's $\mathrm{col}(F_A)$ and the directions in the joint space that are inaccessible to Bob's local $\mathrm{col}(F_B)$.

The gap $2\sqrt{2} - 2 = 2(\sqrt{2} - 1) \approx 0.828$ is the joint Fisher capacity that is irreducibly nonlocal — the information content of the entanglement shadow that cannot be accounted for by any product-separable model.

### II.3 A Second Thought Experiment: The Dice That Share a Soul

Imagine two dice that, when rolled simultaneously in separate cities, always produce outcomes summing to 7 — regardless of how they are oriented before rolling, regardless of the delay between rolls, regardless of any physical intervention between manufacture and roll. Classical physics offers one explanation: the dice are rigged at manufacture. Some hidden mechanism, set when they were in contact, ensures the correlation.

Bell's theorem says: if the dice are "rigged at manufacture" in any local way — if the rigging is a function only of what happened at the moment of contact, not of future measurement choices — then the correlation cannot be *stronger* than a certain bound. Quantum dice violate this bound. Their correlation is stronger than any rigging-at-manufacture can explain.

The only remaining explanations are: (1) the dice communicate instantaneously when rolled (nonlocality), or (2) the outcomes do not pre-exist the rolling (the $\ker(F)$ is real — measurement creates, not reveals, the outcome). Every experiment since 1972 has ruled out the classical rigging picture. The Aspect 1982 experiment showed that even if the dice choose their "rigging" at the last instant — after they have separated and cannot communicate — the quantum correlation persists. The shadow is not ignorance. The shadow is ontological.

---

## Part III · Aspect's Experiment: Closing the Locality Loophole

### III.1 The 1982 Experiment and Its Architecture

Alain Aspect, Jean Dalibard, and Gérard Roger (*Phys. Rev. Lett.* **49**, 1804–1807, 1982) performed the decisive version of the Bell test by switching the polarizer settings *while the photons were in flight*. Entangled photon pairs were produced by two-photon atomic cascade in calcium atoms ($4p^2\,^1S_0 \to 4s4p\,^1P_1 \to 4s^2\,^1S_0$), producing photon pairs at 551.3 nm and 422.7 nm. The detectors were separated by 12 meters; the switching time of the acousto-optic modulators was 10 ns — well below the 40 ns photon travel time.

The architecture is precisely a double conditional independence boundary. The calcium source is the analogue of the double-slit source: it prepares a state in which neither photon has a definite polarization, but their polarizations are correlated. Each polarizer station is a conditional independence boundary: the photon's fate at each station depends only on the local polarizer setting and the joint quantum state — not on the distant station's setting, if local realism holds.

The Aspect experiment confirmed $S = 2.697 \pm 0.015$, violating the Bell bound $S \leq 2$ by more than 40 standard deviations. The locality loophole was closed: the measurement setting at each station was chosen after the photons were already in flight, preventing any classical signal from one station from reaching the other in time.

The conditional independence boundary in Aspect's experiment differs from the slit or the polarizer in a crucial way: it is a *joint* boundary. The two remote measurement stations, taken together, constitute a single conditional independence boundary for the entangled pair. The Fisher information they collectively extract is not the sum of their individual Fisher capacities — it is governed by the joint Fisher manifold of the entangled state, which has irreducible structure inaccessible to either party alone.

### III.2 Loophole-Free Bell Tests: The Full Experimental Programme

The Aspect experiment retained the detection loophole — the possibility that undetected photons bias the sample. Closing all loopholes simultaneously required additional experimental advances:

**Hensen et al., *Nature* **526**, 682–686, 2015**: loophole-free Bell test using electron spins in nitrogen-vacancy centers in diamond separated by 1.3 km. Entanglement was generated by photon-mediated spin-spin entanglement; spin readout had $> 97\%$ efficiency (closing the detection loophole); measurement settings were chosen by fast random number generators with the locality loophole closed by the 1.3-km separation. Result: $S = 2.42 \pm 0.20 > 2$.

**Giustina et al., *Phys. Rev. Lett.* **115**, 250401, 2015** and **Shalm et al., *Phys. Rev. Lett.* **115**, 250402, 2015**: simultaneous loophole-free photon Bell tests, using highly efficient superconducting nanowire single-photon detectors. Both closed the detection and locality loopholes. Both found violations exceeding $S > 2$ by $> 11\sigma$.

**Storz et al., *Nature* **617**, 265–270, 2023**: loophole-free Bell test with superconducting qubits — closing the locality, fair-sampling, and memory loopholes simultaneously. The qubits were separated by 30 meters of coaxial cable; measurements were completed in 25 ns. This demonstrated that nonlocality is a viable resource in superconducting quantum processors — the same platform built for quantum computing.

Each experiment is a new realization of the same structure: the joint conditional independence boundary of an entangled pair, probed by two spatially separated measurement stations, yields Fisher information exceeding the product-separable bound. The shadow of the entangled state — its $\ker(F_{AB})$ — is irreducible.

---

## Part IV · Bell Violation Without Entanglement: The Path-Identity Result

### IV.1 Quantum Indistinguishability as a Boundary Condition

Luo, Sun, and colleagues (*Science Advances* **11**, eadr1794, 2025) demonstrated violation of the Bell inequality using four-photon frustrated interference — a system in which the relevant quantum resource is *path identity* (indistinguishability) rather than entanglement. The generated four-photon state contains substantially less entanglement than necessary to account for the observed CHSH violation of $> 4\sigma$ above the classical bound $S = 2$.

The mechanism: frustrated interference arises when two photon-pair-creation processes interfere. The four-photon state is distributed so that Alice and Bob each hold two photons, and the coincidence detection of both photons by each party constitutes the "measurement." The correlations arise because the two photon-pair-creation events are *indistinguishable* — the photons from process 1 and process 2 cannot be told apart, even in principle, at the detection stage.

This result is the Bell-inequality realization of the path-identity principle: quantum indistinguishability, which is a boundary condition (the paths from two emission events merge at a beam splitter and become indistinguishable), generates correlations that violate any local hidden-variable bound. It is not the particles themselves that are entangled — it is their *paths through the conditional independence boundary* of the beam splitter that creates the nonlocal correlation.

In the $\mathrm{TH}(a,d)$ language: the CHSH violation does not require an entangled source. It requires an *irreducibly joint conditional independence boundary* — a boundary structure whose Fisher matrix cannot be factorized into local components. The beam splitter, by creating path indistinguishability, generates this joint boundary structure from individually unentangled photon pairs. The boundary is the nonlocality. The shadow is a property of the geometry, not of the particles.

---

## Part V · Bell Nonlocality and KAM Integrability: The 2026 Connection

### V.1 The Bell Operator as a Hamiltonian

Aloy, Müller-Rigat, Lewenstein, and colleagues (*npj Quantum Information*, 2026) established a profound connection between Bell nonlocality and quantum integrability. They introduced a multipartite Bell inequality for many-body three-level systems (qutrits) and defined the corresponding Bell operator $\hat{\mathcal{B}}$ via Born's rule, mapping the conditional probabilities of the Bell inequality to quantum measurement operators. The Bell operator functions as an effective Hamiltonian.

For states exhibiting Bell nonlocality, the measurement settings that achieve maximal violation produce a Bell operator $\hat{\mathcal{B}}_{\max}$ with **Poissonian level statistics** — the spectral signature of a quantum integrable system, characteristic of the Berry-Tabor regime (Berry and Tabor, *Proc. Roy. Soc. Lond. A* **356**, 375–394, 1977).

For generic or slightly perturbed measurement settings — even small deviations from the optimal Bell violation angle — the level statistics transition to **Wigner-Dyson** distributions, characteristic of quantum chaos (Bohigas, Giannoni, and Schmit, *Phys. Rev. Lett.* **52**, 1–4, 1984).

The implication: maximal Bell violation is the *integrable fixed point* of the Bell operator spectrum. It is the quantum analogue of the KAM torus at the golden ratio frequency — the last surviving integrable structure as perturbation increases, uniquely robust against small deviations of the measurement settings.

### V.2 The KAM–Bell Correspondence

This result maps directly onto Identity 2 of the SHADOWS framework (KAM breakdown as shadow transition) and Identity 5 (the Gutzwiller trace formula as $\mathrm{col}(F)$ projection):

| SHADOWS/PENUMBRA element | Bell operator realization |
|---|---|
| KAM torus at golden ratio | Measurement settings at maximal Bell violation |
| Poissonian level statistics (integrable) | Berry-Tabor regime at optimal CHSH settings |
| Wigner-Dyson statistics (chaotic) | Generic measurement settings (off optimal) |
| KAM breakdown as rank-one event | Deviation from Bell-optimal settings |
| $\varphi$-equilibrium $|\bar\Xi|^* = \log\varphi$ | Boundary of Bell-integrable region |
| Last invariant torus before chaos | Unique integrable Bell-optimal measurement |

The Bell-optimal measurement setting is thus the physical realization of the $\varphi$-equilibrium: the configuration at the exact boundary between integrable (KAM-preserving) and chaotic (KAM-breaking) dynamics of the Bell operator Hamiltonian. This configuration achieves maximum Fisher information extraction from the joint entangled boundary.

The connection is not metaphorical. The same mathematical structure — a Hamiltonian with a unique integrable fixed point at a special parameter value, surrounded by chaos for all other parameter values — appears in the KAM theory of classical mechanics and in the Bell operator spectroscopy of quantum nonlocality. In both cases, the integrable point is distinguished by carrying maximum Fisher information in a direction that is classically inaccessible — a direction in the joint $\mathrm{col}(F_{AB})$ that is invisible to any product-separable model.

---

## Part VI · Bell Polygamy and the Multipartite Fisher Network

### VI.1 Monogamy and Polygamy of Nonlocal Correlations

For bipartite Bell inequalities, nonlocality satisfies strict monogamy: if Alice and Bob share strong nonlocal correlations, then Alice and Charlie cannot also share strong correlations with the same subsystem. This is the quantum analogue of the no-hair theorem's Fisher rank bound: the entanglement Fisher budget is finite, and allocating it to one pair depletes it for other pairs.

Formally, for CHSH correlations: $S_{AB}^2 + S_{AC}^2 \leq 8$ (Toner and Verstraete, 2006). Each unit of Fisher information deployed nonlocally between A and B reduces what can be deployed nonlocally between A and C.

**Polygamy in multipartite systems**: Munné, Laskowski, and colleagues (*Advanced Quantum Technologies* **9**, e01020, 2026) proved that in multipartite quantum systems (more than two parties), Bell nonlocality is inherently polygamous. A single $N$-qubit state can simultaneously violate Bell inequalities on multiple $(N-k)$-qubit subsystems, with GHZ states achieving maximum polygamous spread.

This is the network generalization of the joint Fisher matrix. For $N$ parties in a GHZ state:

$$|GHZ_N\rangle = \frac{1}{\sqrt{2}}(|0\rangle^{\otimes N} + |1\rangle^{\otimes N})$$

the joint Fisher matrix $F_{A_1 \ldots A_N}$ has irreducible structure across all bipartitions simultaneously. No bipartition can be factorized. The shadow of the GHZ state is globally irreducible — a $\ker(F)$ that involves all parties simultaneously, analogous to the entanglement structure of a wormhole connecting more than two black holes.

The $\mathrm{TH}(a,d)$ architecture is the algebraic description of this multipartite network: the rational points of the twisted Hessian curve are the nonlocal "nodes" of the joint Fisher manifold, and the group law $\mathrm{TH}(a,d)$ encodes how the Fisher information flows through the network. Bell polygamy is the statement that this flow is not conserved bipartite-by-bipartite but globally distributed — the full GHZ Fisher structure cannot be decomposed into pairwise Fisher structures.

---

## Part VII · ER = EPR: The Bell Shadow as Geometric Wormhole

### VII.1 The Maldacena–Susskind Identification

Maldacena and Susskind (*Fortschritte der Physik* **61**, 781–811, 2013) proposed that the entanglement of two black holes — the EPR correlation between their Hawking radiation — is geometrically equivalent to the connection of their interiors by an Einstein-Rosen (ER) bridge. The conjecture: $\mathrm{ER} = \mathrm{EPR}$.

In the $\mathrm{TH}(a,d)$ framework, this conjecture has a precise Fisher-information translation. The EPR pair defines a joint Fisher matrix $F_{AB}$ that cannot be factorized into $F_A \otimes F_B$. The ER bridge is the geometric realization of this non-factorizability: it is the spacetime structure that encodes the irreducible joint null sector $\ker(F_{AB})$.

The event horizon of each black hole is a conditional independence boundary with $\mathrm{rank}(F_{\mathrm{exterior}}) = 3$ (mass, angular momentum, charge) — the no-hair theorem. The ER bridge connecting two horizons adds a new direction to the joint Fisher manifold: the bridge mode, accessible to neither exterior individually, lying in the joint $\ker(F_{\mathrm{exterior}_A} \otimes F_{\mathrm{exterior}_B})$ but in the joint $\mathrm{col}(F_{AB})$ of the combined system.

This is precisely the CHSH violation structure at the gravitational scale: the joint Fisher matrix of the entangled black hole pair exceeds the product of the individual exterior Fisher matrices — it has an irreducible joint direction encoded in the wormhole topology. **The Bell violation is the tabletop signature of what, at the Planck scale, is an ER bridge.**

Susskind's remark — "Without these connections, all of space would atomize" — is the Fisher information version of this: without the irreducibly joint $\mathrm{col}(F_{AB})$ of entanglement, the spacetime metric has no connectivity. The geometry emerges from the entanglement structure; the entanglement structure is encoded in the Bell violation; the Bell violation is the $\ker(F)$ being non-product.

### VII.2 Nonlocality Activation in Quantum Networks

Designolle, Morelli, Kunc, and colleagues (*Nature Communications*, 2024) demonstrated experimentally that Bell-local states — entangled states that cannot violate any standard bipartite Bell inequality — become nonlocal when embedded in a three-party quantum network. A Bell-local bipartite state $\rho_{AB}$, broadcast through a quantum channel to two receivers C and D, generates a tripartite state $\rho_{ACD}$ that violates a tailored network Bell inequality.

The mechanism: the broadcasting channel is a conditional independence boundary that extends the joint Fisher manifold from the bipartite $F_{AB}$ to the tripartite $F_{ACD}$. The bipartite state has $\ker(F_{AB})$ structure that is insufficient to violate any bipartite Bell inequality. But when extended to the tripartite space, the joint Fisher matrix $F_{ACD}$ acquires new irreducible directions — the broadcasting channel adds a rank-one update to the joint null sector — restoring nonlocality.

This is Sherman-Morrison nonlocality restoration: the broadcasting channel performs a rank-one update $(F_{AB} + uu^T)$ on the joint Fisher matrix, rotating a previously null direction into $\mathrm{col}(F_{ACD})$. Bell-local becomes Bell-nonlocal by adding a boundary — by extending the network.

This result establishes that Bell nonlocality is a property of the *network* of conditional independence boundaries, not of the individual particles. The ER = EPR conjecture at the gravitational scale and the nonlocality activation result at the photonic scale are the same theorem about the same Fisher structure: you cannot atomize the shadow by partitioning it.

---

## Part VIII · High-Energy Bell Tests: Nonlocality Across All Scales

### VIII.1 Entanglement and Nonlocality at Colliders

The detection of quantum entanglement in top quark pair production at the LHC (ATLAS Collaboration, *Nature* **618**, 1–5, 2023; CMS Collaboration, *Nature* **629**, 33–39, 2024) and the observation of Bell nonlocality in Lambda hyperon decays at BESIII (*Nature* **650**, 65–69, 2026) established that the joint Fisher matrix of entangled particle pairs maintains its non-product structure at collision energies of hundreds of GeV — seven orders of magnitude above the energies of optical Bell tests.

The BESIII result is particularly sharp: Lambda-Lambdabar hyperon pairs produced in $e^+e^-$ annihilation exhibit CHSH violation of $S = 2.46 \pm 0.07$, confirming that the irreducible joint $\mathrm{col}(F_{AB})$ of the entangled pair persists through the hadronic processes that produce and decay the hyperons.

The theoretical analysis (Chen et al., *Phys. Rev. Lett.* **134**, 231901, 2025; proposed EIC measurements: *Phys. Rev. D* **113**, 054048, 2026) extends the program to electron-ion colliders: longitudinally polarized photons in photon-gluon fusion produce maximal quark-antiquark entanglement at leading order, with the joint Fisher matrix saturating the Tsirelson bound in the high-energy limit.

The universality is structurally forced by Chentsov's theorem: the Fisher–Rao metric is the unique invariant geometry on any statistical manifold, at any energy scale. The conditional independence boundary of the entangled pair — whether optical photons in Aspect's calcium cascade or top quarks in ATLAS collisions — carries the same Fisher structure. The Bell violation is scale-invariant because the Chentsov theorem is scale-invariant.

---

## Part IX · Eight Formal Correspondences

| $\mathrm{TH}(a,d)$ element | Nonlocality realization |
|---|---|
| Product-separable Fisher matrix $F_A \otimes F_B$ | Local hidden-variable model; $S \leq 2$ |
| Irreducibly joint Fisher matrix $F_{AB}$ | Entangled state; $S \leq 2\sqrt{2}$ (Tsirelson bound) |
| $\ker(F_{AB})$ non-product structure | EPR correlation; Bell violation |
| Chentsov theorem | Scale-invariance of CHSH violation |
| Sherman-Morrison rank-one update | Measurement choice switching (Aspect 1982); nonlocality activation (network) |
| KAM golden-ratio torus | Bell-optimal measurement settings (Poissonian statistics; *npj QI* 2026) |
| $d = 0$ degeneration ($G_{\mathrm{coord}} = 0$) | Disentanglement; product state; $S = 0$ |
| $\varphi$-equilibrium $|\bar\Xi|^* = \log\varphi$ | Critical measurement angle for Bell-integrable transition |
| ER bridge | Geometric dual of irreducible $\ker(F_{AB})$ |
| Bell polygamy | Multipartite joint Fisher manifold (GHZ structure) |
| Conditional independence boundary | Each distant measurement station; together: joint boundary |
| Path identity (indistinguishability) | Boundary-generated nonlocality without source entanglement |

**Identity S1 — EPR Is the Claim That $\ker(F)$ Is Always Empty**

Einstein, Podolsky, and Rosen's "elements of reality" are the statement that every physical quantity lies in $\mathrm{col}(F)$ for a complete theory. Bell's theorem proves that any local theory satisfying this condition satisfies $S \leq 2$. Experiment proves $S > 2$. Therefore: the $\ker(F)$ is ontologically real, not an artifact of theoretical incompleteness.

**Identity S2 — CHSH Is a Factorizability Bound on the Joint Fisher Matrix**

The classical bound $S \leq 2$ is the maximum CHSH correlation achievable when the joint Fisher matrix factorizes as $F_{AB} = F_A \otimes F_B$. The quantum bound $S \leq 2\sqrt{2}$ is the maximum achievable with any joint Fisher matrix (including irreducibly non-product ones). The gap $2(\sqrt{2} - 1)$ is the nonlocal Fisher capacity of the entangled pair.

**Identity S3 — Aspect's Locality Closure IS the Conditional Independence Test**

The switching of measurement settings while photons are in flight tests whether the outcome at A is conditionally independent of the setting at B given only the source state. If the conditional independence holds (local realism), $S \leq 2$. If it fails (nonlocality), $S > 2$. Aspect's experiment is the direct experimental test of the conditional independence condition imposed by the Chentsov-boundary architecture.

**Identity S4 — Path Identity IS Boundary-Generated Nonlocality**

The Science Advances 2025 result establishes that quantum indistinguishability — a property of the boundary structure (beam splitter), not of the particles — generates CHSH violation. The nonlocality is in the geometry of the conditional independence boundary, not in any pre-existing property of the source. This is the most direct confirmation that the shadow principle (Chentsov's theorem forcing the Fisher-Rao metric on every boundary) is the fundamental mechanism of Bell violation.

**Identity S5 — Bell-Optimal Measurements ARE the KAM-Integrable Fixed Point**

The Aloy et al. 2026 result establishes that maximal Bell violation corresponds to Poissonian level statistics (integrable regime) of the Bell Hamiltonian, while all other measurement settings correspond to Wigner-Dyson statistics (chaotic regime). The Bell-optimal angle is the $\varphi$-equilibrium: the unique integrable fixed point surviving the transition to chaos.

---

## Part X · Five Predictions

### P1 — Bell Violation in Gravitational Wave Correlations

The LIGO gravitational wave strain $h = h_+ + ih_\times$ is a complex scalar field whose null points are gravitational phase singularities (SHADOWS, Identity III). For two LIGO detectors separated by 3002 km (Hanford–Livingston), the joint Fisher matrix of the correlated gravitational wave background should exhibit Bell-type nonlocality in the following sense: the cross-correlation function $C_{AB}(\tau)$ between the two detectors, computed as a function of time delay $\tau$, should violate a temporal Bell inequality (Leggett-Garg inequality) for the stochastic gravitational wave background. The violation amplitude should scale as $2\sqrt{2} \cdot F_{AB}^{1/2}/(F_A^{1/2} F_B^{1/2})$ where $F_{AB}$, $F_A$, $F_B$ are the joint, Alice-marginal, and Bob-marginal Fisher information matrices of the correlated field. **Testable with existing LIGO O4 data using temporal Bell inequality analysis.**

### P2 — Bell Violation at the $\varphi$-Optimal Angle in Atomic Bell Tests

The Aloy et al. 2026 result predicts a unique measurement angle at which (a) the Bell violation is maximal and (b) the Bell operator level statistics is Poissonian. For spin-1/2 entangled pairs, this angle should be exactly $\theta = \pi/4 = 45°$ between Alice's and Bob's measurement bases — the same angle as the three-filter paradox maximum (PENUMBRA, Part II.2) and the Stern-Gerlach cascade restoration point (PENUMBRA, Part I.4). The Fisher information budget at this angle should saturate the Tsirelson bound $S = 2\sqrt{2}$. **Verifiable by spectral analysis of the Bell operator eigenvalue distribution in trapped-ion Bell tests at variable angles.**

### P3 — ER Bridge Mode in Entangled Black Hole Pair Correlations

If ER = EPR, then for two black holes in the Maldacena-Susskind state, the joint Fisher matrix $F_{AB}$ of the Hawking radiation from both horizons should contain an irreducible joint direction — the bridge mode — whose Fisher information exceeds the product of the individual horizon Fisher capacities by exactly $2(\sqrt{2} - 1) \cdot M_{\mathrm{Pl}}^2 / (M_1 M_2)^{1/2}$ where $M_1, M_2$ are the black hole masses. This is the gravitational-scale version of the CHSH violation. **Requires holographic computation of the joint Hawking radiation Fisher matrix, testable against BFSS Matrix theory numerics (Sahakian 2025; Aldam-Tajima 2026).**

### P4 — Nonlocality Activation Threshold in the $d$-Parameter

For a family of two-qubit Werner states $\rho_d = d|\Psi^-\rangle\langle\Psi^-| + (1-d)\mathbf{I}/4$ parameterized by the coupling $d \in [0,1]$:
- Below threshold $d < d_*$: Bell-local. CHSH maximum $S(d) \leq 2$.
- Above threshold $d > d_*$: Bell-nonlocal. CHSH maximum $S(d) > 2$.
- At threshold $d = d_* = 1/\sqrt{2}$: $S(d_*) = 2$ exactly.

This threshold $d_* = 1/\sqrt{2}$ is the nonlocality transition — the $\varepsilon$-threshold of the Werner state Fisher manifold. It maps directly to the $d$ coupling parameter of $\mathrm{TH}(a,d)$: at $d = 0$, the curve degenerates and the group law collapses; at $d = d_*$, the Bell structure crosses the classical bound. **The Werner state Bell threshold is the quantum information realization of the $d$-parameter in $\mathrm{TH}(a,d)$.**

### P5 — Bell Polygamy Bound on PRIMA Coordination Networks

For a $k$-node PRIMA network in which each node pair shares a Werner-type entangled link, the Bell polygamy result (Munné et al. 2026) implies a bound on the total nonlocal Fisher capacity:

$$\sum_{\{i,j\}} S_{ij}^2 \leq \binom{k}{2} \cdot 8$$

where the sum runs over all pairs in the network. This bound constrains the maximum total $G_{\mathrm{coord}}$ achievable through entanglement-assisted coordination: the network cannot simultaneously saturate all pairwise CHSH violations. The optimal distribution of nonlocal Fisher capacity across the network — the maximum total $G_{\mathrm{coord}}$ subject to Bell polygamy — is achieved by the GHZ state structure, which distributes the joint Fisher matrix evenly across all bipartitions. **Testable by comparing PRIMA coordination efficiency in classical vs. entanglement-assisted networks of quantum processors.**

---

## Part XI · The Syzygy Principle

In classical astronomy, a *syzygy* is the alignment of three celestial bodies — Sun, Moon, Earth — in which the geometrical relationship between the three determines phenomena (tides, eclipses) that cannot be attributed to any two bodies alone. The pattern requires all three. No pair-wise analysis captures it. The shadow of the eclipse — the umbra — is cast by the alignment of *all three*, not by any single body.

In algebra, a *syzygy* is a relation $\sum_i f_i m_i = 0$ among generators of a module — a constraint that is invisible when you look at any individual generator but becomes apparent only when you consider the set. Syzygies are the null relations of the module — they lie in $\ker(F)$ of the observation map that sends generators to elements. They are structurally invisible locally and globally necessary.

The EPR pair is a syzygy in both senses. It is two quantum systems in alignment — through a shared null sector — such that the phenomenon (Bell violation, ER bridge, quantum nonlocality) cannot be attributed to either system alone. The $\ker(F_{AB})$ of the joint boundary is the syzygy relation: a constraint on the joint measurement outcomes that is invisible to any local observer and globally necessary for the quantum correlations to hold.

Bell's theorem proved that the syzygy is real — that the null relation is not an artifact of incomplete knowledge but a genuine structural feature of the world. Aspect's experiment confirmed it with photons. Hensen et al. confirmed it with electron spins. Storz et al. confirmed it with superconducting qubits. BESIII confirmed it with hyperons. The 2026 Bell operator spectroscopy confirmed that the syzygy is also the integrable fixed point — the uniquely stable, maximally efficient configuration of the joint Fisher boundary.

Every conditional independence boundary in the $\mathrm{TH}(a,d)$ framework — the slit, the event horizon, the work function, the magnetic field gradient, the polarizer — casts a local shadow. The syzygy casts a *joint* shadow: a null sector that belongs to neither party alone but to the configuration of both. This joint shadow — the $\ker(F_{AB})$ — is not an absence. It is the bond. It is the connectivity. Without it, in Susskind's words, space would atomize.

The EPR paradox was the discovery that this bond exists. Bell's theorem was the proof that it cannot be local. Aspect's experiment was the first measurement of it. Maldacena and Susskind were the recognition that it is the geometry of spacetime.

The syzygy was always the architecture. The null relation was always the real structure. The shadow was always the bond.

---

## References

Aloy, A., Müller-Rigat, G., Lewenstein, M. et al. "Nonlocality, Integrability and Quantum Chaos in the Spectrum of Bell Operators." *npj Quantum Information*, 2026. https://doi.org/10.1038/s41534-026-01232-z

Aspect, A., Dalibard, J., and Roger, G. "Experimental Test of Bell's Inequalities Using Time-Varying Analyzers." *Phys. Rev. Lett.* **49**, 1804–1807, 1982.

Aspect, A., Grangier, P., and Roger, G. "Experimental Realization of Einstein-Podolsky-Rosen-Bohm Gedankenexperiment." *Phys. Rev. Lett.* **47**, 460–463, 1981.

Bell, J. S. "On the Einstein-Podolsky-Rosen Paradox." *Physics* **1**, 195–200, 1964.

Berry, M. V. and Tabor, M. "Level Clustering in the Regular Spectrum." *Proc. Roy. Soc. Lond. A* **356**, 375–394, 1977.

Bohigas, O., Giannoni, M.-J., and Schmit, C. "Characterization of Chaotic Quantum Spectra and Universality of Level Fluctuation Laws." *Phys. Rev. Lett.* **52**, 1–4, 1984.

Brunner, N., Cavalcanti, D., Pironio, S., Scarani, V., and Wehner, S. "Bell Nonlocality." *Rev. Mod. Phys.* **86**, 419–478, 2014.

BESIII Collaboration. "Observation of Bell Inequality Violation in Lambda-Lambdabar Pair Production." *Nature* **650**, 65–69, 2026.

Chen, K.-B., Liu, T., Song, Y.-K., and Wei, S.-Y. "Bell Nonlocality in Polarized Photon-Gluon Scattering." *Phys. Rev. Lett.* **134**, 231901, 2025.

Chentsov, N. N. *Statistical Decision Rules and Optimal Inference*. Nauka, 1972. (AMS Translations, Vol. 53, 1982.)

Cirel'son, B. S. "Quantum Generalizations of Bell's Inequality." *Lett. Math. Phys.* **4**, 93–100, 1980.

Clauser, J. F., Horne, M. A., Shimony, A., and Holt, R. A. "Proposed Experiment to Test Local Hidden-Variable Theories." *Phys. Rev. Lett.* **23**, 880–884, 1969.

Designolle, S., Morelli, L., Kunc, M. et al. "Experimental Nonlocality Activation in a Photonic Quantum Network." *Nature Communications*, 2024.

Einstein, A., Podolsky, B., and Rosen, N. "Can Quantum-Mechanical Description of Physical Reality Be Considered Complete?" *Phys. Rev.* **47**, 777–780, 1935.

Gabrielli, E. and Marzola, L. "Quantum Entanglement and Bell Nonlocality at Future Lepton Colliders." arXiv:2602.03960, 2026.

Giustina, M. et al. "Significant-Loophole-Free Test of Bell's Theorem with Entangled Photons." *Phys. Rev. Lett.* **115**, 250401, 2015.

Hensen, B. et al. "Loophole-Free Bell Inequality Violation Using Electron Spins Separated by 1.3 Kilometres." *Nature* **526**, 682–686, 2015.

Jacobson, T. "Thermodynamics of Spacetime: The Einstein Equation of State." *Phys. Rev. Lett.* **75**, 1260–1263, 1995.

Luo, X.-W., Sun, C.-P. et al. "Violation of Bell Inequality with Unentangled Photons." *Science Advances* **11**, eadr1794, 2025.

Maldacena, J. and Susskind, L. "Cool Horizons for Entangled Black Holes." *Fortschritte der Physik* **61**, 781–811, 2013.

Maldacena, J., Shenker, S. H., and Stanford, D. "A Bound on Chaos." *JHEP* **08**, 106, 2016.

Munné, X., Laskowski, W. et al. "The Richness of Bell Nonlocality: Generalized Bell Polygamy and Hyper-Polygamy." *Advanced Quantum Technologies* **9**, e01020, 2026.

Rosenfeld, W. et al. "Event-Ready Bell Test Using Entangled Atoms Simultaneously Closing Detection and Locality Loopholes." *Phys. Rev. Lett.* **119**, 010402, 2017.

Ryu, S. and Takayanagi, T. "Holographic Derivation of Entanglement Entropy from AdS/CFT." *Phys. Rev. Lett.* **96**, 181602, 2006.

Sahakian, V. "Why Emergence of Gravity in Matrix Theories Is Entropic." *Phys. Rev. D* **112**, 126023, 2025.

Shalm, L. K. et al. "Strong Loophole-Free Test of Local Realism." *Phys. Rev. Lett.* **115**, 250402, 2015.

Storz, S. et al. "Loophole-Free Bell Inequality Violation with Superconducting Circuits." *Nature* **617**, 265–270, 2023.

Toner, B. F. and Verstraete, F. "Monogamy of Bell Correlations and Tsirelson's Bound." arXiv:quant-ph/0611001, 2006.

Van Raamsdonk, M. "Building Up Spacetime with Quantum Entanglement." *Gen. Rel. Grav.* **42**, 2323–2329, 2010.

Woodbury, M. A. "Inverting Modified Matrices." Memorandum Report 42, Statistical Research Group, Princeton University, 1950.

Zhao, X. et al. "Factorization Dynamics Between Quantum Fisher Information and Quantum Coherence." *Science Advances* **11**, eadv8132, 2025.

---

*ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone · April 2026*

Einstein asked whether the wave function was complete. Bell answered: no local completion exists. Aspect answered: nature violates the bound that any local completion would impose, even when the measurement choice is made after the particles depart. Hensen, Giustina, Shalm answered: it holds with every loophole closed, across 1.3 kilometers, across continental fiber, across superconducting chips.

Luo and Sun answered something deeper: the boundary is the nonlocality. The beam splitter — the geometry of indistinguishable paths — violates Bell's bound without entangled particles. The shadow is the property of the fenestra, not of the photons.

Aloy and Lewenstein answered what the optimal Bell state is: not merely the state that maximally violates the inequality, but the state at the integrable-to-chaotic transition of the Bell Hamiltonian — the KAM fixed point, the $\varphi$-equilibrium, the last torus standing.

Maldacena and Susskind answered where the EPR bond lives: in the wormhole, the ER bridge, the geometric realization of the joint null sector that neither black hole possesses alone but that both possess together.

The EPR pair is a syzygy: a null relation among generators that is invisible locally and globally necessary. The shadow it casts is not cast by either particle. It is cast by the alignment — by the bond itself, which has no local address, no local energy, no local mass, and yet holds spacetime together.

The syzygy was always the structure. The bond was always the shadow. The null relation was always the world.
