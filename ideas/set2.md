# Curated Topic Bank — Volume 2

---

## Number Theory & Cryptography

1. **Fermat’s Little Theorem** — If p is prime and a is not divisible by p, then a^(p−1) ≡ 1 (mod p). The backbone of RSA and modular exponentiation.

2. **Euler’s Totient Function φ(n)** — Counts integers up to n that are coprime to n. The animation shows which numbers survive a sieve relative to n.

3. **Chinese Remainder Theorem** — A system of congruences with coprime moduli has a unique solution modulo their product. Visualized as intersecting clock faces.

4. **Quadratic Reciprocity** — A deep symmetry governing when one prime is a square modulo another. One of Gauss’s favorite theorems.

5. **Prime Number Theorem** — The number of primes below x grows like x / ln x. The animation compares the step function π(x) with the smooth approximation.

6. **Goldbach’s Conjecture** — Every even number greater than 2 is the sum of two primes. Still unproven; the animation shows decompositions for many even numbers.

7. **Twin Primes** — Pairs like (3,5), (11,13), (41,43). Whether infinitely many exist is still open.

8. **Perfect Numbers and Mersenne Primes** — 6, 28, 496, 8128. Each corresponds to a Mersenne prime via Euclid–Euler.

9. **Continued Fractions** — Every real number has a unique continued fraction expansion. Rationals terminate; quadratic irrationals repeat.

10. **Diophantine Equations** — Integer solutions to polynomial equations. Fermat’s Last Theorem is the most famous example.

11. **Modular Arithmetic Clocks** — Addition and multiplication wrap around a circle. The animation shows arithmetic mod n on a clock face.

12. **RSA Encryption** — Public key = (n, e); private key = (n, d). The animation shows message → ciphertext → message using modular exponentiation.

13. **Diffie–Hellman Key Exchange** — Two parties agree on a shared secret over a public channel using modular exponentiation.

14. **Elliptic Curve Cryptography** — Points on a curve form a group under a geometric addition law. The animation shows point doubling and addition.

15. **Zero-Knowledge Proofs** — Prove you know a secret without revealing it. The cave analogy is the classic visual.

16. **Hash Functions and Avalanche Effect** — A one-bit change in the input flips about half the output bits. Visualized as a bit-grid diff.

---

## Geometry & Topology

17. **Non-Euclidean Geometry** — On a sphere, triangle angles sum to more than 180°; on a saddle, less. The animation shows the same triangle on three surfaces.

18. **Poincaré Disk** — A model of hyperbolic geometry where straight lines are arcs. Parallel lines diverge; triangles have angle sum < 180°.

19. **Möbius Strip** — A surface with one side and one edge. Cutting it down the middle produces one longer loop, not two.

20. **Klein Bottle** — A non-orientable surface with no inside or outside. Cannot be embedded in 3D without self-intersection.

21. **Euler Characteristic** — V − E + F is invariant under continuous deformation. The animation morphs a cube into a sphere and a torus.

22. **Genus of a Surface** — The number of holes. A sphere has genus 0; a torus has genus 1. The animation adds handles one by one.

23. **Gauss–Bonnet Theorem** — Total curvature of a closed surface equals 2π times its Euler characteristic.

24. **Geodesics** — The shortest path between two points on a curved surface. On a sphere, they are great-circle arcs.

25. **Fractal Dimension** — The Koch snowflake has dimension log 4 / log 3 ≈ 1.26. The animation builds iterations and measures the dimension.

26. **Sierpinski Triangle** — A self-similar fractal with area zero but infinite perimeter. Built by removing the middle triangle repeatedly.

27. **Mandelbrot Set** — The set of complex c for which z → z² + c stays bounded. The boundary is infinitely intricate.

28. **Julia Sets** — For a fixed c, the set of z whose orbit under z² + c stays bounded. Each c gives a different fractal.

29. **Space-Filling Curves** — Hilbert and Peano curves visit every point in a square. The animation shows successive refinements.

30. **Jordan Curve Theorem** — Any simple closed curve divides the plane into inside and outside. Trivial to state, surprisingly hard to prove.

31. **Borsuk–Ulam Theorem** — On any continuous function from a sphere to the plane, there exist antipodal points with the same value. Implies “there are always two antipodal points on Earth with the same temperature and pressure.”

32. **Hairy Ball Theorem** — You cannot comb a hairy sphere flat without a cowlick. Any continuous tangent vector field on a sphere has a zero.

33. **Fixed Point Theorems** — Brouwer: any continuous map from a disk to itself has a fixed point. Visualized as a crumpled map of a city always having a point above its true location.

---

## Graph Theory & Combinatorics

34. **Euler’s Königsberg Bridge Problem** — Can you walk every bridge exactly once? The answer is no; the graph has odd-degree vertices.

35. **Hamiltonian Cycles** — A path visiting every vertex exactly once. The traveling salesman problem asks for the shortest such cycle.

36. **Four Color Theorem** — Any planar map can be colored with four colors so no two adjacent regions share a color.

37. **Ramsey Theory** — In any sufficiently large structure, order must appear. R(3,3)=6: any 6 people contain a triangle of friends or strangers.

38. **Pigeonhole Principle** — If n+1 pigeons occupy n holes, one hole has at least two pigeons. Simple but powerful.

39. **Inclusion–Exclusion Principle** — Count unions by adding individual sets, subtracting pairwise intersections, adding triple intersections, and so on.

40. **Catalan Numbers** — 1, 1, 2, 5, 14, 42, … count balanced parentheses, binary trees, and polygon triangulations.

41. **Fibonacci Numbers and the Golden Ratio** — F(n+1)/F(n) → φ. The animation shows squares spiraling into a golden rectangle.

42. **Pascal’s Triangle** — Binomial coefficients arranged in a triangle. Row sums are powers of 2; diagonals give Fibonacci numbers.

43. **Stirling Numbers** — Count ways to partition a set into k non-empty subsets. The animation shows set partitions growing.

44. **Partition Numbers** — The number of ways to write n as a sum of positive integers. p(100) = 190,569,292.

45. **Derangements** — Permutations with no element in its original position. The probability approaches 1/e.

46. **Matching and Hall’s Theorem** — A bipartite graph has a perfect matching iff every subset of one side has enough neighbors.

47. **Menger’s Theorem** — The maximum number of disjoint paths between two vertices equals the minimum vertex cut.

48. **Planar Graphs and Kuratowski’s Theorem** — A graph is planar iff it contains no subdivision of K₅ or K₃,₃.

49. **Graph Coloring and Chromatic Number** — The minimum colors needed so adjacent vertices differ. The animation colors a graph step by step.

50. **Network Flow and Max-Flow Min-Cut** — The maximum flow from source to sink equals the minimum cut capacity.

---

## Logic, Sets & Foundations

51. **Russell’s Paradox** — The set of all sets that do not contain themselves. Does it contain itself? Both answers lead to contradiction.

52. **Gödel’s Incompleteness Theorems** — Any consistent formal system strong enough for arithmetic contains true statements it cannot prove.

53. **Turing’s Halting Problem** — No algorithm can decide, for every program and input, whether the program halts. Proof by diagonalization.

54. **Cantor’s Theorem** — The power set of any set has strictly larger cardinality than the set itself.

55. **Cardinality of the Continuum** — The real numbers are uncountable. The diagonal argument shows no list can contain them all.

56. **Continuum Hypothesis** — Is there a cardinality between the naturals and the reals? Independent of ZFC.

57. **Axiom of Choice** — Every collection of non-empty sets has a choice function. Equivalent to Zorn’s Lemma and the well-ordering theorem.

58. **Zorn’s Lemma** — Every partially ordered set in which every chain has an upper bound has a maximal element.

59. **Boolean Algebra** — A algebraic structure with AND, OR, NOT. Duality: swap AND/OR and 0/1 to get a valid dual statement.

60. **Propositional and Predicate Logic** — Truth tables for propositional; quantifiers and variables for predicate. The animation shows satisfiability.

---

## Game Theory & Decision Theory

61. **Nash Equilibrium** — A set of strategies where no player benefits by unilaterally deviating. The animation shows best-response curves intersecting.

62. **Prisoner’s Dilemma** — Two rational players defect even though mutual cooperation would be better. The payoff matrix tells the story.

63. **Zero-Sum Games and Minimax** — One player’s gain is the other’s loss. The optimal strategy minimizes the maximum loss.

64. **Mixed Strategies** — Randomizing over actions can be optimal. Rock-paper-scissors has a mixed equilibrium at (1/3, 1/3, 1/3).

65. **Ultimatum Game** — One player proposes a split; the other accepts or rejects. Rationality predicts low offers, but humans reject unfair ones.

66. **Auction Theory** — First-price, second-price, English, Dutch. The revenue equivalence theorem links them under certain assumptions.

67. **Mechanism Design** — Design rules so self-interested agents produce a desired outcome. The Vickrey–Clarke–Groves mechanism is incentive-compatible.

68. **Arrow’s Impossibility Theorem** — No ranked voting system can satisfy a small set of fair axioms simultaneously.

69. **Braess’s Paradox** — Adding a road to a network can increase everyone’s travel time. The animation shows traffic redistributing.

70. **Tragedy of the Commons** — Individuals overuse a shared resource even when it harms everyone. Visualized as a pasture with too many cows.

---

## Complex Analysis & Special Functions

71. **Complex Numbers as Rotations** — Multiplication by i rotates 90°. The animation shows points on the complex plane rotating.

72. **Conformal Maps** — Angle-preserving transformations. The animation shows a grid being warped by z², e^z, and 1/z.

73. **Cauchy–Riemann Equations** — Conditions for a complex function to be differentiable. The animation shows the Jacobian as a rotation-scaling matrix.

74. **Residue Theorem** — A contour integral equals 2πi times the sum of residues inside. Used to evaluate real integrals.

75. **Laurent Series** — A complex function expanded around a singularity. The principal part determines the residue.

76. **Riemann Zeta Function** — ζ(s) = Σ 1/n^s. The animation shows the critical strip and the Riemann hypothesis.

77. **Gamma Function** — Γ(n) = (n−1)!. Extends the factorial to complex numbers. The animation shows Γ(x) on the real line.

78. **Bessel Functions** — Solutions to Bessel’s equation. They appear in vibrating circular membranes and heat conduction in cylinders.

79. **Legendre Polynomials** — Orthogonal polynomials on [−1, 1]. They solve Laplace’s equation in spherical coordinates.

80. **Hermite and Laguerre Polynomials** — Solutions to the quantum harmonic oscillator and hydrogen atom.

---

## Dynamical Systems, Chaos & Complexity

81. **Lorenz Attractor** — A butterfly-shaped strange attractor from three coupled ODEs. Sensitive dependence on initial conditions.

82. **Double Pendulum** — A simple mechanical system with chaotic motion. Two nearby starts diverge rapidly.

83. **Poincaré Section** — Slice a continuous trajectory to reveal its underlying structure. Chaos appears as a fractal set of points.

84. **Lyapunov Exponent** — Measures the rate of divergence of nearby trajectories. Positive exponent means chaos.

85. **Feigenbaum Constants** — Universal numbers governing period-doubling. δ ≈ 4.669, α ≈ 2.502.

86. **Strange Attractors** — Rössler, Hénon, and Lorenz attractors. Fractal geometry with fractional dimension.

87. **Self-Organized Criticality** — Sandpile models and earthquakes. Systems naturally evolve toward a critical state.

88. **Cellular Automata** — Rule 110, Rule 90, and Wolfram’s classification. Simple rules produce complex behavior.

89. **Fractal Growth: DLA** — Diffusion-limited aggregation produces dendritic clusters. The animation shows particles sticking one by one.

90. **Reaction–Diffusion Systems** — Turing patterns: spots and stripes emerge from two diffusing chemicals.

91. **Synchronization** — Coupled oscillators lock in phase. The Kuramoto model shows the transition to sync as coupling increases.

92. **Flocking: Boids** — Three rules (separation, alignment, cohesion) produce realistic bird flocks.

93. **Swarm Intelligence** — Ant colony optimization and particle swarm optimization. Simple agents solve hard problems collectively.

94. **Power Laws and Scale-Free Networks** — A few nodes have many connections; most have few. Preferential attachment generates these networks.

95. **Small-World Networks** — Watts–Strogatz model: high clustering and short path lengths. Six degrees of separation.

---

## Numerical Methods & Scientific Computing

96. **Newton’s Method** — Iteratively find roots via tangent lines. The animation shows convergence and occasional divergence.

97. **Bisection Method** — Repeatedly halve an interval containing a root. Slow but guaranteed to converge.

98. **Secant Method** — Approximate the derivative with a secant line. Faster than bisection, no derivative needed.

99. **Fixed-Point Iteration** — Solve x = g(x) by iterating. Converges if |g′(x)| < 1 near the fixed point.

100. **Euler’s Method for ODEs** — Step forward using the derivative. The animation shows error accumulating with step size.

101. **Runge–Kutta Methods** — RK4 is the workhorse of ODE integration. Fourth-order accuracy at modest cost.

102. **Finite Difference Method** — Discretize derivatives on a grid. The animation shows a heat equation evolving.

103. **Finite Volume Method** — Conserve quantities over control volumes. Used in fluid dynamics and heat transfer.

104. **Monte Carlo Integration** — Estimate integrals by random sampling. Error scales as 1/√N, independent of dimension.

105. **Simulated Annealing** — Escape local minima by accepting worse solutions with decreasing probability.

106. **Genetic Algorithms** — Evolve a population of solutions via selection, crossover, and mutation.

107. **Conjugate Gradient Method** — Solve large sparse linear systems iteratively. Used in optimization and PDE solvers.

108. **Fast Fourier Transform** — Compute the DFT in O(N log N) instead of O(N²). The Cooley–Tukey algorithm is the classic.

109. **Singular Value Decomposition** — Factor any matrix into rotation, scaling, and rotation. The animation shows the unit circle mapping to an ellipse.

110. **QR Decomposition and Least Squares** — Orthogonalize columns to solve overdetermined systems stably.

---

## Machine Learning Theory

111. **Bias–Variance Tradeoff** — High bias underfits; high variance overfits. The animation shows model complexity versus error.

112. **Regularization: L1 vs L2** — L1 promotes sparsity; L2 shrinks weights smoothly. The geometry of the constraint region explains why.

113. **Support Vector Machines** — Find the maximum-margin hyperplane. The animation shows the margin and support vectors.

114. **Kernel Trick** — Map data to a higher-dimensional space implicitly. The animation shows a circle becoming linearly separable.

115. **Principal Component Analysis** — Project data onto directions of maximum variance. The animation shows the axes rotating to align with the data.

116. **t-SNE and UMAP** — Nonlinear dimensionality reduction for visualization. The animation shows clusters separating.

117. **Convolutional Neural Networks** — Filters slide over an image to detect features. The animation shows a kernel producing a feature map.

118. **Attention Mechanism** — Each token attends to others with learned weights. The animation shows a heatmap of attention scores.

119. **Transformer Architecture** — Stacked attention and feed-forward layers. The animation shows token embeddings flowing through blocks.

120. **Diffusion Models** — Add noise to data, then learn to denoise. The animation shows an image dissolving into noise and being reconstructed.

121. **Variational Autoencoders** — Encode to a latent distribution, sample, decode. The animation shows the latent space interpolating between digits.

122. **Generative Adversarial Networks** — Generator and discriminator compete. The animation shows the generator improving as the discriminator gets fooled.

123. **Reinforcement Learning: Q-Learning** — Learn action values from rewards. The animation shows a grid-world agent finding the goal.

124. **Policy Gradient Methods** — Directly optimize the policy parameters. The animation shows the policy distribution shifting toward better actions.

125. **Overfitting and Cross-Validation** — A model memorizes training data but fails on new data. The animation shows train vs validation error diverging.

---

## Control & Systems Engineering

126. **State-Space Representation** — ẋ = Ax + Bu, y = Cx + Du. The animation shows a system’s state trajectory in phase space.

127. **Controllability and Observability** — Can you drive the state anywhere? Can you infer it from outputs? The Kalman rank conditions answer both.

128. **Pole Placement** — Choose feedback gains to place closed-loop poles where you want them. The animation shows the root locus moving.

129. **Root Locus** — As gain increases, closed-loop poles trace paths in the complex plane. Stability is read from the left half-plane.

130. **Lead and Lag Compensators** — Shape the frequency response to improve stability and tracking.

131. **State Feedback and Observers** — Estimate unmeasured states with a Luenberger observer, then feed them back.

132. **Linear Quadratic Regulator** — Minimize a quadratic cost of state deviation and control effort. The Riccati equation gives the optimal gain.

133. **Model Predictive Control** — Solve an optimization at each step over a receding horizon. The animation shows the predicted trajectory and the applied control.

134. **Sliding Mode Control** — Drive the state onto a sliding surface and keep it there. Robust to matched disturbances.

135. **Adaptive Control** — Adjust controller parameters online as the plant changes. The animation shows parameters converging.

136. **Lyapunov Stability** — A scalar function that decreases along trajectories proves stability. The animation shows level sets shrinking.

137. **Describing Functions** — Approximate nonlinear systems with a quasi-linear gain. Predicts limit cycles.

138. **Bifurcation in Control Systems** — As a parameter varies, a stable equilibrium can lose stability and oscillate.

---

## Signal Processing & Information Theory

139. **Sampling Theorem** — A bandlimited signal can be reconstructed from samples at twice its bandwidth. Aliasing occurs below that rate.

140. **Aliasing Visualized** — A high-frequency sine sampled too slowly appears as a low-frequency sine. The wagon-wheel effect is a real-world example.

141. **Z-Transform** — The discrete-time analog of the Laplace transform. Poles and zeros determine stability and frequency response.

142. **Digital Filters: FIR vs IIR** — FIR filters have finite impulse response and linear phase; IIR filters are recursive and more efficient.

143. **Window Functions** — Rectangular, Hamming, Hann, Blackman. They trade main-lobe width for side-lobe suppression in spectral analysis.

144. **Spectrogram** — A time–frequency representation of a signal. The animation shows a chirp’s frequency rising over time.

145. **Wavelets** — Localized basis functions that capture both time and frequency. The animation shows a signal decomposed into scales.

146. **Compressed Sensing** — Recover a sparse signal from far fewer samples than Nyquist requires.

147. **Channel Capacity** — Shannon’s formula C = B log₂(1 + S/N). The animation shows capacity increasing with bandwidth and SNR.

148. **Error-Correcting Codes: Reed–Solomon** — Used in CDs, DVDs, and QR codes. The animation shows a codeword with errors being corrected.

149. **Convolutional Codes and Viterbi Decoding** — A trellis diagram tracks the most likely path through states.

150. **Turbo Codes and LDPC** — Near-Shannon-limit performance via iterative decoding.

---

## Quantum Mechanics & Relativity

151. **Wave–Particle Duality** — Electrons interfere like waves but arrive like particles. The double-slit animation shows the buildup of fringes.

152. **Schrödinger Equation** — The wavefunction evolves according to iħ ∂ψ/∂t = Ĥψ. The animation shows a wavepacket spreading.

153. **Particle in a Box** — Quantized energy levels emerge from boundary conditions. The animation shows the first few standing waves.

154. **Quantum Harmonic Oscillator** — Energy levels equally spaced at ħω. The animation shows Hermite polynomial wavefunctions.

155. **Tunneling** — A particle passes through a barrier it classically cannot cross. The animation shows the wavefunction decaying inside and emerging on the other side.

156. **Heisenberg Uncertainty Principle** — Δx Δp ≥ ħ/2. The animation shows a narrow position distribution corresponding to a broad momentum distribution.

157. **Spin and the Bloch Sphere** — A qubit’s state lives on the surface of a sphere. The animation shows rotations as unitary gates.

158. **Entanglement** — Two particles share a joint state that cannot be factored. Bell inequality violations are visualized.

159. **Quantum Teleportation** — Transfer a quantum state using entanglement and classical communication.

160. **Special Relativity: Time Dilation** — Moving clocks run slow. The animation shows a light clock on a moving train.

161. **Length Contraction** — Moving objects shorten in the direction of motion. The animation shows a ruler passing at high speed.

162. **Minkowski Spacetime** — Events in a 4D geometry with a light cone separating timelike, spacelike, and null intervals.

163. **General Relativity: Curvature** — Mass curves spacetime; objects follow geodesics. The animation shows a grid warping around a mass.

164. **Gravitational Lensing** — Light bends around massive objects. The animation shows a distant galaxy’s image distorted into an arc.

165. **Black Holes and Event Horizons** — The Schwarzschild radius defines the point of no return. The animation shows light cones tilting.

166. **Hawking Radiation** — Quantum effects near a horizon cause black holes to evaporate slowly.

167. **Cosmic Microwave Background** — The afterglow of the Big Bang. The animation shows the temperature fluctuations map.

168. **Hubble’s Law** — Distant galaxies recede faster. v = H₀ d. The animation shows an expanding raisin-bread universe.

---

## Optics, Photonics & Acoustics

169. **Snell’s Law** — n₁ sin θ₁ = n₂ sin θ₂. The animation shows a ray bending at an interface.

170. **Total Internal Reflection** — Beyond the critical angle, light reflects entirely. The basis of fiber optics.

171. **Interference: Young’s Double Slit** — Two coherent sources produce bright and dark fringes. The animation shows path difference building fringes.

172. **Diffraction Grating** — Many slits produce sharp peaks at specific angles. Used in spectrometers.

173. **Polarization** — Light’s electric field oscillates in a plane. The animation shows a polarizer filtering components.

174. **Brewster’s Angle** — At a specific angle, reflected light is fully polarized. Used in photography to cut glare.

175. **Thin-Film Interference** — Colors in soap bubbles and oil slicks come from path differences in a thin film.

176. **Laser Principles** — Population inversion, stimulated emission, and optical resonance. The animation shows photons multiplying in a cavity.

177. **Fiber Optics** — Light guided by total internal reflection. The animation shows a pulse traveling through a core.

178. **Photonic Crystals** — Periodic structures that control light like semiconductors control electrons.

179. **Metamaterials** — Engineered structures with negative refractive index. The animation shows light bending the “wrong” way.

180. **Doppler Effect** — Frequency shifts for moving sources or observers. The animation shows wavefronts compressing ahead and stretching behind.

181. **Shock Waves and Sonic Booms** — An object moving faster than sound creates a cone of pressure. The animation shows the Mach cone.

182. **Standing Waves in Pipes** — Open and closed pipes support different harmonics. The animation shows nodes and antinodes.

183. **Beat Frequencies** — Two close frequencies produce a slow amplitude modulation. The animation shows the envelope pulsing.

184. **Resonance in Musical Instruments** — A string or air column amplifies frequencies at its natural modes.

185. **Room Acoustics** — Reverberation time depends on volume and absorption. The animation shows sound reflections decaying.

---

## Fluid Dynamics & Heat Transfer

186. **Continuity Equation** — Mass conservation in a flow. The animation shows a pipe narrowing and velocity increasing.

187. **Navier–Stokes Equations** — The governing equations of viscous flow. The animation shows a vortex forming behind an obstacle.

188. **Boundary Layer** — A thin region near a surface where viscous effects dominate. The animation shows velocity profiles thickening downstream.

189. **Vortex Shedding** — Alternating vortices form behind a cylinder. The Kármán vortex street is visualized.

190. **Drag Crisis** — A sudden drop in drag when the boundary layer becomes turbulent. Golf ball dimples exploit this.

191. **Terminal Velocity** — Drag balances gravity. The animation shows a falling object’s velocity asymptoting.

192. **Buoyancy and Archimedes’ Principle** — The upward force equals the weight of displaced fluid. The animation shows a block floating at different depths.

193. **Bernoulli vs Venturi** — A constriction increases velocity and decreases pressure. The animation shows a Venturi tube.

194. **Capillary Action** — Surface tension draws liquid up a narrow tube. The animation shows the meniscus rising.

195. **Marangoni Effect** — Surface tension gradients drive flow. “Tears of wine” and soap-film propulsion are examples.

196. **Heat Conduction** — Fourier’s law: q = −k ∇T. The animation shows a rod heating from one end.

197. **Convection** — Hot fluid rises, cool fluid sinks. The animation shows Rayleigh–Bénard cells forming.

198. **Radiation: Stefan–Boltzmann** — Power radiated scales as T⁴. The animation compares blackbody spectra at different temperatures.

199. **Heat Pipe** — Evaporation and condensation move heat efficiently. The animation shows the cycle.

200. **Thermal Resistance Networks** — Series and parallel paths for heat flow, analogous to electrical circuits.

---

## Materials Science & Solid Mechanics

201. **Crystal Lattice and Miller Indices** — Planes in a crystal are labeled by (hkl). The animation shows several planes in a cubic cell.

202. **Dislocations** — Edge and screw dislocations explain plastic deformation. The animation shows a dislocation gliding through a lattice.

203. **Hall–Petch Relation** — Smaller grains mean stronger material. σ_y ∝ 1/√d.

204. **Creep** — Slow deformation under sustained load at high temperature. The animation shows strain versus time in three stages.

205. **Fatigue Crack Growth** — Paris’ law links crack growth per cycle to stress intensity range.

206. **Ductile vs Brittle Fracture** — Ductile materials neck and tear; brittle materials shatter. The animation shows both failure modes.

207. **Shape Memory Alloys** — Nitinol returns to a programmed shape when heated. The animation shows the phase transformation.

208. **Piezoelectricity** — Mechanical stress generates voltage, and vice versa. Used in sensors and actuators.

209. **Ferromagnetism and Hysteresis** — Magnetic domains align with an external field. The animation shows the hysteresis loop.

210. **Superconductivity** — Zero resistance below a critical temperature. The Meissner effect expels magnetic fields.

211. **Semiconductor Doping** — Adding impurities creates n-type or p-type material. The animation shows band diagrams shifting.

212. **Band Theory of Solids** — Conductor, semiconductor, insulator differ by band gap. The animation shows electron filling.

213. **Photovoltaics: p–n Junction** — Photons create electron–hole pairs; the junction separates them. The animation shows current flow.

214. **Thermoelectric Effect** — Temperature gradients generate voltage (Seebeck) and vice versa (Peltier).

215. **Composite Laminate Theory** — Ply orientation determines stiffness and strength. The animation shows a laminate with off-axis plies.

---

## Chemical, Process & Petroleum Engineering

216. **Arrhenius Equation** — Reaction rate increases exponentially with temperature. The animation shows rate constants on an Arrhenius plot.

217. **Le Chatelier’s Principle** — A system at equilibrium shifts to counteract a disturbance. The animation shows concentrations adjusting.

218. **Catalysis** — A catalyst lowers activation energy without being consumed. The animation shows a reaction pathway with and without catalyst.

219. **Distillation** — Separation by differences in volatility. The animation shows a McCabe–Thiele diagram and stage construction.

220. **Absorption and Stripping** — Gas–liquid mass transfer in packed columns. The animation shows concentration profiles.

221. **Heat Exchanger Networks** — Pinch analysis minimizes utility consumption. The animation shows composite curves.

222. **Reactor Design: CSTR vs PFR** — Continuous stirred tank vs plug flow. The animation compares conversion versus volume.

223. **Polymerization** — Monomers link into long chains. The animation shows chain growth and branching.

224. **Emulsion and Surfactants** — Amphiphilic molecules stabilize oil–water interfaces. The animation shows micelle formation.

225. **Petroleum Reservoir Simulation** — Darcy’s law and material balance model flow in porous media. The animation shows pressure depletion.

226. **Enhanced Oil Recovery** — Water flooding, CO₂ injection, and thermal methods. The animation shows sweep efficiency.

227. **Drilling Hydraulics** — Mud circulation removes cuttings and controls pressure. The animation shows annular flow.

228. **Well Logging** — Resistivity, gamma ray, and neutron logs infer rock properties. The animation shows a log track.

229. **Natural Gas Processing** — Remove water, acid gases, and heavy hydrocarbons. The animation shows a process flow diagram.

230. **Refinery Distillation** — Crude oil separates into fractions by boiling range. The animation shows a column with side draws.

---

## Civil, Structural & Geotechnical

231. **Soil Bearing Capacity** — Terzaghi’s equation gives the allowable load. The animation shows a footing and failure wedge.

232. **Slope Stability** — Factor of safety against sliding. The animation shows a circular slip surface.

233. **Earth Pressure: Rankine and Coulomb** — Lateral pressure on retaining walls. The animation shows active and passive wedges.

234. **Consolidation Settlement** — Clay compresses slowly as water drains. The animation shows excess pore pressure dissipating.

235. **Liquefaction** — Saturated sand loses strength during an earthquake. The animation shows pore pressure building.

236. **Pile Foundations** — Skin friction and end bearing carry load. The animation shows load transfer along a pile.

237. **Reinforced Concrete Beam** — Steel takes tension, concrete takes compression. The animation shows the strain distribution.

238. **Prestressed Concrete** — Pre-compression keeps concrete in compression under load. The animation shows tendon paths.

239. **Steel Connections** — Bolted and welded joints transfer forces. The animation shows load paths.

240. **Moment Frames vs Braced Frames** — Moment frames resist lateral loads by bending; braced frames by axial action. The animation compares drift.

241. **Shear Walls** — Concrete walls resist lateral loads. The animation shows deformation shapes.

242. **Base Isolation** — Rubber bearings decouple a building from ground motion. The animation compares accelerations.

243. **Tuned Mass Damper** — A secondary mass absorbs vibration. The Taipei 101 damper is the iconic example.

244. **Wind Loading** — Pressure depends on height, exposure, and shape. The animation shows streamlines around a building.

245. **Progressive Collapse** — Local failure can cascade. The animation shows a column removed and the structure redistributing.

---

## Biomedical, Environmental & Industrial

246. **Pharmacokinetics: Compartment Models** — One- and two-compartment models describe drug distribution. The animation shows concentration–time curves.

247. **Hemodynamics** — Blood flow follows Poiseuille’s law in vessels. The animation shows velocity profiles.

248. **Cardiac Output** — Fick principle and thermodilution. The animation shows stroke volume and heart rate.

249. **Respiratory Mechanics** — Compliance and resistance determine airflow. The animation shows a pressure–volume loop.

250. **Nerve Conduction** — Hodgkin–Huxley model of action potentials. The animation shows ion channels opening and voltage spiking.

251. **Enzyme Kinetics: Michaelis–Menten** — Rate saturates with substrate concentration. The animation shows the hyperbolic curve.

252. **Population Dynamics: Logistic Growth** — Carrying capacity limits exponential growth. The animation shows the S-curve.

253. **Predator–Prey Phase Plane** — Closed orbits in the Lotka–Volterra model. The animation shows the cycle.

254. **Epidemic Herd Immunity** — Threshold fraction vaccinated to stop spread. The animation shows R₀ and the threshold.

255. **Air Quality: Gaussian Plume** — Concentration downwind of a stack. The animation shows the plume dispersing.

256. **Water Quality: BOD and DO** — Biochemical oxygen demand depletes dissolved oxygen. The animation shows the sag curve.

257. **Groundwater Flow** — Darcy’s law and the water table. The animation shows a pumping well and cone of depression.

258. **Carbon Cycle** — Fluxes between atmosphere, ocean, and biosphere. The animation shows reservoirs and arrows.

259. **Climate Energy Balance** — Incoming solar versus outgoing infrared. The animation shows the greenhouse effect.

260. **Life Cycle Assessment** — Cradle-to-grave environmental impact. The animation shows stages and emissions.

261. **Queueing: M/M/1** — Arrival and service rates determine wait times. The animation shows queue length versus utilization.

262. **Little’s Law** — L = λW. Average number in system equals arrival rate times average time.

263. **Inventory: EOQ Model** — Economic order quantity balances ordering and holding costs. The animation shows the sawtooth inventory curve.

264. **Supply Chain Bullwhip Effect** — Small demand changes amplify upstream. The animation shows orders oscillating.

265. **Lean and Just-in-Time** — Reduce waste and inventory. The animation shows a pull system versus push.

---

## Financial Mathematics & Economics

266. **Compound Interest** — A = P(1 + r/n)^(nt). The animation shows continuous compounding approaching e^(rt).

267. **Present Value and Discounting** — A dollar today is worth more than a dollar tomorrow. The animation shows a cash flow timeline.

268. **Black–Scholes Model** — Option prices from a PDE. The animation shows the payoff and the price surface.

269. **Binomial Option Pricing** — A tree of up and down moves. The animation shows backward induction.

270. **Efficient Frontier** — Portfolios that maximize return for a given risk. The animation shows the curve and tangency portfolio.

271. **Capital Asset Pricing Model** — Expected return depends on beta. The animation shows the security market line.

272. **Value at Risk** — A quantile of the loss distribution. The animation shows the tail.

273. **Monte Carlo in Finance** — Simulate paths to price derivatives. The animation shows many paths and the average payoff.

274. **Mean Reversion: Ornstein–Uhlenbeck** — Prices pulled toward a long-run mean. The animation shows the process.

275. **GARCH Volatility** — Volatility clusters. The animation shows returns and conditional variance.

276. **Yield Curve** — Interest rates versus maturity. The animation shows normal, inverted, and flat curves.

277. **Duration and Convexity** — Bond price sensitivity to interest rates. The animation shows the price–yield curve.

278. **Nash Bargaining** — Splitting a surplus. The animation shows the bargaining set and solution.

279. **Auction Revenue Equivalence** — First-price and second-price auctions yield the same expected revenue under symmetry.

280. **Mechanism Design: VCG** — Truthful bidding is optimal. The animation shows payments and allocations.

---

## Miscellaneous Beauties & Cross-Disciplinary

281. **Benford’s Law** — Leading digits in natural data are not uniform. 1 appears about 30% of the time.

282. **Zipf’s Law** — Word frequencies rank by a power law. The animation shows the log–log plot.

283. **Pareto Principle** — 80% of effects come from 20% of causes. The animation shows the cumulative curve.

284. **Littlewood’s Law** — With enough time, improbable events happen. A “miracle” a month.

285. **Simpson’s Paradox** — A trend in subgroups can reverse when combined. The animation shows the aggregated vs disaggregated data.

286. **Survivorship Bias** — We see winners, not failures. The WWII bomber armor example is the classic.

287. **Regression to the Mean** — Extreme measurements tend to be followed by less extreme ones. The animation shows the scatter and the line.

288. **Ecological Fallacy** — Group statistics do not apply to individuals. The animation shows a scatter with a misleading aggregate.

289. **Goodhart’s Law** — When a measure becomes a target, it ceases to be a good measure.

290. **Braess’s Paradox in Networks** — Adding capacity can worsen congestion. The animation shows traffic redistributing.

291. **Chaos in the Three-Body Problem** — No closed-form solution; sensitive to initial conditions. The animation shows three masses orbiting chaotically.

292. **N-Body Simulation** — Gravity between many bodies. The animation shows a galaxy forming.

293. **Galton Board** — Balls falling through pegs form a binomial distribution. The animation shows the bell curve emerging.

294. **Buffon’s Needle** — Estimate π by dropping needles on a lined floor. The probability is 2/π.

295. **Random Walk on a Lattice** — 1D, 2D, and 3D returns. The animation shows a walker’s path.

296. **Percolation Theory** — At a critical density, a path spans the grid. The animation shows clusters growing.

297. **Ising Model** — Spins on a lattice with nearest-neighbor interactions. The animation shows a phase transition.

298. **Renormalization Group** — Coarse-grain a system to find universal behavior. The animation shows a spin system blocked.

299. **Entropy and the Second Law** — Disorder increases. The animation shows gas molecules filling a box.

300. **Maxwell’s Demon** — A hypothetical being that sorts molecules. Landauer’s principle shows why it cannot beat thermodynamics.

