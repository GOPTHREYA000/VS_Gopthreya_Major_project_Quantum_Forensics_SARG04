# 🔐 Quantum-Inspired Digital Watermarking for Forensic Evidence Authentication Using SARG04 Protocol

## 📖 Overview

Digital forensic images are vulnerable to unauthorized modifications, manipulation, and tampering. Ensuring the authenticity and integrity of digital evidence is a major challenge in cybersecurity and forensic investigations.

This project presents a **Quantum-Inspired Digital Watermarking Framework** that combines:

- **SARG04 Quantum Key Distribution (QKD)**
- **Discrete Wavelet Transform (DWT) Watermarking**
- **Secure Watermark Encryption**
- **Forensic Evidence Authentication**
- **Tamper Detection and Integrity Verification**

The framework generates a secure shared key using the SARG04 protocol, encrypts forensic watermark information, embeds the encrypted watermark into an image using DWT, and verifies image authenticity through watermark extraction and decryption.

---

# 🎯 Project Objectives

- Generate secure keys using the SARG04 protocol.
- Encrypt forensic watermark information.
- Embed encrypted watermarks into digital images.
- Extract and recover watermark information.
- Verify image authenticity.
- Detect unauthorized image modifications.
- Preserve image quality after watermark embedding.
- Evaluate robustness against tampering attacks.

---

# 🏗️ System Architecture

```text
Alice
 │
 ▼
SARG04 Key Generation
 │
 ▼
Watermark Creation
 │
 ▼
Watermark Encryption
 │
 ▼
DWT Watermark Embedding
 │
 ▼
Watermarked Image
 │
 ▼
Transmission
 │
 ▼
Bob
 │
 ▼
Watermark Extraction
 │
 ▼
Watermark Decryption
 │
 ▼
Authentication Verification
 │
 ▼
AUTHENTIC / TAMPERED
```

---

# 🔬 Core Technologies Used

## 1️⃣ SARG04 Quantum Key Distribution (QKD)

SARG04 is used to securely generate a shared secret key between Alice and Bob.

### Purpose

- Secure key generation
- Watermark encryption
- Authentication support
- Improved security against interception attacks

### Features

- Quantum-inspired communication
- State-pair based key generation
- Shared secret establishment
- Authentication verification

---

## 2️⃣ Discrete Wavelet Transform (DWT)

DWT is used to embed watermark information in the frequency domain.

### Purpose

- Watermark embedding
- Image decomposition
- Robustness improvement
- Quality preservation

### DWT Sub-bands

```text
LL → Approximation Component

LH → Horizontal Details

HL → Vertical Details

HH → Diagonal Details
```

### Workflow

```text
Original Image
      ↓
DWT
      ↓
HH Band Selection
      ↓
Watermark Embedding
      ↓
Inverse DWT
      ↓
Watermarked Image
```

---

## 3️⃣ XOR-Based Watermark Encryption

The generated SARG04 key is used to encrypt watermark information before embedding.

### Process

```text
Watermark
      +
SARG04 Shared Key
      ↓
XOR Encryption
      ↓
Encrypted Watermark
```

### Benefits

- Lightweight
- Fast
- Secure
- Easy implementation

---

## 4️⃣ Digital Watermarking

Digital watermarking is used to hide authentication information inside forensic images.

### Features

- Invisible watermark
- Integrity verification
- Tamper detection
- Ownership authentication

---

## 5️⃣ Forensic Evidence Authentication

Used to verify whether a digital image has been modified after transmission.

### Authentication Process

```text
Watermarked Image
        ↓
Watermark Extraction
        ↓
Watermark Decryption
        ↓
Authentication Check
        ↓
AUTHENTIC / TAMPERED
```

---

# 🧰 Libraries Used

| Library | Purpose |
|----------|----------|
| NumPy | Numerical computation and matrix operations |
| Pillow (PIL) | Image processing and manipulation |
| OpenCV | Image handling and attack simulation |
| Matplotlib | Data visualization and plotting |
| PyWavelets | DWT and inverse DWT operations |
| Scikit-Image | SSIM calculation and image datasets |
| Random | SARG04 state generation |

---

# ⚙️ Algorithms Implemented

## SARG04 Key Generation

Functions:

```python
generate_quantum_states()

generate_state_pairs()

shared_key_generation()
```

Purpose:

- Generate a secure shared secret key.

---

## Watermark Encryption

Functions:

```python
encrypt_watermark()

decrypt_watermark()
```

Purpose:

- Protect watermark information before embedding.

---

## DWT Watermark Embedding

Functions:

```python
pywt.dwt2()

pywt.idwt2()
```

Purpose:

- Embed watermark into image frequency coefficients.

---

## Authentication Verification

Functions:

```python
watermark_comparison()

similarity_calculation()
```

Purpose:

- Verify integrity and authenticity.

---

# 🚀 Project Workflow

## Stage 1 – SARG04 Key Generation

- Quantum state generation
- State pair generation
- Alice-Bob communication
- Shared key creation
- Authentication verification

---

## Stage 2 – Watermark Creation & Encryption

- Create forensic watermark
- Binary conversion
- XOR encryption using SARG04 key
- Watermark preparation

---

## Stage 3 – DWT Watermark Embedding

- DWT decomposition
- HH-band selection
- Encrypted watermark embedding
- Image reconstruction
- Watermarked image generation

---

## Stage 4 – Watermark Extraction & Authentication

- Watermark extraction
- Watermark recovery
- Watermark decryption
- Integrity verification
- Authentication decision

---

## Stage 5 – Tampering Detection

Simulated attacks:

- Gaussian Noise
- Salt & Pepper Noise
- JPEG Compression
- Cropping

---

## Stage 6 – Robustness Evaluation

Metrics:

- PSNR
- SSIM
- BER (Bit Error Rate)
- Similarity Analysis

---

## Stage 7 – Results & Analysis

- Performance evaluation
- Authentication analysis
- Tamper detection analysis
- Final conclusions

---

# 📊 Evaluation Metrics

## PSNR (Peak Signal-to-Noise Ratio)

Measures image quality degradation after watermark embedding.

### Formula

```text
PSNR = 20 log10(MAX / √MSE)
```

### Interpretation

```text
Higher PSNR → Better Image Quality
```

---

## SSIM (Structural Similarity Index)

Measures structural similarity between images.

### Range

```text
0 to 1
```

### Interpretation

```text
Closer to 1 → Better Similarity
```

---

## Similarity Score

Measures watermark recovery accuracy.

### Interpretation

```text
100% → Perfect Recovery
```

---

# 📈 Experimental Results

| Metric | Result |
|----------|----------|
| Protocol | SARG04 |
| Watermarking Technique | DWT |
| Encryption Method | XOR Encryption |
| PSNR | 68.64 dB |
| SSIM | 0.9999 |
| Watermark Recovery | Successful |
| Authentication | Successful |
| Image Quality | Excellent |

---

# 🔒 Security Features

- SARG04-based secure key generation
- Shared secret key authentication
- Watermark encryption
- Secure watermark embedding
- Integrity verification
- Tamper detection framework
- Quantum-inspired security architecture

---
