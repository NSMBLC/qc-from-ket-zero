# Quantum Computing From |0⟩

> *Learn quantum computing the way qubits do: starting from |0⟩.*

Companion notebooks for IBM Quantum's
[*Understanding Quantum Information and Computation*](https://quantum.cloud.ibm.com/learning)
series by John Watrous (also available as a [free text](https://arxiv.org/abs/2507.11536) and
[videos](https://www.youtube.com/@qiskit)). Each course lesson has a matching notebook whose
headings mirror the course pages one to one: you read a course section, close the tab, rebuild
what you just learned **from memory, from scratch, in NumPy**, and verify it against Qiskit.
The notebooks teach nothing on their own and repeat nothing from the course; they are where
what you read becomes something you own. Along the way, Units I and II prepare you to pass the
IBM badge exams for their courses.

**The running project:** in parallel, the notebooks incrementally build a complete quantum
simulator using plain NumPy. Each lesson's verified from-memory functions are promoted into a
small, permanent library that later lessons import and extend. Lesson by lesson it learns to
hold a qubit, run circuits, execute the famous algorithms, simulate noise, and correct errors.
By the end, it covers essentially everything the course taught, in a few hundred lines of code
you understand completely, because you wrote every one of them.

## Philosophy

1. **Read short, build immediately.** Study sessions are 20–30 minutes. Then you close the
   source and reconstruct the concept in code, from memory. The struggle to reconstruct is
   where your learning happens.
2. **Two implementations of everything.** First by hand in NumPy (to understand it), then in
   Qiskit (to verify it, and to build real-world fluency). Your two versions must agree.
3. **Pedagogy over cleverness, always.** Explicit loops beat compact one-liners. Named
   intermediate variables beat chained expressions. Every cell can be read top-to-bottom and
   narrated. Optimized versions appear only in cells labeled as such.
4. **Confusion is data.** The moment something confuses you is the moment you have found the
   edge of your understanding, and it is likely where the next insight lives. In the confusion
   log, capture what puzzled you and how it clicked. This reinforces your learning.
5. **Teach while learning.** Each lesson ends with a teach-back and an exercise you design
   yourself. Explaining a concept in your own words is the strongest test of whether you
   understand it, and the finished notebooks become course material anyone can learn from.

## The method, in one loop

Work in two windows: the course in one, the matching notebook in the other.
For each section of a lesson:

1. 📖 Read/watch the matching course section, **20–30 min max**, then close the tab
2. ✍️ Notes in your own words + "the one sentence I'd use to teach this"
3. 🔨 **Build from memory** in NumPy
4. ✅ **Verify** against Qiskit and the course's own worked examples
5. 🧩 Log confusions · write one exercise of your own design
6. 🌾 Promote the keeper functions into the growing simulator library, so later lessons build on them

Each lesson closes with a from-memory gauntlet and a teach-back. Before each new lesson,
reproduce one result from the previous lesson from memory. Once a week, hold a consolidation
session: no new material.

## Getting started

Open **`notebooks/lesson00_setup.ipynb`** and follow it to the end. It walks you through
installing the dependencies, a short Python self-test, and
verifying that everything works. Every ✅ must print before moving on. It also has you choose
a path:

- **Path A: Real hardware + simulation (recommended).** Free
  [IBM Quantum](https://quantum.cloud.ibm.com) account, credentials saved once, and a day-one
  run on a real quantum computer. Lessons 4, 8, and 12 include hardware runs.
- **Path B: Simulation only.** Everything runs locally on your own machine, using Qiskit's
  simulators. This path covers the full course content and is ready the moment the packages
  are installed. Lesson 0 explains what simulation gives you and where it differs from real
  hardware.

Hardware setup is deferrable: nothing before Lesson 4 requires it, and you can switch paths
at any time.

## Notebook index

### Week 0: Setup & warm-ups

The warm-ups cover the full background the *Basics of Quantum Information* course recommends
(sets and functions, complex numbers, basic linear algebra), plus two things it quietly
assumes: probability and bit-string indexing. They are ordered by difficulty and by
dependency, each one handing off to the next.

| Notebook | What it covers |
|---|---|
| `lesson00_setup.ipynb` | Environment install & verification; Python self-test; path choice; day-one two-act hardware run (superposition, then interference); what simulation gives you and where it differs from real hardware |
| `warmup0a_sets_functions_bits.ipynb` | Sets, functions, Cartesian products and bit strings |
| `warmup0b_complex_numbers.ipynb` | Arithmetic, conjugate, modulus; polar form & Euler's formula; phases and an interference preview |
| `warmup0c_linear_algebra.ipynb` | Complex inner products & the dagger; matrices as machines & composition order; eigenvalues & spectral decomposition |
| `warmup0d_probability.ipynb` | Distributions as vectors; expectation, marginals, conditionals; sampling, 1/√shots convergence, and a Born-rule teaser that hands off to Lesson 1 |

### Unit I: Basics of Quantum Information

Pairs with the [course of the same name](https://quantum.cloud.ibm.com/learning/en/courses/basics-of-quantum-information); each notebook's headings match the course pages one to one.

| # | Notebook | Simulator harvest |
|---|---|---|
| 1 | `lesson01_single_systems.ipynb` | State validation, inner product, Born rule, the gate zoo |
| 2 | `lesson02_multiple_systems.ipynb` | Multi-qubit states, CNOT/CZ, partial measurement |
| 3 | `lesson03_quantum_circuits.ipynb` | The `Circuit` class: gate-on-qubit-k via Kronecker products |
| 4 | `lesson04_entanglement_in_action.ipynb` | Teleportation, superdense coding, CHSH · 🖥️ first hardware run |
| 🏅 | Badge exam | [*Basics of Quantum Information* exam](https://quantum.cloud.ibm.com/learning/en/courses/basics-of-quantum-information/exam) at IBM Training → IBM Credly badge |

### Unit II: Fundamentals of Quantum Algorithms

| # | Notebook | Highlight |
|---|---|---|
| 5 | `lesson05_quantum_query_algorithms.ipynb` | Deutsch–Jozsa, Bernstein–Vazirani, Simon; phase kickback |
| 6 | `lesson06_algorithmic_foundations.ipynb` | Reversible computation, Toffoli logic |
| 7 | `lesson07_phase_estimation_factoring.ipynb` | QFT, phase estimation, factoring 15 end-to-end |
| 8 | `lesson08_grovers_algorithm.ipynb` | The geometric picture, animated · 🖥️ hardware run |
| 🏅 | Badge exam | [*Fundamentals of Quantum Algorithms*](https://quantum.cloud.ibm.com/learning/en/courses/fundamentals-of-quantum-algorithms) exam → IBM Credly badge |

### Unit III: General Formulation of Quantum Information

| # | Notebook | Highlight |
|---|---|---|
| 9 | `lesson09_density_matrices.ipynb` | Partial trace; half a Bell state is pure noise |
| 10 | `lesson10_quantum_channels.ipynb` | Kraus operators; the simulator learns to be noisy |
| 11 | `lesson11_general_measurements.ipynb` | POVMs; distinguishing non-orthogonal states |
| 12 | `lesson12_purifications_fidelity.ipynb` | Schmidt = SVD; scoring real hardware with fidelity · 🖥️ |

### Unit IV: Foundations of Quantum Error Correction

| # | Notebook | Highlight |
|---|---|---|
| 13 | `lesson13_correcting_quantum_errors.ipynb` | Repetition & Shor codes; watching correction actually help |
| 14 | `lesson14_stabilizer_formalism.ipynb` | Pauli algebra; syndromes from stabilizers |
| 15 | `lesson15_code_constructions.ipynb` | CSS codes; a toric-code visualizer |
| 16 | `lesson16_fault_tolerance.ipynb` | The threshold theorem; capstone teach-back |

## Attribution & license

Lesson structure and topics follow *Understanding Quantum Information and Computation* by
John Watrous ([arXiv:2507.11536](https://arxiv.org/abs/2507.11536)), created with IBM and
released under a Creative Commons license for free use and adaptation by educators.
All notebooks, code, and exercises in this repository are original companion material,
designed by [Jesús Hernández Tapia](https://github.com/jtapia-ensmbl).

Repository license: CC BY-SA 4.0 (share and adapt with attribution, same license), chosen to
match the spirit of the source course. The simulator code may alternatively be used under MIT.
