Quantum Disturbance-Based Photon Cloning Attack (QD-PCA)
What is it?
QD-PCA is an advanced quantum hacking technique designed to exploit vulnerabilities in Quantum Key Distribution (QKD) systems. It combines approximate quantum cloning with controlled quantum disturbances to extract secret key information without being detected.

Unlike traditional quantum attacks that introduce detectable errors, QD-PCA stealthily copies quantum states and injects subtle noise that blends with natural channel noise, thereby maintaining a low Quantum Bit Error Rate (QBER).

How Does It Work?
Imagine a QKD system where Alice sends quantum bits (qubits) to Bob to establish a secret key. Here’s how Eve (the attacker) uses QD-PCA:

Step-by-step:
Interception and Cloning:

Eve intercepts each qubit sent from Alice.

She uses an approximate quantum cloning machine (like the Bužek-Hillery Cloner) to create two imperfect copies.

Eve keeps one copy and forwards the other to Bob.

Controlled Disturbance Injection:

Before sending the qubit to Bob, Eve applies tiny disturbances (e.g., phase shifts, polarization rotation, intensity fluctuations).

These disturbances mimic normal quantum noise, so Bob doesn’t suspect anything.

Avoiding Detection:

By keeping the QBER below the system’s rejection threshold (typically <11%), Eve ensures her presence remains undetected.

Learning Over Time (Adaptive ML):

Over multiple transmissions, Eve uses machine learning to:

Tune the amount of disturbance

Maximize the key extraction fidelity

Minimize the chance of being detected 



**output**



--- Starting QD-PCA Attack Simulation with 500 bits ---

--- Post-processing and Key Reconciliation ---

Alice's Final Key (matching bases) : [np.int32(0), np.int32(1), np.int32(1), np.int32(0), np.int32(0), np.int32(1), np.int32(1), np.int32(0), np.int32(0), np.int32(0), np.int32(0), np.int32(1), np.int32(1), np.int32(1), np.int32(1), np.int32(0), np.int32(0), np.int32(0), np.int32(0), np.int32(0)]...
Bob's Final Key (matching bases)   : [0, 1, 0, 0, 0, 1, 1, 0, 0, 1, 1, 1, 0, 1, 1, 1, 0, 0, 1, 0]...
Eve's Potential Key (matching bases): [0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 1, 1, 1, 1, 1, 0, 0, 1, 0]...

Total matching bits: 244
Errors in shared key : 103
Detected QBER        : 0.422 (Threshold: 0.11)

⚠️ QBER too high. Attack detected! Alice and Bob will abort key exchange.
The disturbance caused by Eve's cloning was significant enough to be noticed.

--- Plotting QBER Results ---
