# Quantum-Inspired Digital Watermarking for Forensic Evidence Authentication Using SARG04 Protocol

## 📌 Project Overview

Digital forensic evidence is highly vulnerable to unauthorized modifications, manipulation, and tampering. Ensuring the authenticity and integrity of digital images is a critical challenge in forensic investigations.

This project proposes a **Quantum-Inspired Digital Watermarking Framework** that combines **SARG04 Quantum Key Distribution (QKD)** with **Discrete Wavelet Transform (DWT) Watermarking** to provide secure forensic evidence authentication.

The system generates a secure shared secret key using the SARG04 protocol, encrypts forensic watermark information, embeds the encrypted watermark into an image, and later verifies image authenticity through watermark extraction and decryption.

---

## 🎯 Objectives

- Generate secure cryptographic keys using the SARG04 protocol.
- Encrypt forensic watermark information.
- Embed encrypted watermarks into forensic images using DWT.
- Extract and decrypt watermarks at the receiver side.
- Authenticate forensic evidence.
- Detect unauthorized image modifications.
- Evaluate image quality using PSNR and SSIM metrics.
- Analyze robustness against image tampering attacks.

---

## 🏗️ System Architecture

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
