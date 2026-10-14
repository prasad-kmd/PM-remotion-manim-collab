Below is a curated topic bank of mathematics and engineering ideas suitable for short-form vertical videos. Each entry gives the core concept in a sentence or two, plus the natural visual hook where useful.

---

## Mathematics — Visual & Counterintuitive

1. **The π = 4 Staircase Paradox** — A square of perimeter 8 is repeatedly folded into a staircase that appears to become a circle of circumference 2π. The twist: the perimeter never changes, because the staircase’s tangent directions never converge to the circle’s.

2. **Sum of Odd Numbers = Perfect Squares** — 1 = 1², 1+3 = 2², 1+3+5 = 3², and so on. The visual proof is an L-shaped tile that wraps around a square and always completes the next perfect square.

3. **The Basel Problem** — The infinite sum 1 + 1/4 + 1/9 + 1/16 + … equals π²/6. A surprising bridge between simple fractions and the geometry of circles.

4. **Circle Area = πr² (Unrolling Proof)** — Cut a circle into thin concentric rings and unroll them into a triangle with base 2πr and height r. The area formula falls out geometrically.

5. **Why (−1) × (−1) = 1** — Multiplication by −1 is a 180° rotation on the number line. Doing it twice is a 360° rotation, which lands you back at the original number.

6. **Pythagorean Theorem by Rearrangement** — Four copies of a right triangle rearrange inside a square to reveal a² + b² = c² without algebra.

7. **Gabriel’s Horn** — A solid with finite volume but infinite surface area. It can be filled with paint but never painted.

8. **Banach–Tarski Paradox** — A sphere can be decomposed into finitely many pieces and reassembled into two identical spheres. A pure-math result that breaks physical intuition.

9. **Cantor’s Diagonal Argument** — There are more real numbers than natural numbers. The proof uses a diagonal construction that systematically produces a number missing from any proposed list.

10. **Hilbert’s Hotel** — An infinite hotel that is fully occupied can still accommodate infinitely many new guests by shifting everyone down one room. A clean introduction to countable infinity.

---

## Mathematics — Calculus, Analysis & Differential Equations

11. **Derivative as Infinite Zoom** — Zoom into any smooth curve far enough and it becomes a straight line. The slope of that line is the derivative.

12. **Integral as Accumulation** — The area under a curve is the limit of increasingly thin rectangles. This is the geometric meaning of the integral.

13. **Fundamental Theorem of Calculus** — Differentiation and integration are inverse operations. The animation shows a moving area function whose rate of change is the original curve.

14. **Taylor Series** — Any smooth function can be approximated by a polynomial built from its derivatives. Adding more terms makes the approximation hug the curve over a wider interval.

15. **Fourier Series of a Square Wave** — A square wave is the sum of odd sine waves with decreasing amplitudes. The animation shows sine waves stacking to form sharp corners.

16. **Fourier Transform** — Any signal can be decomposed into frequencies. The visual is a time-domain wave and its frequency-domain spectrum side by side.

17. **Euler’s Formula e^{iθ} = cos θ + i sin θ** — Complex exponentials trace out circles. The real part is cosine, the imaginary part is sine.

18. **Euler’s Identity e^{iπ} + 1 = 0** — A single equation linking e, i, π, 1, and 0. The animation shows a half-turn around the complex unit circle.

19. **The Gaussian Integral** — ∫ e^{−x²} dx = √π. The trick is to square the integral and switch to polar coordinates, where the double integral collapses.

20. **Harmonic Series Diverges** — 1 + 1/2 + 1/3 + 1/4 + … grows without bound, even though each term shrinks to zero. The grouping proof is a satisfying visual.

21. **Alternating Harmonic Series = ln 2** — 1 − 1/2 + 1/3 − 1/4 + … converges to the natural logarithm of 2. A rare case where rearrangement changes the sum.

22. **The Logistic Map and Chaos** — A simple recurrence xₙ₊₁ = r xₙ(1 − xₙ) produces period-doubling and chaos as r increases. The bifurcation diagram is one of the most beautiful objects in mathematics.

23. **SIR Model of Epidemics** — Three coupled differential equations track susceptible, infected, and recovered populations. The curve flattening is a direct consequence of the parameters.

24. **Lotka–Volterra Predator–Prey Equations** — Populations of predators and prey oscillate in a closed loop. The phase portrait shows a cycle rather than a fixed point.

25. **The Heat Equation** — Temperature diffuses from hot regions to cold regions. The animation shows an initial spike smoothing out over time.

26. **The Wave Equation** — A vibrating string decomposes into standing waves. Plucking at different points excites different harmonics.

---

## Probability, Statistics & Information

27. **Monty Hall Problem** — Switching doors wins two-thirds of the time. The visual shows the probability tree and why intuition fails.

28. **Birthday Paradox** — In a room of 23 people, there is a >50% chance two share a birthday. The count of pairs grows quadratically, not linearly.

29. **Bayes’ Theorem** — Prior belief plus new evidence gives posterior belief. A medical-test example shows why a positive result on a rare disease is often a false alarm.

30. **Central Limit Theorem** — Sums of independent random variables tend toward a normal distribution, regardless of the original distribution. The animation shows histograms smoothing into a bell curve.

31. **Law of Large Numbers** — Sample averages converge to the expected value as sample size grows. The running average wanders less and less.

32. **Random Walks** — A walker takes steps left or right with equal probability. In 1D, it returns to the origin infinitely often; in 2D, almost surely; in 3D, with positive probability it never returns.

33. **Markov Chains** — A system transitions between states with fixed probabilities. The animation shows a state diagram and the long-run distribution emerging.

34. **Gambler’s Ruin** — A gambler with finite capital playing a fair game will eventually go broke. The probability of ruin depends on the ratio of capital to bet size.

35. **Kelly Criterion** — The optimal fraction of capital to bet to maximize long-run growth. Bet too little and you grow slowly; bet too much and you risk ruin.

36. **Entropy and Information** — Shannon entropy measures uncertainty. A fair coin has 1 bit; a biased coin has less. The visual is a probability distribution and its entropy.

37. **Shannon Coding** — Frequent symbols get shorter codes. Huffman coding builds an optimal prefix code from a binary tree.

38. **Error-Correcting Codes** — Redundant bits let a receiver detect and fix errors. The Hamming code animation shows a 7-bit block correcting a single-bit flip.

---

## Discrete Math, Computer Science & Algorithms

39. **Big-O Notation** — How runtime scales with input size. The graph compares O(1), O(log n), O(n), O(n log n), and O(n²) as n grows.

40. **Sorting Algorithms Visualized** — Bubble sort, insertion sort, merge sort, and quicksort race on the same array. The comparison makes the efficiency difference obvious.

41. **Traveling Salesman Problem** — Find the shortest route visiting every city once. The number of possible tours explodes factorially, making brute force impossible beyond a few dozen cities.

42. **P vs NP** — Problems whose solutions are easy to verify but possibly hard to find. The animation contrasts a polynomial-time verifier with a hypothetical polynomial-time solver.

43. **Conway’s Game of Life** — A grid of cells evolves by three simple rules. Gliders, oscillators, and guns emerge from local interactions.

44. **Rule 30 Cellular Automaton** — A one-dimensional automaton that produces complex, seemingly random patterns from a simple rule. It is used as a random number generator.

45. **Neural Networks and Backpropagation** — A network of weights and biases learns by propagating errors backward. The animation shows a loss surface and gradient descent steps.

46. **Gradient Descent** — Follow the negative gradient downhill on a loss surface. Learning rate too small means slow convergence; too large means overshooting.

47. **Quantum Computing: Qubits** — A qubit is a superposition of |0⟩ and |1⟩ on the Bloch sphere. Measurement collapses it to one basis state.

48. **Shor’s Algorithm** — Factors large integers exponentially faster than the best known classical algorithm. It threatens RSA encryption.

49. **Grover’s Algorithm** — Searches an unsorted database in O(√N) queries instead of O(N). The amplitude-amplification steps are a clean geometric visual.

---

## Engineering — Electrical & Electronics

50. **Ohm’s Law** — V = IR. The animation shows voltage as pressure, current as flow, and resistance as a narrow pipe.

51. **Kirchhoff’s Laws** — Current into a node equals current out; voltage around a loop sums to zero. The visual is a circuit with annotated arrows.

52. **RLC Circuits** — A resistor, inductor, and capacitor in series produce damped oscillations. The step response shows overshoot, ringing, and settling.

53. **Fourier Analysis in Signal Processing** — A noisy signal is filtered by removing frequency components. The spectrum before and after shows the effect.

54. **PID Controller** — Proportional, integral, and derivative terms combine to control a system. The animation shows a step response with and without each term.

55. **Bode Plots** — Magnitude and phase of a system’s frequency response. The plot reveals gain margin and phase margin.

56. **Nyquist Criterion** — Stability of a feedback system from its open-loop frequency response. The Nyquist plot encircles −1 to determine closed-loop poles.

57. **Kalman Filter** — Recursively estimates the state of a noisy system. The animation shows a true trajectory, noisy measurements, and the filter’s estimate converging.

58. **PN Junction** — A p-type and n-type semiconductor form a depletion region and a built-in potential. Forward bias shrinks it; reverse bias widens it.

59. **MOSFET** — A voltage-controlled switch. The animation shows the channel forming as gate voltage increases.

60. **Op-Amp** — A high-gain differential amplifier. Negative feedback turns it into a precise amplifier, integrator, or differentiator.

61. **Digital Logic Gates** — AND, OR, NOT, NAND, NOR, XOR. The truth tables and transistor-level implementations are shown side by side.

62. **Boolean Algebra and Karnaugh Maps** — Simplify logic expressions by grouping adjacent 1s in a grid. The visual makes minimization intuitive.

63. **Finite State Machines** — A system with a finite number of states and transitions. The animation shows a traffic light or vending machine controller.

---

## Engineering — Mechanical, Aerospace & Robotics

64. **Stress–Strain Curve** — Elastic region, yield point, plastic region, ultimate strength, and fracture. The curve defines a material’s mechanical behavior.

65. **Mohr’s Circle** — A graphical method for transforming stress components. The circle shows principal stresses and maximum shear.

66. **Beam Bending** — A beam under load deflects. The animation shows the neutral axis, bending moment diagram, and deflection curve.

67. **Trusses** — A triangulated structure carries loads through axial forces in members. The method of joints solves for tension and compression.

68. **Buckling** — A slender column under compression suddenly bows sideways. The critical load depends on length and end conditions.

69. **Fatigue** — Repeated cyclic loading causes failure at stresses below the yield strength. The S–N curve shows life versus stress amplitude.

70. **Gears and Gear Ratios** — Meshing gears trade speed for torque. The animation shows teeth engaging and the ratio of angular velocities.

71. **Four-Bar Linkage** — A mechanism that converts rotation into complex motion. The coupler curve traces a path determined by link lengths.

72. **Robot Forward and Inverse Kinematics** — Forward: joint angles → end-effector position. Inverse: desired position → joint angles. The animation shows a 2D or 3D arm.

73. **Denavit–Hartenberg Parameters** — A systematic way to assign frames to robot joints. The table of DH parameters defines the kinematic chain.

74. **Bernoulli’s Principle** — Faster fluid flow means lower pressure. The animation shows streamlines over an airfoil and the resulting lift.

75. **Reynolds Number** — The ratio of inertial to viscous forces. Low Re is laminar; high Re is turbulent. The dye experiment is iconic.

76. **Laminar vs Turbulent Flow** — Smooth parallel layers versus chaotic eddies. The transition is shown in a pipe or boundary layer.

77. **Airfoil Lift and Drag** — Angle of attack, camber, and circulation generate lift. The pressure distribution and wake are visualized.

78. **Rocket Equation** — Δv = Isp g₀ ln(m₀/m_f). The tyranny of the rocket equation: most of the mass is fuel.

79. **Orbital Mechanics** — Conic sections describe orbits. The animation shows a satellite’s elliptical path with the central body at a focus.

80. **Hohmann Transfer** — The most fuel-efficient two-burn maneuver between circular orbits. The transfer ellipse touches both orbits.

81. **Kepler’s Laws** — Orbits are ellipses; equal areas in equal times; T² ∝ a³. The animation sweeps the area and compares periods.

82. **Gravity Assist** — A spacecraft steals momentum from a planet. The flyby changes the heliocentric velocity without fuel.

---

## Engineering — Civil, Materials & Environmental

83. **Truss Bridges** — Triangulated members carry tension and compression. The animation shows force flow under a moving load.

84. **Arch Bridges** — The arch converts vertical loads into compression along its curve. The thrust line stays within the arch.

85. **Suspension Bridges** — The cable takes tension, the deck takes bending, and the towers take compression. The animation shows load paths.

86. **Structural Resonance** — The Tacoma Narrows Bridge twisted itself apart because wind excited a torsional mode. The animation shows a structure vibrating at its natural frequency.

87. **Earthquake Engineering** — Base isolation and dampers reduce seismic forces. The animation compares a fixed-base building with a base-isolated one.

88. **Concrete vs Steel** — Concrete is strong in compression; steel is strong in tension. Reinforced concrete combines both.

89. **Phase Diagrams** — Temperature and composition determine which phases exist. The lever rule gives phase fractions.

90. **Crystal Structures** — FCC, BCC, and HCP unit cells. The animation shows atoms packing and the resulting coordination numbers.

91. **Fracture Mechanics** — Stress intensity factor and crack propagation. A small crack can grow catastrophically.

92. **Composite Materials** — Fibers carry load in the direction of alignment; the matrix transfers load between fibers. The animation shows a lamina and its anisotropy.

93. **Water Treatment** — Coagulation, flocculation, sedimentation, filtration, and disinfection. The animation follows a particle through the process.

94. **Air Pollution Dispersion** — Gaussian plume model. The concentration downwind depends on stack height, wind speed, and stability class.

---

## Engineering — Thermal, Energy & Chemical

95. **Carnot Cycle** — The most efficient possible heat engine operating between two reservoirs. The P–V diagram shows two isotherms and two adiabats.

96. **Entropy** — A measure of disorder or unavailable energy. The animation shows gas expanding into a vacuum and the number of microstates increasing.

97. **Rankine Cycle** — The ideal cycle for steam power plants. Pump, boiler, turbine, condenser. The T–s diagram shows the four processes.

98. **Brayton Cycle** — The ideal cycle for gas turbines and jet engines. Compressor, combustor, turbine. The animation shows the open vs closed cycle.

99. **Refrigeration Cycle** — A reversed Rankine cycle moves heat from cold to hot. The coefficient of performance is the ratio of cooling to work input.

100. **Heat Exchangers** — Counterflow vs parallel flow. The temperature profiles show why counterflow is more effective.

101. **Solar PV** — Photons excite electrons across a bandgap. The I–V curve and maximum power point are shown.

102. **Wind Turbines** — Betz limit: no turbine can extract more than 16/27 of the wind’s kinetic energy. The animation shows the wake and power curve.

103. **Battery Chemistry** — Lithium-ion cells shuttle lithium ions between electrodes. The animation shows charge and discharge cycles.

104. **Fuel Cells** — Hydrogen and oxygen combine to produce electricity and water. The animation shows the anode, cathode, and proton-exchange membrane.

105. **Nuclear Fission** — A neutron splits a heavy nucleus, releasing energy and more neutrons. The chain reaction is controlled by moderators and control rods.

106. **Fusion** — Light nuclei combine at extreme temperatures. The proton–proton chain and tokamak magnetic confinement are visualized.

---

## Engineering — Biomedical & Systems

107. **ECG** — The electrical activity of the heart. The P, QRS, and T waves correspond to atrial depolarization, ventricular depolarization, and repolarization.

108. **MRI** — Magnetic fields align nuclear spins; radio waves excite them; gradients encode position. The animation shows slice selection and Fourier reconstruction.

109. **Prosthetics** — A prosthetic limb uses sensors, actuators, and control algorithms. The animation shows a myoelectric hand responding to muscle signals.

110. **Drug Delivery** — A drug’s concentration in the body follows pharmacokinetic curves. The animation shows immediate-release vs sustained-release profiles.

111. **Epidemiology** — SIR, SEIR, and network models. The animation shows herd immunity thresholds and the effect of vaccination.

112. **Reliability Engineering** — Bathtub curve: infant mortality, useful life, wear-out. Redundancy and mean time between failures are visualized.

113. **Queueing Theory** — Arrivals, service, and waiting lines. Little’s Law: L = λW. The animation shows queue length versus arrival rate.

114. **Linear Programming** — Optimize a linear objective subject to linear constraints. The feasible region is a polygon; the optimum is at a vertex.

115. **Monte Carlo Methods** — Estimate π by throwing random darts at a square. The animation shows the ratio converging.

116. **Finite Element Method** — Divide a complex domain into simple elements. The animation shows a mesh refining and the solution converging.