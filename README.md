# Quantum Computing From |0⟩

> *Learn quantum computing the way qubits do — starting from |0⟩.*

A hands-on, build-everything-yourself journey through quantum computing, following John Watrous's
[*Understanding Quantum Information and Computation*](https://arxiv.org/abs/2507.11536)
(16 lessons, also available as [videos](https://www.youtube.com/@qiskit) and interactively on
[IBM Quantum Learning](https://quantum.cloud.ibm.com/learning)). Every lesson gets a companion
Jupyter notebook where the concepts are rebuilt **from memory, from scratch, in NumPy** — then
verified against Qiskit.

**The running project:** in parallel with the notebooks, this repo incrementally builds a
complete quantum simulator using plain NumPy. Each lesson's verified from-memory functions are
promoted into a small, permanent library that later lessons import and extend. Lesson by lesson
it learns to hold a qubit, run circuits, execute the famous algorithms, simulate noise, and
correct errors — by the end, it covers essentially everything the course taught, in a few
hundred lines of code you understand completely, because you wrote every one of them.

## Philosophy

1. **Read short, build immediately.** Study sessions are 20–30 minutes. Then you close the
   source and reconstruct the concept in code, from memory. The struggle to reconstruct is
   where your learning happens.
2. **Two implementations of everything.** First by hand in NumPy (to understand it), then in
   Qiskit (to verify it, and to build real-world fluency). Your two versions must agree.
3. **Pedagogy over cleverness — always.** Explicit loops beat compact one-liners. Named
   intermediate variables beat chained expressions. Every cell can be read top-to-bottom and
   narrated. Optimized versions appear only in cells labeled as such.
4. **Confusion is data.** The moment something confuses you is the moment you have found the 
   edge of your understanding, and it is likely where the next insight lives. In the confusion log,
   capture what puzzled you and how it clicked. This reinforces your learning.
5. **Teach while learning.** Each lesson ends with a teach-back and an exercise you design
   yourself. Explaining a concept in your own words is the strongest test of whether you
   understand it — and the finished notebooks become course material anyone can learn from.

## Choose your path

- **Path A — Real hardware + simulation (recommended):** free
  [IBM Quantum](https://quantum.cloud.ibm.com) account; credentials saved once in Lesson 0.
  Lessons 4, 8, and 12 include runs on real quantum computers.
- **Path B — Simulation only:** everything runs locally on your own machine, using Qiskit's
  simulators (`Statevector`, `AerSimulator`, and noisy snapshots of real devices). This path
  covers the full course content and is ready the moment the packages are installed.
  Lesson 0 explains what simulation gives you and where it differs from real hardware.

## Getting started

Open **`notebooks/lesson00_setup.ipynb`** and follow it to the end. It walks you through
installing the dependencies, choosing your path, and verifying that everything works —
every ✅ must print before moving on.

## Notebook index

### Week 0 — Setup & warm-ups
| Notebook | What it covers |
|---|---|
| `lesson00_setup.ipynb` | Environment install & verification; Path A credentials (saved safely) or Path B simulation; the limitations of simulation, honestly |
| `warmup0a_complex_numbers.ipynb` | Arithmetic, conjugate, modulus; polar form & Euler's formula; phases and an interference preview |
| `warmup0b_linear_algebra.ipynb` | Complex inner products & the dagger; matrices as machines & composition order; eigenvalues & spectral decomposition |
| `warmup0c_probability.ipynb` | Distributions as vectors; expectation, marginals, conditionals; sampling and 1/√shots convergence |

### Unit I — Basics of Quantum Information
| # | Notebook | Simulator harvest |
|---|---|---|
| 1 | `lesson01_single_systems.ipynb` | State validation, inner product, Born rule, the gate zoo |
| 2 | `lesson02_multiple_systems.ipynb` | Multi-qubit states, CNOT/CZ, partial measurement |
| 3 | `lesson03_quantum_circuits.ipynb` | The `Circuit` class — gate-on-qubit-k via Kronecker products |
| 4 | `lesson04_entanglement_in_action.ipynb` | Teleportation, superdense coding, CHSH · 🖥️ first hardware run |

### Unit II — Fundamentals of Quantum Algorithms
| # | Notebook | Highlight |
|---|---|---|
| 5 | `lesson05_quantum_query_algorithms.ipynb` | Deutsch–Jozsa, Bernstein–Vazirani, Simon; phase kickback |
| 6 | `lesson06_algorithmic_foundations.ipynb` | Reversible computation, Toffoli logic |
| 7 | `lesson07_phase_estimation_factoring.ipynb` | QFT, phase estimation, factoring 15 end-to-end |
| 8 | `lesson08_grovers_algorithm.ipynb` | The geometric picture, animated · 🖥️ hardware run |

### Unit III — General Formulation of Quantum Information
| # | Notebook | Highlight |
|---|---|---|
| 9 | `lesson09_density_matrices.ipynb` | Partial trace; half a Bell state is pure noise |
| 10 | `lesson10_quantum_channels.ipynb` | Kraus operators; the simulator learns to be noisy |
| 11 | `lesson11_general_measurements.ipynb` | POVMs; distinguishing non-orthogonal states |
| 12 | `lesson12_purifications_fidelity.ipynb` | Schmidt = SVD; scoring real hardware with fidelity · 🖥️ |

### Unit IV — Foundations of Quantum Error Correction
| # | Notebook | Highlight |
|---|---|---|
| 13 | `lesson13_correcting_quantum_errors.ipynb` | Repetition & Shor codes; watching correction actually help |
| 14 | `lesson14_stabilizer_formalism.ipynb` | Pauli algebra; syndromes from stabilizers |
| 15 | `lesson15_code_constructions.ipynb` | CSS codes; a toric-code visualizer |
| 16 | `lesson16_fault_tolerance.ipynb` | The threshold theorem; capstone teach-back |

## The method, in one loop

For each section of a lesson:

1. 📖 Read/watch **20–30 min max**, then close the source
2. ✍️ Notes in your own words + "the one sentence I'd use to teach this"
3. 🔨 **Build from memory** in NumPy
4. ✅ **Verify** against Qiskit
5. 🧩 Log confusions · write one self-made exercise
6. 🌾 Promote the keeper functions into the growing simulator library, so later lessons build on them

Before each new lesson: reproduce one result from the previous lesson from memory.
One weekly consolidation session: no new material.

## Attribution & license

Lesson structure and topics follow *Understanding Quantum Information and Computation* by
John Watrous ([arXiv:2507.11536](https://arxiv.org/abs/2507.11536)), created with IBM and
released under a Creative Commons license for free use and adaptation by educators.
All notebooks, code, and exercises in this repository are original companion material.

Repository license: CC BY-SA 4.0 (share and adapt with attribution, same license) — chosen to
match the spirit of the source course. The simulator code may alternatively be used under MIT.
