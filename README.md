# Projects

### Angle Encoding and Mathematical Representation in Quantum Circuits

Angle encoding is a method of embedding classical data into quantum states by using data values as angles for rotation operations on qubits. This approach leverages the trigonometric properties of quantum states to represent classical information.

#### Angle Encoding

**Concept**:
Angle encoding maps each classical data point \( x_i \) to the angle of a quantum gate, typically a rotation around the Y-axis (RY gate). This encoding transforms classical data into quantum states by rotating qubits from their initial state \( |0\rangle \).

**Mathematical Representation**:
For a classical data point \( x_i \), the corresponding quantum state after applying an RY gate is:

![gen1](https://github.com/Roua91/Reaserch_Project/assets/165356652/382fad5c-7880-4c3c-87fa-ec97269f1998)


The rotation matrix \( R_y(\theta) \) is given by:

![gen2](https://github.com/Roua91/Reaserch_Project/assets/165356652/a1a62527-cd41-4624-8263-44891475dda8)



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
![SQC1](https://github.com/Roua91/Reaserch_Project/assets/165356652/62770080-6bb5-492c-b9e8-03ed22f52b60)


where 

![SQC2](https://github.com/Roua91/Reaserch_Project/assets/165356652/be62b9eb-4ed6-4afb-a139-f5a32ffb0d21)


and 

![SQC3](https://github.com/Roua91/Reaserch_Project/assets/165356652/5710c856-5fc9-4046-9903-d561e0e56564)



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

![EQC1](https://github.com/Roua91/Reaserch_Project/assets/165356652/188a45cf-ff3d-487a-9130-3beb816a74c7)


and 

![EQC2](https://github.com/Roua91/Reaserch_Project/assets/165356652/ed14957a-32d6-4e78-926f-366a1836c315)


then 

![EQC3](https://github.com/Roua91/Reaserch_Project/assets/165356652/4ff4ee7e-9296-4ef5-b3ed-3fe2856bd57b)



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

![AQC1](https://github.com/Roua91/Reaserch_Project/assets/165356652/54dbcdb6-b348-4833-9462-08e440379616)


Where

![AQC2](https://github.com/Roua91/Reaserch_Project/assets/165356652/cd92fe25-f82c-441c-a95e-a241c311d1e5)



and 

![AQC3](https://github.com/Roua91/Reaserch_Project/assets/165356652/5e4dc61a-187e-4245-a5de-e503de43943e)


Then 

![AQC4](https://github.com/Roua91/Reaserch_Project/assets/165356652/06103953-0371-4214-850e-2e38651e3e3d)




When including entanglement, the full state representation for pairs of qubits \( (q_i, q_j) \) is:

![AQC5](https://github.com/Roua91/Reaserch_Project/assets/165356652/aaf4a2f8-d85f-4588-93fe-3590664e41d0)



### Summary

Angle encoding is a versatile and powerful method for embedding classical data into quantum states. In the described quantum circuits:

- **SQC** uses angle encoding through RY rotations.

![Sum_SQC](https://github.com/Roua91/Reaserch_Project/assets/165356652/3a10fd4d-3eb4-4c54-a760-d1da1265bd62)


- **EQC** builds on SQC's angle encoding and adds entanglement with CNOT gates.

![Sum_EQC](https://github.com/Roua91/Reaserch_Project/assets/165356652/d3cc43f5-6fff-48ad-be58-f73021a73235)


- **AQC** further enhances EQC with additional phase shifts (RZ gates) and deeper entanglement using controlled-Z gates.

![Sum_AQC](https://github.com/Roua91/Reaserch_Project/assets/165356652/96e63a4b-cf26-4bc6-a31d-92ee983cebf1)



These methods enable the transformation of classical data into quantum states, leveraging the unique properties of quantum computation to potentially improve machine learning performance.
