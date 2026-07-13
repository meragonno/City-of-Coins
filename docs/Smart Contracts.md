# 🛡️ Smart Contracts

This repository integrates the deBridge Widget as part of the City of Coins liquidity routing platform.
The underlying smart contracts are maintained and deployed by the deBridge team and are not developed or modified in this repository.

## 🔗 Official Contract Sources

- [deBridge Contracts Repository](https://github.com/debridge-finance/debridge-contracts-v1)
- [deBridge Contract Adresses](https://docs.debridge.com/dln-details/overview/deployed-contracts)
- [Smart Contract Security Audits](https://github.com/debridge-finance/debridge-security)

## 🧩 Integration Model

City of Coins uses the deBridge Widget integration model. The frontend loads the official widget, which communicates with deBridge infrastructure and deployed smart contracts managed by the protocol.

```
City of Coins Frontend
↓
deBridge Widget
↓
deBridge Protocol
↓
Official deBridge Smart Contracts
```

## ✅ Included in This Repository

- Frontend integration code 

- UI logic 

- Widget initialization scripts 

- Documentation

## ❌ Not Included

- deBridge Solidity source code 

- deBridge deployment scripts 

- Protocol-owned infrastructure 

- Private keys or administrative credentials

## 📋 Audit Information

Audit reports for the underlying deBridge protocol are available in the official deBridge security repository:

- https://github.com/debridge-finance/debridge-security

## ⚠️ Disclaimer

City of Coins operates as a non-custodial liquidity routing frontend. All cross-chain swap execution and smart contract interactions are performed through the official deBridge protocol infrastructure.
