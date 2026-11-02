# 💧 Drop-Drop (DD)

> **Secure, instant, code-authenticated file distribution pipelines.**

Drop-Drop (DD) is an open-source data sharing platform designed to instantly stream high-volume files from a single producer to up to 70 simultaneous consumers using a compressed 6-digit access code.

---

## 🎯 Overview & Problem Statement

Sharing large files often requires creating accounts, uploading to public cloud storage, generating long cumbersome links, and dealing with permission toggles. 

**Drop-Drop** simplifies this process into a zero-friction pipeline:
1. **Producer** selects payload data (up to **5 GB**) and clicks **Send**.
2. **System** generates a secure cryptographic hash mapping to an ephemeral **6-digit code**.
3. **Consumers** input the 6-digit code to join the pipeline and download the files.

---

## ⚡ Key System Capabilities & Constraints

| Feature | Specification | Description |
| :--- | :--- | :--- |
| **Max Payload Size** | `5 GB` per pipeline | Supports large media assets, archives, and datasets |
| **Consumer Capacity** | Up to `70` consumers | Atomic concurrency control strictly limits concurrent stream access |
| **Access Key** | `6-Digit Code` | Ephemeral, compressed short-code resolved via key-value store |
| **Data Lifecycle** | Auto-expiring (TTL) | Temporary storage pipelines self-terminate after completion or TTL |

---

## 🏗 High-Level System Architecture
