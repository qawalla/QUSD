# 💵 QUSD – Qawalla USD Stablecoin

**QUSD** is a fully collateralized, dollar-pegged stablecoin issued by Qawalla. Built on Ethereum-compatible networks, QUSD is designed to provide secure, transparent, and composable digital dollars for DeFi, businesses, and payments.

> 🧪 Currently live on **Base Testnet**. Support for **Ethereum Mainnet** and **Polygon PoS** is planned.

---

## 🌍 Overview

QUSD is a centralized stablecoin smart contract system backed 1:1 by U.S. dollar reserves. It is designed to be modular, secure, and easy to integrate across EVM-compatible networks.

### Key Properties
- 🔐 **Permissioned Minting & Burning**  
- 💵 **1:1 USD Backing (off-chain reserves)**  
- 🧩 **ERC-20 Standard** for full wallet and DeFi compatibility  
- 🌉 **Cross-chain ready** via bridges and proxy architectures  
- 🛠️ **Developer Friendly** with clear roles and deployment tools  

---

## 🔧 Smart Contract Features

| Feature           | Description |
|------------------|-------------|
| ERC-20 Base       | Fully compatible with wallets and DeFi protocols |
| Role-based Access | `MINTER`, `PAUSER`, and `ADMIN` roles for safety |
| Mint/Burn Controls| Only authorized minters can issue or redeem QUSD |
| Pause Support     | Transfers can be paused in emergencies |
| Transparent Events| Emits standard events for all key actions |
| Upgradeable Ready | Compatible with proxy patterns (optional) |
| Cross-Chain Ready | Designed for bridging to ETH, Polygon, etc. |

---

## 🧱 Architecture & Roles

### Roles via AccessControl
- `DEFAULT_ADMIN_ROLE`: Contract owner (Qawalla or delegated multisig)
- `MINTER_ROLE`: Authorized fiat issuers
- `PAUSER_ROLE`: Can pause/unpause transfers

### Example Flow
```mermaid
sequenceDiagram
  participant User
  participant Custodian
  participant Contract

  User->>Custodian: Off-chain USD deposit
  Custodian->>Contract: Mint QUSD to User
  User->>Contract: Transfer QUSD on-chain
  User->>Custodian: Request redemption
  Custodian->>Contract: Burn QUSD
  Custodian->>User: Off-chain USD payout
🚀 Deployment
Deployed Networks
Network	Status	Contract Address
Base Testnet	✅ Active	0x... (example)
Ethereum	🔜 Planned	
Polygon	🔜 Planned	

🧪 Getting Started
bash
Copy
Edit
git clone https://github.com/qawalla/QUSD.git
cd QUSD
npm install

# Compile contracts
npx hardhat compile

# Deploy to local or testnet
npx hardhat run scripts/deploy.js --network baseTestnet
See scripts/deploy.js and hardhat.config.js for full configuration.

🌉 Cross-Chain Strategy (Upcoming)
QUSD will support bridging to Ethereum and Polygon via:

LayerZero or Wormhole

Proxy contract support for synced supply

Burn/mint bridge strategy to prevent double-minting

🧠 Use Cases
Stable DeFi trading pairs

Business payments

Tokenized invoicing

Treasury management

Multi-chain ecosystem rewards

🤝 Contributing
Contributions are welcome!
Please fork the repo, open a PR, or suggest ideas via GitHub Issues.

📜 License
MIT License (c) Qawalla LLC
See LICENSE for full terms.

📬 Contact
Website: https://www.qwla.io
Email: team@qwla.io
Twitter: @qwla_io
