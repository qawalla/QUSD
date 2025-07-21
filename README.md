# QUSD – Qawalla USD Stablecoin

**QUSD** is Qawalla’s foundational stablecoin, pegged 1:1 to the U.S. Dollar and deployed on the Base blockchain. This project provides a secure, centralized ERC-20 compliant smart contract for managing issuance and redemption of USD-backed digital tokens.

> ⚠️ This repository is in early development and not yet open source. Smart contract deployment is currently restricted to the Base testnet for internal testing.

---

## 🌐 Overview

QUSD is designed to be:
- ✅ **Dollar-backed**: Fully collateralized by off-chain USD reserves
- ✅ **Compliant**: Role-based minting, burning, and pausing controls
- ✅ **Efficient**: Lightweight and upgradeable with ERC-20 compatibility
- ✅ **Base-first**: Developed for Base L2 for scalability and low fees

---

## 🔧 Contract Features

| Feature         | Description |
|----------------|-------------|
| ERC-20 Token    | Fully compliant with OpenZeppelin standards |
| Role-Based Access | Separate roles for minting, burning, pausing |
| Pause Mechanism | Transfers can be paused in emergencies |
| Transparent Events | Emits logs for all key actions (mint, burn, pause) |
| Upgrade-Ready | (Optional) via proxy architecture (future phase) |

---

## 📦 Project Structure

