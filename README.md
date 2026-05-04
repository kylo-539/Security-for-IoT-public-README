# Security for IoT – AES VS PRESENT (Python)
# Grade: 99%
**Author:** Kyle Sheehy  
**Date:** March 2026

This repository contains Python implementations of two block ciphers used for learning and verification with known‑answer test vectors:

- **AES‑128 (encryption only)** 
- **PRESENT‑80 (encryption only)** 

---

## ⚠️ Source Code Availability

To preserve academic integrity, full source code is not publicly available.

This repository instead provides:

- Processed datasets (CSV)  
- High-resolution visualisations  
- Simulation structure and methodology  
- Analysis outputs and key findings  

Full implementation details are available upon request for professional or academic review.

---

## File Overview

### AES.py
Implements AES‑128 with:
- Byte/State conversions (`toByteArray`, `state_matrix`)
- Key schedule (`key_expansion`, `SubWord`)
- Core round operations (`SubBytes`, `ShiftRows`, `MixColumns`, `AddRoundKey`)
- End‑to‑end encryption and test vector checks (`algorithm`, `FullCodeRun`)

### PRESENT.py
Implements PRESENT‑80 with:
- Key schedule (`generateKeys`)
- S‑box layer (`SBox`)
- Permutation layer (`PermLayer`)
- Round key addition (`addRoundKey`)
- End‑to‑end encryption and test vector checks (`algorithm`)

---

## Cipher Parameters

**AES‑128**
- Block size: 128 bits
- Key size: 128 bits
- Rounds: 10

**PRESENT‑80**
- Block size: 64 bits
- Key size: 80 bits
- Rounds: 31 + final key whitening

---

## AES vs PRESENT (Quick Comparison)

- **Security margin:** AES‑128 is a modern standard with a large security margin; PRESENT‑80 is a lightweight design with a smaller key size.
- **Performance target:** AES is widely accelerated in hardware and software; PRESENT is optimized for constrained devices with limited gates and memory.
- **State size:** AES uses 128‑bit blocks; PRESENT uses 64‑bit blocks.

### Applicable Scenarios

- **AES‑128:** general‑purpose encryption, desktops/servers, mobile devices, and IoT hardware with AES acceleration.
- **PRESENT‑80:** ultra‑constrained IoT/embedded devices where code size, RAM, or gate count is the main constraint.

---

## How to Run

From a terminal (PowerShell / CMD / VS Code terminal):

```bash
python AES.py
```

```bash
python PRESENT.py
```

Each script prints the computed ciphertexts and compares them with the expected test vectors.

---

## Notes

- Implementations are for educational use only.
- These are raw block cipher primitives (no modes of operation or authentication).

---

## 🎓 Educational Value

This project demonstrates:

- Implementation of two block ciphers from formal specifications
- Substitution–Permutation Network (SPN) design and round structure
- Key schedule construction and round key usage
- Byte/nibble manipulation and bit‑level permutations
- Diffusion and confusion via S‑boxes and mixing layers
- Verification using known‑answer test vectors

It highlights trade‑offs between a standard cipher (AES‑128) and a lightweight cipher (PRESENT‑80) for IoT environments.

---

## 📧 Contact

**Kyle Sheehy**  
Course: EEN1059 Security for IoT and Edge Networks  
Institution: DCU

---

## 📄 License

Created for educational purposes as part of university coursework.
