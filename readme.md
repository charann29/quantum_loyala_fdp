# 🌟 Quantum Computing Workshop - Complete Guide

> A comprehensive 2-day workshop covering quantum computing fundamentals, from basic concepts to hands-on circuit building with IBM Qiskit.

[![Qiskit](https://img.shields.io/badge/Qiskit-Enabled-6929c4?style=flat&logo=qiskit)](https://qiskit.org/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat&logo=python)](https://www.python.org/)
[![IBM Quantum](https://img.shields.io/badge/IBM-Quantum-052FAD?style=flat&logo=ibm)](https://quantum-computing.ibm.com/)

---

## 📚 Table of Contents

- [Workshop Overview](#workshop-overview)
- [Prerequisites](#prerequisites)
- [Day 1: Foundations](#day-1-foundations-of-quantum-computation)
- [Day 2: Quantum Logic & Circuits](#day-2-quantum-logic--circuits)
- [Setup Instructions](#setup-instructions)
- [Complete Lab Guide](#complete-lab-guide)
- [Resources](#resources)
- [Assignments](#assignments)

---

## 🎯 Workshop Overview

This intensive 2-day workshop introduces quantum computing through a balanced mix of theoretical foundations and practical hands-on experience. Participants will learn to build, simulate, and analyze quantum circuits using industry-standard tools.

### Learning Outcomes

By the end of this workshop, you will:

- ✅ Understand the fundamental principles of quantum computation
- ✅ Master quantum gates and circuit construction
- ✅ Visualize quantum states using the Bloch sphere
- ✅ Build and simulate quantum circuits using IBM Qiskit
- ✅ Create entangled states and understand multi-qubit systems
- ✅ Design educational materials for teaching quantum concepts

---

## 🔧 Prerequisites

### Knowledge Requirements
- Basic linear algebra (vectors, matrices)
- Familiarity with complex numbers
- Basic Python programming (helpful but not required)

### Technical Requirements
- Computer with internet access
- Google Colab account (free) OR local Python 3.8+ installation
- IBM Quantum account (free) - [Register here](https://quantum-computing.ibm.com/)

### Recommended Preparation
- Review complex number operations
- Brush up on vector and matrix multiplication
- Install Python and Jupyter Notebook (optional)

---

## 📅 Day 1: Foundations of Quantum Computation

### 🌅 Morning Session (3 hours)

#### 1. Introduction to Quantum Computing (45 mins)

**Topics Covered:**
- **Motivation**: Why quantum computing? Current limitations of classical computers
- **Real-world applications**: Drug discovery, cryptography, optimization, AI
- **Quantum advantage**: Problems where quantum computers excel
- **Current state**: IBM, Google, IonQ, and other quantum platforms

**Key Concepts:**
- Moore's Law limitations
- Quantum supremacy vs. quantum advantage
- NISQ era (Noisy Intermediate-Scale Quantum)

**Presentation Materials:**
- [Day 1 Slides](http://loyola0.netlify.app/)
- [Quantum Computing Notes](https://drive.google.com/file/d/1MvAUtJ7jURzMa5qLPwOwmgTgf_1UnBHm/view?usp=sharing)

---

#### 2. Quantum Computing Postulates (45 mins)

**The Four Postulates:**

1. **State Space**: Quantum systems are described by vectors in Hilbert space
2. **Evolution**: Quantum gates are unitary transformations
3. **Measurement**: Observables are Hermitian operators
4. **Composite Systems**: Multiple qubits form tensor product spaces

**Mathematical Foundations:**
- Dirac notation: |ψ⟩, ⟨ψ|
- Probability amplitudes
- Born rule for measurement

---

#### 3. Linear Algebra Essentials (45 mins)

**Core Concepts:**

**Vectors:**
```
|0⟩ = [1]    |1⟩ = [0]    |+⟩ = [1/√2]
      [0]          [1]           [1/√2]
```

**Complex Numbers:**
- Form: a + bi where i² = -1
- Magnitude: |z| = √(a² + b²)
- Phase: θ = arctan(b/a)

**Matrices and Operators:**
- Identity matrix
- Pauli matrices (X, Y, Z)
- Hadamard matrix
- Matrix multiplication and conjugate transpose

**Key Operations:**
- Inner product: ⟨ψ|φ⟩
- Outer product: |ψ⟩⟨φ|
- Tensor product: |ψ⟩ ⊗ |φ⟩

---

#### 4. Qubits and Superposition (45 mins)

**Classical vs Quantum Bits:**

| Feature | Classical Bit | Qubit |
|---------|--------------|-------|
| States | 0 OR 1 | 0 AND 1 simultaneously |
| Information | 1 bit | Infinite (continuous parameters) |
| Measurement | Read without change | Collapses to 0 or 1 |

**Superposition:**
```
|ψ⟩ = α|0⟩ + β|1⟩
```
where:
- α, β are complex probability amplitudes
- |α|² + |β|² = 1 (normalization)
- |α|² = probability of measuring 0
- |β|² = probability of measuring 1

**Examples:**
- Equal superposition: |+⟩ = (|0⟩ + |1⟩)/√2
- Phase superposition: |-⟩ = (|0⟩ - |1⟩)/√2

**The Measurement Problem:**
- Superposition exists before measurement
- Measurement collapses the state
- Outcome is probabilistic
- Cannot measure without disturbing

---

#### 5. Bloch Sphere Representation (45 mins)

**Understanding the Bloch Sphere:**

The Bloch sphere is a 3D visualization where any single-qubit state maps to a point on the sphere's surface.

**Key Features:**
- **North Pole**: |0⟩ state
- **South Pole**: |1⟩ state
- **Equator**: Equal superposition states
- **Latitude**: Probability of measuring 0 vs 1
- **Longitude**: Relative phase between amplitudes

**Parametric Form:**
```
|ψ⟩ = cos(θ/2)|0⟩ + e^(iφ)sin(θ/2)|1⟩
```
where θ ∈ [0, π] and φ ∈ [0, 2π]

**Cardinal States:**
- **|0⟩**: θ=0 (North Pole)
- **|1⟩**: θ=π (South Pole)
- **|+⟩**: θ=π/2, φ=0 (X-axis, positive)
- **|-⟩**: θ=π/2, φ=π (X-axis, negative)
- **|+i⟩**: θ=π/2, φ=π/2 (Y-axis, positive)
- **|-i⟩**: θ=π/2, φ=3π/2 (Y-axis, negative)

---

### 🌆 Afternoon Session: Hands-on Labs (2.5 hours)

#### Lab 1: IBM Quantum Composer Introduction (30 mins)

**Objective:** Familiarize yourself with the IBM Quantum Composer interface

**Steps:**
1. Visit [IBM Quantum Composer](https://quantum-computing.ibm.com/composer)
2. Create a free IBM Quantum account
3. Explore the interface:
   - Circuit canvas
   - Gate palette
   - Measurement tools
   - Visualization options

**Activities:**
- Create your first single-qubit circuit
- Add an H gate and measurement
- Run simulation (1024 shots)
- Observe the histogram results

**Expected Output:**
- Approximately 50% measurements of |0⟩
- Approximately 50% measurements of |1⟩

---

#### Lab 2: Setting Up Qiskit Environment (30 mins)

**Option A: Google Colab (Recommended)**

```python
# Run in a Colab cell
!pip install qiskit qiskit-aer matplotlib numpy --quiet

print("✅ Installation complete!")
print("Ready to explore quantum computing!")
```

**Option B: Local Installation**

```bash
# Create virtual environment
python -m venv quantum_env

# Activate environment
# Windows:
quantum_env\Scripts\activate
# Mac/Linux:
source quantum_env/bin/activate

# Install packages
pip install qiskit qiskit-aer matplotlib numpy jupyter
```

**Verify Installation:**

```python
import qiskit
print(f"Qiskit version: {qiskit.__version__}")

from qiskit import QuantumCircuit
qc = QuantumCircuit(1)
print("✅ Qiskit is working!")
```

---

#### Lab 3: Creating and Measuring Single-Qubit States (45 mins)

**Part A: The |0⟩ State**

```python
from qiskit import QuantumCircuit, transpile
from qiskit_aer import AerSimulator
from qiskit.visualization import plot_histogram
import matplotlib.pyplot as plt

# Create circuit
qc_zero = QuantumCircuit(1, 1)
qc_zero.measure(0, 0)

# Run simulation
simulator = AerSimulator()
compiled = transpile(qc_zero, simulator)
job = simulator.run(compiled, shots=1000)
result = job.result()
counts = result.get_counts()

# Visualize
print("Results:", counts)
plot_histogram(counts, title='State |0⟩')
plt.show()
```

**Expected:** {'0': 1000} (100% probability)

---

**Part B: The |1⟩ State (X Gate)**

```python
qc_one = QuantumCircuit(1, 1)
qc_one.x(0)  # Apply X gate (quantum NOT)
qc_one.measure(0, 0)

# Simulate
compiled = transpile(qc_one, simulator)
job = simulator.run(compiled, shots=1000)
counts = job.result().get_counts()

plot_histogram(counts, title='State |1⟩ (X Gate)')
plt.show()
```

**Expected:** {'1': 1000} (100% probability)

---

**Part C: Superposition (H Gate)**

```python
qc_super = QuantumCircuit(1, 1)
qc_super.h(0)  # Hadamard gate
qc_super.measure(0, 0)

compiled = transpile(qc_super, simulator)
job = simulator.run(compiled, shots=1000)
counts = job.result().get_counts()

plot_histogram(counts, title='Superposition |+⟩')
plt.show()
```

**Expected:** {'0': ~500, '1': ~500} (50/50 distribution)

**Discussion Points:**
- Why do we get different results each run?
- What happens if we increase shots to 10,000?
- Can we predict which outcome for a single measurement?

---

#### Lab 4: Bloch Sphere Visualization (45 mins)

**Visualizing Multiple States:**

```python
from qiskit.quantum_info import Statevector
from qiskit.visualization import plot_bloch_multivector

# Create circuits (no measurement for visualization)
qc_0 = QuantumCircuit(1)
qc_1 = QuantumCircuit(1)
qc_1.x(0)
qc_plus = QuantumCircuit(1)
qc_plus.h(0)

# Get statevectors
state_0 = Statevector.from_instruction(qc_0)
state_1 = Statevector.from_instruction(qc_1)
state_plus = Statevector.from_instruction(qc_plus)

# Create subplot with 3D projections
fig, axes = plt.subplots(1, 3, figsize=(15, 4), 
                         subplot_kw=dict(projection='3d'))

# Plot on Bloch spheres
plot_bloch_multivector(state_0, title="|0⟩", ax=axes[0])
plot_bloch_multivector(state_1, title="|1⟩", ax=axes[1])
plot_bloch_multivector(state_plus, title="|+⟩", ax=axes[2])

plt.tight_layout()
plt.show()
```

**Creating All Six Cardinal States:**

```python
# Define all cardinal states
circuits = {
    '|0⟩': QuantumCircuit(1),
    '|1⟩': QuantumCircuit(1),
    '|+⟩': QuantumCircuit(1),
    '|-⟩': QuantumCircuit(1),
    '|+i⟩': QuantumCircuit(1),
    '|-i⟩': QuantumCircuit(1)
}

circuits['|1⟩'].x(0)
circuits['|+⟩'].h(0)
circuits['|-⟩'].x(0); circuits['|-⟩'].h(0)
circuits['|+i⟩'].h(0); circuits['|+i⟩'].s(0)
circuits['|-i⟩'].h(0); circuits['|-i⟩'].sdg(0)

# Create 2x3 grid of Bloch spheres
fig, axes = plt.subplots(2, 3, figsize=(15, 10),
                         subplot_kw=dict(projection='3d'))
axes = axes.flatten()

for idx, (name, qc) in enumerate(circuits.items()):
    state = Statevector.from_instruction(qc)
    plot_bloch_multivector(state, title=name, ax=axes[idx])

plt.tight_layout()
plt.show()
```

**Exploration Tasks:**
1. Identify the position of each state on the Bloch sphere
2. Measure the angle from the Z-axis for each state
3. Note which states have phase differences

---

#### Lab 5: Group Activity - Build Superposition States (30 mins)

**Activity: Custom Quantum State Builder**

**Objective:** Work in groups to create specific quantum states using gate combinations

**Challenge Problems:**

**Problem 1: Create the |-⟩ state**
```python
# Your solution here
qc = QuantumCircuit(1)
# Add gates to create |-⟩
```

<details>
<summary>Solution</summary>

```python
qc = QuantumCircuit(1)
qc.x(0)  # Flip to |1⟩
qc.h(0)  # Apply Hadamard
# Result: |-⟩ = (|0⟩ - |1⟩)/√2
```
</details>

---

**Problem 2: Create the |+i⟩ state**
```python
qc = QuantumCircuit(1)
# Add gates to create |+i⟩
```

<details>
<summary>Solution</summary>

```python
qc = QuantumCircuit(1)
qc.h(0)  # Create |+⟩
qc.s(0)  # Add 90° phase
# Result: |+i⟩ = (|0⟩ + i|1⟩)/√2
```
</details>

---

**Problem 3: What does H-X-H create?**
```python
qc = QuantumCircuit(1)
qc.h(0)
qc.x(0)
qc.h(0)
# What state is this?
```

<details>
<summary>Answer</summary>

Creates the |1⟩ state! (H-X-H is equivalent to Z gate)
</details>

---

**Group Challenge: State Detective**

One group creates a mystery quantum state (using 2-3 gates). Other groups must:
1. Measure the state multiple times
2. View it on the Bloch sphere
3. Deduce which gates were used

```python
# Mystery state creator
mystery = QuantumCircuit(1)
# Add your secret gates here...

# Detective code
state = Statevector.from_instruction(mystery)
plot_bloch_multivector(state, title="Mystery State")
plt.show()

# Can you figure out which gates were used?
```

---

### 📝 Day 1 Assignment

**Part 1: Lecture Plan (15-20 minutes)**

Create a detailed lesson plan for introducing quantum computing to beginners.

**Requirements:**
- **Topic**: Introduction to Qubits and Superposition
- **Duration**: 15-20 minutes
- **Components needed**:
  - Learning objectives (3-5 points)
  - Key concepts to cover
  - Real-world analogies or examples
  - Visual aids or diagrams description
  - Engagement questions for students
  - Common misconceptions to address

**Suggested Structure:**
1. Hook/Motivation (2 mins)
2. Classical vs Quantum (3 mins)
3. Superposition Explained (5 mins)
4. Bloch Sphere Introduction (5 mins)
5. Practical Demonstration (3 mins)
6. Q&A and Summary (2 mins)

---

**Part 2: Lab Activity Outline**

Design a hands-on lab activity for students.

**Requirements:**
- **Title**: Creative and descriptive
- **Duration**: 30-45 minutes
- **Learning Objectives**: What will students achieve?
- **Prerequisites**: What should students know beforehand?
- **Materials Needed**: Software, accounts, handouts
- **Step-by-Step Instructions**: Clear, numbered steps
- **Expected Outcomes**: What results should students see?
- **Discussion Questions**: 3-5 questions to reinforce learning
- **Extensions**: Optional challenges for advanced students

**Example Topics:**
- Exploring quantum gates visually
- Building a quantum random number generator
- Comparing classical and quantum probability
- Creating art with quantum superposition

**Submission Format:**
- PDF or Markdown document
- Include code snippets if relevant
- Add screenshots or diagrams
- Provide answer keys for instructors

---

## 📅 Day 2: Quantum Logic & Circuits

### 🌅 Morning Session (3 hours)

#### 1. Single-Qubit Quantum Gates (60 mins)

**Pauli Gates:**

**X Gate (Quantum NOT):**
```
X = [0  1]    X|0⟩ = |1⟩
    [1  0]    X|1⟩ = |0⟩
```
- Flips qubit state (bit flip)
- Rotation by π around X-axis of Bloch sphere
- Classical equivalent: NOT gate

```python
qc = QuantumCircuit(1)
qc.x(0)
```

---

**Y Gate:**
```
Y = [0  -i]    Y|0⟩ = i|1⟩
    [i   0]    Y|1⟩ = -i|0⟩
```
- Bit flip AND phase flip
- Rotation by π around Y-axis
- Less commonly used but important for completeness

```python
qc = QuantumCircuit(1)
qc.y(0)
```

---

**Z Gate (Phase Flip):**
```
Z = [1   0]    Z|0⟩ = |0⟩
    [0  -1]    Z|1⟩ = -|1⟩
```
- Flips phase of |1⟩ state
- Rotation by π around Z-axis
- No effect on computational basis states (|0⟩, |1⟩)
- Changes superposition: |+⟩ → |-⟩

```python
qc = QuantumCircuit(1)
qc.z(0)
```

---

**Hadamard Gate (H):**
```
H = 1/√2 [1   1]    H|0⟩ = |+⟩ = (|0⟩ + |1⟩)/√2
         [1  -1]    H|1⟩ = |-⟩ = (|0⟩ - |1⟩)/√2
```
- Creates equal superposition
- Most important gate in quantum computing
- Rotation by π around axis at 45° between X and Z
- Self-inverse: H·H = I (applying twice returns to original)

```python
qc = QuantumCircuit(1)
qc.h(0)
```

**Key Property:** H transforms between computational basis (|0⟩, |1⟩) and superposition basis (|+⟩, |-⟩)

---

**Phase Gates:**

**S Gate (Phase π/2):**
```
S = [1  0]    S|0⟩ = |0⟩
    [0  i]    S|1⟩ = i|1⟩
```
- Adds 90° phase rotation
- Quarter turn around Z-axis
- S² = Z (two S gates equal one Z gate)

```python
qc = QuantumCircuit(1)
qc.s(0)
qc.sdg(0)  # S-dagger (inverse)
```

---

**T Gate (Phase π/4):**
```
T = [1  0    ]    T|0⟩ = |0⟩
    [0  e^(iπ/4)]    T|1⟩ = e^(iπ/4)|1⟩
```
- Adds 45° phase rotation
- Eighth turn around Z-axis
- T² = S (two T gates equal one S gate)
- Important for universal quantum computation

```python
qc = QuantumCircuit(1)
qc.t(0)
qc.tdg(0)  # T-dagger (inverse)
```

---

**Gate Relationships:**

```
X·X = I (identity)
Y·Y = I
Z·Z = I
H·H = I

S·S = Z
T·T·T·T = Z
S·S·S·S = I

H·Z·H = X  (basis transformation)
H·X·H = Z
```

**Universal Gate Set:** Any quantum operation can be built from {H, T, CNOT}

---

#### 2. Quantum Circuit Representation (45 mins)

**Circuit Notation Basics:**

**Reading Circuits:**
```
     ┌───┐┌───┐┌─┐
q_0: ┤ H ├┤ X ├┤M├
     └───┘└───┘└╥┘
c: 1/═══════════╩═
                0
```

**Components:**
- **Horizontal lines**: Qubits (top) and classical bits (bottom)
- **Gates**: Boxes on qubit wires
- **Measurements**: Meter symbols
- **Time flows left to right**

---

**Multi-Gate Circuits:**

```python
from qiskit import QuantumCircuit

qc = QuantumCircuit(1, 1)
qc.h(0)      # Apply Hadamard
qc.t(0)      # Apply T gate
qc.h(0)      # Apply Hadamard again
qc.measure(0, 0)

print(qc.draw(output='text'))
```

**Circuit Composition:**
```python
# Create sub-circuits
qc1 = QuantumCircuit(1)
qc1.h(0)

qc2 = QuantumCircuit(1)
qc2.x(0)

# Combine them
full_circuit = qc1.compose(qc2)
```

---

**Barriers and Organization:**

```python
qc = QuantumCircuit(3)
qc.h(0)
qc.h(1)
qc.barrier()  # Visual separator (no operation)
qc.x(2)
qc.barrier()
qc.measure_all()

print(qc.draw(output='text'))
```

Barriers help organize circuits visually and can prevent optimization across sections.

---

#### 3. Multi-Qubit Systems (45 mins)

**Tensor Product Notation:**

**Two-Qubit Basis States:**
```
|00⟩ = |0⟩ ⊗ |0⟩ = [1, 0, 0, 0]ᵀ
|01⟩ = |0⟩ ⊗ |1⟩ = [0, 1, 0, 0]ᵀ
|10⟩ = |1⟩ ⊗ |0⟩ = [0, 0, 1, 0]ᵀ
|11⟩ = |1⟩ ⊗ |1⟩ = [0, 0, 0, 1]ᵀ
```

**State Space Size:**
- 1 qubit: 2¹ = 2 basis states
- 2 qubits: 2² = 4 basis states
- 3 qubits: 2³ = 8 basis states
- n qubits: 2ⁿ basis states (exponential!)

**General Two-Qubit State:**
```
|ψ⟩ = α|00⟩ + β|01⟩ + γ|10⟩ + δ|11⟩
where |α|² + |β|² + |γ|² + |δ|² = 1
```

---

**Product States vs Entangled States:**

**Product State (Separable):**
```
|ψ⟩ = (α|0⟩ + β|1⟩) ⊗ (γ|0⟩ + δ|1⟩)
     = |ψ_A⟩ ⊗ |ψ_B⟩
```
Can be written as a product of individual qubit states.

**Example:**
```python
qc = QuantumCircuit(2)
qc.h(0)  # First qubit in superposition
qc.x(1)  # Second qubit in |1⟩
# Result: |ψ⟩ = |+⟩ ⊗ |1⟩ (separable)
```

---

**Entangled State (Non-separable):**
```
|Φ⁺⟩ = (|00⟩ + |11⟩)/√2
```
**Cannot** be written as |ψ_A⟩ ⊗ |ψ_B⟩

**Key Properties of Entanglement:**
- Measurement of one qubit instantly affects the other
- Correlation exists even at arbitrary distances
- Foundation of quantum teleportation and cryptography
- Einstein called it "spooky action at a distance"

---

#### 4. The CNOT Gate and Entanglement (30 mins)

**CNOT (Controlled-NOT) Gate:**

```
     ●
     │
     ⊕

CNOT Matrix (4×4):
[1 0 0 0]
[0 1 0 0]
[0 0 0 1]
[0 0 1 0]
```

**Operation:**
- **Control qubit** (●): Top qubit
- **Target qubit** (⊕): Bottom qubit
- **Action**: If control is |1⟩, flip target; otherwise do nothing

**Truth Table:**
```
|00⟩ → |00⟩  (control=0, target unchanged)
|01⟩ → |01⟩  (control=0, target unchanged)
|10⟩ → |11⟩  (control=1, target flipped)
|11⟩ → |10⟩  (control=1, target flipped)
```

---

**Creating Bell States:**

The four **Bell states** form a maximally entangled basis:

**|Φ⁺⟩ (Bell State):**
```python
qc = QuantumCircuit(2)
qc.h(0)      # Create superposition on qubit 0
qc.cx(0, 1)  # CNOT: qubit 0 controls, qubit 1 target
# Result: (|00⟩ + |11⟩)/√2
```

**Mathematical Derivation:**
```
Start: |00⟩
After H on q0: (|0⟩ + |1⟩)/√2 ⊗ |0⟩ = (|00⟩ + |10⟩)/√2
After CNOT: (|00⟩ + |11⟩)/√2 = |Φ⁺⟩
```

---

**All Four Bell States:**

```python
# |Φ⁺⟩ = (|00⟩ + |11⟩)/√2
qc1 = QuantumCircuit(2)
qc1.h(0)
qc1.cx(0, 1)

# |Φ⁻⟩ = (|00⟩ - |11⟩)/√2
qc2 = QuantumCircuit(2)
qc2.h(0)
qc2.z(0)
qc2.cx(0, 1)

# |Ψ⁺⟩ = (|01⟩ + |10⟩)/√2
qc3 = QuantumCircuit(2)
qc3.h(0)
qc3.x(1)
qc3.cx(0, 1)

# |Ψ⁻⟩ = (|01⟩ - |10⟩)/√2
qc4 = QuantumCircuit(2)
qc4.h(0)
qc4.z(0)
qc4.x(1)
qc4.cx(0, 1)
```

**Properties of Bell States:**
- Maximally entangled
- Orthonormal basis for two qubits
- Measurement outcomes are perfectly correlated
- Foundation for quantum communication protocols

---

### 🌆 Afternoon Session: Hands-on Labs (2.5 hours)

#### Lab 6: Building Quantum Circuits (45 mins)

**Part A: Single-Qubit Gate Exploration**

```python
from qiskit import QuantumCircuit, transpile
from qiskit_aer import AerSimulator
from qiskit.visualization import plot_histogram, plot_bloch_multivector
from qiskit.quantum_info import Statevector
import matplotlib.pyplot as plt

simulator = AerSimulator()

# Test each gate
gates = ['x', 'y', 'z', 'h', 's', 't']

for gate_name in gates:
    # Create circuit
    qc = QuantumCircuit(1, 1)
    getattr(qc, gate_name)(0)  # Apply gate dynamically
    qc.measure(0, 0)
    
    # Simulate
    job = simulator.run(transpile(qc, simulator), shots=1000)
    counts = job.result().get_counts()
    
    # Visualize
    print(f"\n{gate_name.upper()} Gate:")
    print(qc.draw(output='text'))
    plot_histogram(counts, title=f'{gate_name.upper()} Gate Results')
    plt.show()
```

---

**Part B: Gate Combinations**

```python
# Experiment: What happens with multiple H gates?
qc = QuantumCircuit(1, 1)
qc.h(0)
qc.h(0)  # Two H gates
qc.measure(0, 0)

job = simulator.run(transpile(qc, simulator), shots=1000)
counts = job.result().get_counts()
print("Two H gates:", counts)  # Should return to |0⟩!

# Experiment: H-Z-H sequence
qc2 = QuantumCircuit(1, 1)
qc2.h(0)
qc2.z(0)
qc2.h(0)
qc2.measure(0, 0)

job = simulator.run(transpile(qc2, simulator), shots=1000)
counts = job.result().get_counts()
print("H-Z-H sequence:", counts)  # Equivalent to X gate!
```

---

**Part C: Phase Gate Effects on Bloch Sphere**

```python
# Visualize phase rotations
fig, axes = plt.subplots(1, 4, figsize=(16, 4),
                         subplot_kw=dict(projection='3d'))

# Base superposition
qc_base = QuantumCircuit(1)
qc_base.h(0)

# Add different phases
circuits = [
    ('|+⟩ (no phase)', qc_base),
    ('S gate', qc_base.copy().compose(QuantumCircuit(1).s(0))),
    ('T gate', qc_base.copy().compose(QuantumCircuit(1).t(0))),
    ('Z gate', qc_base.copy().compose(QuantumCircuit(1).z(0)))
]

for idx, (title, qc) in enumerate(circuits):
    state = Statevector.from_instruction(qc)
    plot_bloch_multivector(state, title=title, ax=axes[idx])

plt.tight_layout()
plt.show()
```

**Observation:** Phase gates rotate the state around the Z-axis of the Bloch sphere.

---

#### Lab 7: Bell State Creation and Analysis (60 mins)

**Part A: Creating the Bell State |Φ⁺⟩**

```python
# Create Bell state circuit
bell_circuit = QuantumCircuit(2, 2)
bell_circuit.h(0)      # Superposition on qubit 0
bell_circuit.cx(0, 1)  # Entangle qubits
bell_circuit.measure([0, 1], [0, 1])

print("Bell State Circuit:")
print(bell_circuit.draw(output='text'))

# Simulate
job = simulator.run(transpile(bell_circuit, simulator), shots=1000)
counts = job.result().get_counts()

print("\nMeasurement Results:")
print(counts)
plot_histogram(counts, title='Bell State |Φ⁺⟩ Measurements')
plt.show()
```

**Expected Results:**
- Approximately 50% |00⟩
- Approximately 50% |11⟩
- **No** |01⟩ or |10⟩ states
- Perfect correlation: both qubits always agree!

---

**Part B: Visualizing Entanglement**

```python
# Visualize the statevector
bell_viz = QuantumCircuit(2)
bell_viz.h(0)
bell_viz.cx(0, 1)

state = Statevector.from_instruction(bell_viz)

print("Statevector:")
print(state)
print("\nProbabilities:")
probs = state.probabilities()
for basis, prob in zip(['|00⟩', '|01⟩', '|10⟩', '|11⟩'], probs):
    print(f"{basis}: {prob:.3f}")

# Visualize on Bloch sphere (both qubits)
plot_bloch_multivector(state, title='Bell State on Bloch Sphere')
plt.show()
```

**Key Insight:** For entangled states, individual qubits don't have well-defined states on the Bloch sphere—only the joint system does.

---

**Part C: Testing Correlation**

```python
# Create circuits to measure in different bases
def measure_bell_state_in_basis(basis='Z'):
    qc = QuantumCircuit(2, 2)
    qc.h(0)
    qc.cx(0, 1)
    
    if basis == 'X':
        qc.h(0)
        qc.h(1)
    elif basis == 'Y':
        qc.sdg(0)
        qc.h(0)
        qc.sdg(1)
        qc.h(1)
    
    qc.measure([0, 1], [0, 1])
    return qc

# Test all three bases
bases = ['Z', 'X', 'Y']
fig, axes = plt.subplots(1, 3, figsize=(15, 4))

for idx, basis in enumerate(bases):
    qc = measure_bell_state_in_basis(basis)
    job = simulator.run(transpile(qc, simulator), shots=1000)
    counts = job.result().get_counts()
    
    plot_histogram(counts, title=f'Bell State in {basis} Basis', ax=axes[idx])

plt.tight_layout()
plt.show()
```

**Discovery:** Perfect correlation exists in **all** measurement bases!

---

#### Lab 8: Circuit Debugging Exercise (30 mins)

**Debugging Challenge: Find the Errors**

```python
# Buggy Circuit 1
qc_bug1 = QuantumCircuit(2, 2)
qc_bug1.h(0)
qc_bug1.cx(1, 0)  # ❌ Control and target swapped!
qc_bug1.measure([0, 1], [0, 1])

# What state does this create?
```

<details>
<summary>Solution</summary>

The CNOT control and target are reversed. This creates a different entangled state. Correct version:
```python
qc_fixed1 = QuantumCircuit(2, 2)
qc_fixed1.h(0)
qc_fixed1.cx(0, 1)  # ✅ Correct: qubit 0 controls qubit 1
qc_fixed1.measure([0, 1], [0, 1])
```
</details>

---

```python
# Buggy Circuit 2
qc_bug2 = QuantumCircuit(2, 2)
qc_bug2.x(0)
qc_bug2.cx(0, 1)
qc_bug2.measure([0, 1], [0, 1])

# What's missing?
```

<details>
<summary>Solution</summary>

Missing the Hadamard gate! This creates |11⟩, not a Bell state. Correct version:
```python
qc_fixed2 = QuantumCircuit(2, 2)
qc_fixed2.h(0)      # ✅ Add Hadamard for superposition
qc_fixed2.x(1)      # Start qubit 1 in |1⟩
qc_fixed2.cx(0, 1)
qc_fixed2.measure([0, 1], [0, 1])
# Creates |Ψ⁺⟩ = (|01⟩ + |10⟩)/√2
```
</details>

---

```python
# Buggy Circuit 3
qc_bug3 = QuantumCircuit(2, 2)
qc_bug3.h(0)
qc_bug3.h(1)
qc_bug3.cx(0, 1)
qc_bug3.measure([0, 1], [0, 1])

# Is this entangled?
```

<details>
<summary>Analysis</summary>

This creates a **separable** state, not entangled! The extra H gate on qubit 1 disrupts entanglement. Results show all four outcomes (|00⟩, |01⟩, |10⟩, |11⟩) with equal probability.
</details>

---

#### Lab 9: Case Study - Bell State Generator (15 mins)

**Complete Implementation:**

```python
class BellStateGenerator:
    """
    A reusable class for generating and analyzing Bell states
    """
    def __init__(self):
        self.simulator = AerSimulator()
    
    def create_bell_state(self, bell_type='phi_plus'):
        """
        Create one of the four Bell states
        
        Args:
            bell_type: 'phi_plus', 'phi_minus', 'psi_plus', or 'psi_minus'
        """
        qc = QuantumCircuit(2, 2)
        
        if bell_type == 'phi_plus':
            # |Φ⁺⟩ = (|00⟩ + |11⟩)/√2
            qc.h(0)
            qc.cx(0, 1)
        
        elif bell_type == 'phi_minus':
            # |Φ⁻⟩ = (|00⟩ - |11⟩)/√2
            qc.h(0)
            qc.z(0)
            qc.cx(0, 1)
        
        elif bell_type == 'psi_plus':
            # |Ψ⁺⟩ = (|01⟩ + |10⟩)/√2
            qc.h(0)
            qc.x(1)
            qc.cx(0, 1)
        
        elif bell_type == 'psi_minus':
            # |Ψ⁻⟩ = (|01⟩ - |10⟩)/√2
            qc.h(0)
            qc.z(0)
            qc.x(1)
            qc.cx(0, 1)
        
        return qc
    
    def measure_and_visualize(self, qc, title, shots=1000):
        """Measure circuit and create visualization"""
        # Add measurements
        qc_measured = qc.copy()
        qc_measured.measure([0, 1], [0, 1])
        
        # Simulate
        job = self.simulator.run(transpile(qc_measured, self.simulator), 
                                 shots=shots)
        counts = job.result().get_counts()
        
        # Print results
        print(f"\n{title}")
        print("=" * 50)
        print(qc.draw(output='text'))
        print(f"\nMeasurement Results ({shots} shots):")
        for outcome, count in sorted(counts.items()):
            percentage = (count / shots) * 100
            print(f"  {outcome}: {count:4d} ({percentage:5.1f}%)")
        
        # Visualize
        plot_histogram(counts, title=title)
        plt.show()
        
        return counts
    
    def compare_all_bell_states(self):
        """Create and compare all four Bell states"""
        bell_types = ['phi_plus', 'phi_minus', 'psi_plus', 'psi_minus']
        titles = ['|Φ⁺⟩', '|Φ⁻⟩', '|Ψ⁺⟩', '|Ψ⁻⟩']
        
        fig, axes = plt.subplots(2, 2, figsize=(12, 10))
        axes = axes.flatten()
        
        for idx, (bell_type, title) in enumerate(zip(bell_types, titles)):
            qc = self.create_bell_state(bell_type)
            qc.measure([0, 1], [0, 1])
            
            job = self.simulator.run(transpile(qc, self.simulator), 
                                     shots=1000)
            counts = job.result().get_counts()
            
            plot_histogram(counts, title=title, ax=axes[idx])
        
        plt.tight_layout()
        plt.show()

# Usage
generator = BellStateGenerator()

# Create and test Φ⁺ state
bell_phi_plus = generator.create_bell_state('phi_plus')
generator.measure_and_visualize(bell_phi_plus, 'Bell State |Φ⁺⟩')

# Compare all four
generator.compare_all_bell_states()
```

---

#### Lab 10: Mini Quiz - Interactive Assessment (20 mins)

**Question 1: Gate Identification**

Which gate creates equal superposition from |0⟩?
- A) X gate
- B) Z gate
- C) H gate ✅
- D) CNOT gate

**Question 2: Entanglement**

What makes a state entangled?
- A) It has multiple qubits
- B) It cannot be written as a product of single-qubit states ✅
- C) It uses a CNOT gate
- D) It has equal measurement probabilities

**Question 3: Bell State Analysis**

For the Bell state (|00⟩ + |11⟩)/√2, what is the probability of measuring |01⟩?
- A) 0% ✅
- B) 25%
- C) 50%
- D) 100%

**Question 4: Circuit Construction**

To create the Bell state, which sequence is correct?
- A) CNOT then H
- B) H then CNOT ✅
- C) Two H gates
- D) X then CNOT

**Question 5: Phase Gates**

What is the effect of the S gate on |1⟩?
- A) |0⟩
- B) i|1⟩ ✅
- C) -|1⟩
- D) |+⟩

**Question 6: Multi-Qubit Systems**

How many basis states does a 3-qubit system have?
- A) 3
- B) 6
- C) 8 ✅
- D) 9

**Question 7: Measurement**

After measuring a Bell state and getting |00⟩, what is the state now?
- A) Still (|00⟩ + |11⟩)/√2
- B) |00⟩ ✅
- C) |11⟩
- D) Cannot determine

**Question 8: Gate Properties**

Which gate is its own inverse (XX = I)?
- A) All Pauli gates ✅
- B) Only X gate
- C) S gate
- D) T gate

---

### 📝 Day 2 Reflection Questions

1. How does entanglement differ from classical correlation?
2. Why is the Hadamard gate fundamental to quantum algorithms?
3. What role does phase play in quantum interference?
4. How would you explain Bell states to someone without a physics background?

---

## 🛠️ Complete Setup Instructions

### Option 1: Google Colab (Recommended for Beginners)

**Advantages:**
- No installation required
- Free GPU access
- Automatic package management
- Easy sharing and collaboration

**Steps:**
1. Visit [colab.research.google.com](https://colab.research.google.com/)
2. Sign in with Google account
3. File → New Notebook
4. Install Qiskit:
```python
!pip install qiskit qiskit-aer matplotlib numpy --quiet
```
5. Start coding!

---

### Option 2: Local Python Installation

**Requirements:**
- Python 3.8 or higher
- pip package manager
- 4GB RAM minimum
- Internet connection

**Installation Steps:**

**Windows:**
```bash
# Open Command Prompt or PowerShell

# Create virtual environment
python -m venv quantum_workshop
quantum_workshop\Scripts\activate

# Install packages
pip install qiskit qiskit-aer matplotlib numpy jupyter ipython

# Launch Jupyter
jupyter notebook
```

**Mac/Linux:**
```bash
# Open Terminal

# Create virtual environment
python3 -m venv quantum_workshop
source quantum_workshop/bin/activate

# Install packages
pip install qiskit qiskit-aer matplotlib numpy jupyter ipython

# Launch Jupyter
jupyter notebook
```

---

### Option 3: IBM Quantum Lab (Cloud-based)

**Advantages:**
- Access to real quantum hardware
- Pre-configured environment
- Saved notebooks in cloud
- No local installation

**Steps:**
1. Visit [quantum-computing.ibm.com](https://quantum-computing.ibm.com/)
2. Create free IBM account
3. Navigate to Quantum Lab
4. Create new notebook
5. Start coding (Qiskit pre-installed!)

---

### Verification Script

Run this to verify your setup:

```python
# Test script to verify installation
print("Testing Qiskit Installation")
print("=" * 50)

# Import test
try:
    import qiskit
    print(f"✅ Qiskit version: {qiskit.__version__}")
except ImportError:
    print("❌ Qiskit not installed")

try:
    from qiskit_aer import AerSimulator
    print("✅ Aer Simulator available")
except ImportError:
    print("❌ Aer Simulator not available")

try:
    import matplotlib.pyplot as plt
    print("✅ Matplotlib available")
except ImportError:
    print("❌ Matplotlib not installed")

try:
    import numpy as np
    print(f"✅ NumPy version: {np.__version__}")
except ImportError:
    print("❌ NumPy not installed")

# Quick functionality test
try:
    from qiskit import QuantumCircuit
    qc = QuantumCircuit(1)
    qc.h(0)
    print("✅ Can create quantum circuits")
    
    simulator = AerSimulator()
    from qiskit import transpile
    job = simulator.run(transpile(qc, simulator), shots=100)
    result = job.result()
    print("✅ Can run simulations")
    
    from qiskit.visualization import plot_histogram
    print("✅ Visualization tools working")
    
    print("\n🎉 All tests passed! You're ready to go!")
    
except Exception as e:
    print(f"❌ Error during test: {e}")
```

---

## 📚 Resources and References

### Official Documentation
- **Qiskit Textbook**: [qiskit.org/learn](https://qiskit.org/learn) - Comprehensive free textbook
- **Qiskit Documentation**: [qiskit.org/documentation](https://qiskit.org/documentation) - API reference
- **IBM Quantum**: [quantum-computing.ibm.com](https://quantum-computing.ibm.com/) - Cloud quantum computers

### Video Tutorials
- **Qiskit YouTube Channel**: [youtube.com/c/qiskit](https://www.youtube.com/c/qiskit)
- **Coding with Qiskit**: Video series for beginners
- **IBM Quantum Seminars**: Advanced topics and research

### Community
- **Qiskit Slack**: [qiskit.slack.com](https://qiskit.slack.com) - Ask questions, get help
- **Qiskit GitHub**: [github.com/Qiskit](https://github.com/Qiskit) - Source code, issues
- **Stack Overflow**: Tag questions with `qiskit`

### Books
- **"Quantum Computation and Quantum Information"** by Nielsen & Chuang - The standard textbook
- **"Dancing with Qubits"** by Robert Sutor - Beginner-friendly introduction
- **"Programming Quantum Computers"** by Johnston, Harrigan & Gimeno-Segovia

### Research Papers
- Original Bell paper (1964): "On the Einstein Podolsky Rosen Paradox"
- Shor's Algorithm (1994): Polynomial-time quantum algorithm for factoring
- Grover's Algorithm (1996): Quantum search algorithm

### Workshop Materials
- [Day 1 Presentation](http://loyola0.netlify.app/)
- [Day 2 Presentation](https://loyola1.netlify.app/)
- [Quantum Computing Notes (PDF)](https://drive.google.com/file/d/1MvAUtJ7jURzMa5qLPwOwmgTgf_1UnBHm/view?usp=sharing)

---

## 🎓 Learning Path After This Workshop

### Immediate Next Steps (Week 1-2)
1. Complete all lab exercises independently
2. Experiment with different gate combinations
3. Create 2-3 qubit circuits
4. Read Qiskit Textbook Chapters 1-3

### Short Term (Month 1-2)
1. Learn quantum algorithms:
   - Deutsch-Jozsa algorithm
   - Bernstein-Vazirani algorithm
   - Simon's algorithm
2. Understand quantum Fourier transform
3. Study Grover's search algorithm
4. Implement superdense coding

### Medium Term (Month 3-6)
1. Study Shor's factoring algorithm
2. Learn about quantum error correction
3. Explore variational quantum algorithms (VQE, QAOA)
4. Run circuits on real quantum hardware
5. Participate in quantum hackathons

### Advanced Topics (6+ months)
1. Quantum machine learning
2. Quantum cryptography protocols
3. Topological quantum computing
4. Quantum simulation of molecules
5. Contribute to open-source quantum projects

---

## 💡 Tips for Success

### Learning Strategies
- **Practice Daily**: Even 20 minutes of practice is valuable
- **Visualize Everything**: Use Bloch spheres and circuit diagrams extensively
- **Start Simple**: Master single-qubit gates before multi-qubit systems
- **Ask Questions**: Use Slack, forums, and office hours
- **Teach Others**: Best way to solidify your understanding

### Common Pitfalls to Avoid
- **Don't memorize matrices**: Focus on understanding what gates do
- **Measurement matters**: Remember that measurement collapses superposition
- **Qubit ordering**: Pay attention to which qubit is control/target
- **Classical intuition fails**: Embrace quantum weirdness
- **Don't skip visualization**: It's crucial for understanding

### Debugging Quantum Circuits
1. **Print the circuit**: Use `print(qc.draw())`
2. **Check statevectors**: Verify states before measurement
3. **Use barriers**: Organize complex circuits
4. **Test incrementally**: Add gates one at a time
5. **Visualize on Bloch sphere**: Catch phase errors early

---

## 🏆 Challenge Projects

### Beginner Projects
1. **Quantum Coin Flip**: True random number generator
2. **Quantum Password Generator**: Use quantum randomness
3. **State Comparison Tool**: Compare any two single-qubit states

### Intermediate Projects
1. **Bell State Tester**: Verify entanglement correlations
2. **Quantum Teleportation**: Implement the protocol
3. **Superdense Coding**: Send 2 classical bits with 1 qubit
4. **GHZ State Generator**: Create 3-qubit entanglement

### Advanced Projects
1. **Grover Search**: Find an element in unsorted database
2. **Quantum Fourier Transform**: Build QFT circuit
3. **Error Correction**: Implement bit-flip code
4. **Variational Eigensolver**: Find ground state energy

---

## 📧 Contact and Support

### Workshop Instructors
- Questions during workshop: Raise hand or use chat
- Post-workshop questions: [workshop email or forum]

### Technical Support
- **Qiskit Issues**: [github.com/Qiskit/qiskit/issues](https://github.com/Qiskit/qiskit/issues)
- **IBM Quantum Support**: [quantum-computing.ibm.com/support](https://quantum-computing.ibm.com/support)

### Stay Connected
- Join the Qiskit Slack workspace
- Follow @Qiskit on Twitter
- Subscribe to IBM Quantum newsletter
- Attend quantum computing meetups

---

## 📜 License and Attribution

This workshop material is created for educational purposes.

**Tools Used:**
- **Qiskit**: Apache License 2.0
- **IBM Quantum**: Free tier for education
- **Python Libraries**: Various open-source licenses

**Acknowledgments:**
- IBM Quantum for providing free access to quantum computers
- Qiskit development team for excellent documentation
- The quantum computing research community

---

## 🎉 Conclusion

Congratulations on completing this quantum computing workshop! You now have:

- ✅ Solid understanding of quantum mechanics fundamentals
- ✅ Hands-on experience with Qiskit
- ✅ Ability to build and analyze quantum circuits
- ✅ Foundation for advanced quantum algorithms
- ✅ Resources to continue learning independently

**Remember:** Quantum computing is a journey, not a destination. Keep experimenting, stay curious, and don't be afraid to make mistakes!

---

### Quick Reference Card

**Essential Qiskit Commands:**
```python
# Create circuit
qc = QuantumCircuit(num_qubits, num_classical_bits)

# Single-qubit gates
qc.x(0)   # NOT gate
qc.h(0)   # Hadamard
qc.z(0)   # Phase flip
qc.s(0)   # S gate (90° phase)
qc.t(0)   # T gate (45° phase)

# Two-qubit gate
qc.cx(0, 1)  # CNOT (control=0, target=1)

# Measurement
qc.measure(qubit, classical_bit)
qc.measure_all()  # Measure all qubits

# Visualization
qc.draw(output='text')  # or 'mpl' for matplotlib
plot_bloch_multivector(statevector)
plot_histogram(counts)

# Simulation
simulator = AerSimulator()
job = simulator.run(transpile(qc, simulator), shots=1000)
result = job.result()
counts = result.get_counts()
```

---

**Happy Quantum Computing! 🚀✨**
