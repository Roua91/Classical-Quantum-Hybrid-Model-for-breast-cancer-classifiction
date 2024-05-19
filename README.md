# Projects

### Angle Encoding and Mathematical Representation in Quantum Circuits

Angle encoding is a method of embedding classical data into quantum states by using data values as angles for rotation operations on qubits. This approach leverages the trigonometric properties of quantum states to represent classical information.

#### Angle Encoding

**Concept**:
Angle encoding maps each classical data point \( x_i \) to the angle of a quantum gate, typically a rotation around the Y-axis (RY gate). This encoding transforms classical data into quantum states by rotating qubits from their initial state \( |0\rangle \).

**Mathematical Representation**:
For a classical data point \( x_i \), the corresponding quantum state after applying an RY gate is:

R_y(x_i) |0\rangle = \cos\left(\frac{x_i}{2}\right) |0\rangle + \sin\left(\frac{x_i}{2}\right) |1\rangle



The rotation matrix \( R_y(\theta) \) is given by:

\[
R_y(\theta) = \begin{pmatrix}
\cos\left(\frac{\theta}{2}\right) & -\sin\left(\frac{\theta}{2}\right) \\
\sin\left(\frac{\theta}{2}\right) & \cos\left(\frac{\theta}{2}\right)
\end{pmatrix}
\]


### Application in Quantum Circuits

#### 1. Simple Quantum Circuit (SQC)

**Angle Encoding in SQC**:
In the SQC, each classical data point \( x_i \) is encoded as an angle for an RY gate applied to an initial qubit state. The process involves initializing the qubit to a superposition state using a Hadamard gate and then applying the RY rotations.

**Circuit Structure**:
```
0: ──H──RY(θ₁)──RY(θ₂)──RY(θ₃)──<Z>
1: ──H──RY(θ₄)──RY(θ₅)──RY(θ₆)──<Z>
2: ──H──RY(θ₇)──RY(θ₈)──RY(θ₉)──<Z>
3: ──H──RY(θ₁₀)──RY(θ₁₁)──RY(θ₁₂)──<Z>
```

**Mathematical Representation**:
For each qubit \( q_i \), the encoding process can be written as:
|q_i\rangle = R_y(\theta_i) H |0\rangle

where 

H |0\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}}

and 

R_y(\theta_i) \frac{|0\rangle + |1\rangle}{\sqrt{2}} = \cos\left(\frac{\theta_i}{2}\right) \frac{|0\rangle + |1\rangle}{\sqrt{2}} + \sin\left(\frac{\theta_i}{2}\right) \frac{|1\rangle - |0\rangle}{\sqrt{2}}


#### 2. Entangled Quantum Circuit (EQC)

**Angle Encoding in EQC**:
The EQC enhances the SQC by introducing entanglement between qubits after angle encoding. Each classical data point is still encoded as an angle for an RY gate, but entanglement is introduced using CNOT gates.

**Circuit Structure**:
```
0: ──H──RY(θ₁)──RY(θ₂)──X──<Z>
1: ──H──RY(θ₃)──RY(θ₄)──X──<Z>
2: ──H──RY(θ₅)──RY(θ₆)──X──<Z>
3: ──H──RY(θ₇)──RY(θ₈)──X──<Z>
```

**Mathematical Representation**:
For each pair of qubits \( (q_i, q_j) \), the encoding process with entanglement can be represented as:
|q_i\rangle = R_y(\theta_i) H |0\rangle

and 

|q_j\rangle = R_y(\theta_j) H |0\rangle

then 

|q_i, q_j\rangle = \text{CNOT}(R_y(\theta_i) H |0\rangle \otimes R_y(\theta_j) H |0\rangle)


This creates an entangled state that reflects the correlations between the encoded data points.

#### 3. Advanced Quantum Circuit (AQC)

**Angle Encoding in AQC**:
The AQC extends the EQC by adding phase shift gates (RZ gates) and deeper entanglement patterns using additional controlled-Z gates. This setup allows for more complex and richer data representations.

**Circuit Structure**:
```
0: ──H──RY(θ₁)──RY(θ₂)──RZ(θ₃)──X──Z──<Z>
1: ──H──RY(θ₄)──RY(θ₅)──RZ(θ₆)──X──Z──<Z>
2: ──H──RY(θ₇)──RY(θ₈)──RZ(θ₉)──X──Z──<Z>
3: ──H──RY(θ₁₀)──RY(θ₁₁)──RZ(θ₁₂)──X──Z──<Z>
```

**Mathematical Representation**:
For each qubit \( q_i \) with an additional phase shift, the encoding can be described as:

|q_i\rangle = R_z(\phi_i) R_y(\theta_i) H |0\rangle

Where

H |0\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}}


and 

R_y(\theta_i) \frac{|0\rangle + |1\rangle}{\sqrt{2}} = \cos\left(\frac{\theta_i}{2}\right) \frac{|0\rangle + |1\rangle}{\sqrt{2}} + \sin\left(\frac{\theta_i}{2}\right) \frac{|1\rangle - |0\rangle}{\sqrt{2}}

Then 

R_z(\phi_i) \left( \cos\left(\frac{\theta_i}{2}\right) \frac{|0\rangle + |1\rangle}{\sqrt{2}} + \sin\left(\frac{\theta_i}{2}\right) \frac{|1\rangle - |0\rangle}{\sqrt{2}} \right)



When including entanglement, the full state representation for pairs of qubits \( (q_i, q_j) \) is:

|q_i, q_j\rangle = \text{CZ}(R_z(\phi_i) R_y(\theta_i) H |0\rangle \otimes R_z(\phi_j) R_y(\theta_j) H |0\rangle)


### Summary

Angle encoding is a versatile and powerful method for embedding classical data into quantum states. In the described quantum circuits:

- **SQC** uses angle encoding through RY rotations.

|q_i\rangle = R_y(\theta_i) H |0\rangle

- **EQC** builds on SQC's angle encoding and adds entanglement with CNOT gates.

  |q_i, q_j\rangle = \text{CNOT}(R_y(\theta_i) H |0\rangle \otimes R_y(\theta_j) H |0\rangle)

- **AQC** further enhances EQC with additional phase shifts (RZ gates) and deeper entanglement using controlled-Z gates.

  |q_i, q_j\rangle = \text{CZ}(R_z(\phi_i) R_y(\theta_i) H |0\rangle \otimes R_z(\phi_j) R_y(\theta_j) H |0\rangle)


These methods enable the transformation of classical data into quantum states, leveraging the unique properties of quantum computation to potentially improve machine learning performance.
