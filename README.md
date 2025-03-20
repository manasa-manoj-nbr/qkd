# **BB84 Protocol Simulation | Quantum Key Distribution (QKD)**  

🔑 **A Qiskit-based Python simulation of the BB84 quantum key distribution (QKD) protocol.**  
👨‍💻 **Detects eavesdropping and ensures secure communication using quantum mechanics.**  

![QKD Diagram](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2d/BB84.svg/500px-BB84.svg.png)  
*(BB84 Protocol Overview - Alice, Bob, and Eve (Eavesdropper))*  

---

## 🚀 **Project Overview**  
This project implements the **BB84 QKD Protocol** to demonstrate how quantum mechanics ensures **secure key exchange** while detecting potential **eavesdropping attacks**.  

- **Simulates quantum communication** using Qiskit.  
- **Implements eavesdropping (Eve)** and measures errors introduced.  
- **Applies cascade protocol(parity check)** for error correction.  
- **Visualization** Provides bar plots to compare key lengths and error rates.

---
## 🛠 **How It Works**
### **1️⃣ Generate Key & Bases**
- Alice randomly generates a **binary key (0s & 1s)**.
- She selects random **bases** (`1` or `0`) to encode the key.

### **2️⃣ Encode & Send Qubits**
- Alice prepares qubits using Hadamard (`H`) gates for `1`-basis encoding.

### **3️⃣ Bob Measures with Random Bases**
- Bob randomly picks bases & **measures** the qubits.
- If Alice & Bob **chose the same bases**, their bits match.

### **4️⃣ Eavesdropping Attack (Optional)**
- Eve **intercepts & measures** qubits.
- This introduces **errors** in Bob's results.

### **5️⃣ Key Agreement & Error Correction**
- Alice & Bob discard mismatched bases.
- **Parity Check** detects potential errors.
- **Visualization** shows the impact of Eve's attack.

---

## 📊 **Visualization**
### **Bar Chart: Key Length Comparison**  
- **Original Key** (Alice’s initial key)
- **Final Key (Without Eve)** (Alice & Bob’s shared key)
- **Final Key (With Eve)** (Eve's interference effects)

The bar chart helps visualize how **eavesdropping affects secure key generation**.

---

## 📜 **Example Output**  
### With no eavesdropping
noeve.png
```bash
Original Key (Alice and Bob agreed on):  [0 1 1 0 1]
Final Secure Key(No Eave):  [0 1 1 0 1]
Corrected Key(No Eave):  [0 1 1 0 1]
```
### With eavesdropping
[witheve.png]
```bash
Original Key (Alice and Bob agreed on):  [0 0 0 0 1]
Final Secure Key(contains errors):  [1 1 0 0 0]
Corrected Key:  [0 0 0 0 1]
```
---

Happy Quantum Coding! ⚛️🚀

