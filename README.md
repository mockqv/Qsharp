# Quantum Computation with Q#

This repository contains two programs written in Q#, each exploring different aspects of quantum computing. The first demonstrates qubit allocation and fundamental operators, while the second implements random number generation using quantum principles.

<hr/>

## Qubit Manipulation 

#### **Explanation:**

### **Qubit Allocation:**

```use(q1, q2) = (Qubit(), Qubit());``` creates two qubits q1 and q2 in the |0> state.

Q# ensures that qubits are deallocated at the end of the operation.

### **Hadamard Operator (H):**

- ```H(q1);``` puts q1 in a superposition between |0> and |1>, creating the state (|0> + |1>)/\sqrt{2}.

### **CNOT Gate (Controlled-NOT):**

- ```CNOT(q1, q2);``` creates entanglement between q1 and q2. If q1 is |0>, q2 remains |0>; if q1 is |1>, q2 also becomes |1>.

### **DumpMachine:**

- ```DumpMachine();``` displays the current state of the quantum system for analysis.

### **Measurement and Reset:**

- ```M(q1) and M(q2)``` measure the qubits.

- ```Reset(q1); Reset(q2);``` returns the qubits to the |0\> state.

## **quantumRandomNumberGeneration File: Random Number Generation**

#### **Explanation:**

### **Main Function (Main):**

- Defines max = 100, the upper limit for the random number.

- Calls ```GenerateRandomNumberInRange(max)``` to obtain a random value.

- Generating Random Bits:

- ```GenerateRandomBit()``` uses a qubit initialized in |0\>.

- Applies Hadamard ```(H(q))``` to create superposition, making the measurement ```M(q)``` equally likely to return 0 or 1.

- The qubit is reset after measurement.

- Building the Random Number:

- ```BitSizeI(max)``` determines the number of bits required to represent max.

- A loop collects nBits random bits.

- ```ResultArrayAsInt(bits)``` converts the bit sequence into an integer.

- If the value exceeds max, the function calls itself recursively.

## **📌 Conclusion**

These two programs illustrate fundamental quantum computing concepts:

- Superposition and entanglement using Hadamard and CNOT gates.

- Measurement and reset of qubits.

- Random number generation based on qubits.

