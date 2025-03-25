
![banner](images/banner.png)

# 🧬 Inheritable Smart Contract Wallet Audit

  * **Audit Date:** March 2025
  * **Platform:** [Cyfrin CodeHawks](https://codehawks.cyfrin.io)
  * **Contract Repo:** [Source Code](https://github.com/CodeHawks-Contests/2025-03-inheritable-smart-contract-wallet)
  * **nSLOC:** 211

---

## 📄 Summary

Inheritance of crypto assets in both cold and hot wallets remains a persistent challenge in decentralized finance. This audit focused on the `InheritanceManager` smart contract, which introduces a **time-locked inheritance system** for secure, decentralized, and automated distribution of assets to predefined beneficiaries.

Key features:
- Time-based locks to delay inheritance claims
- Beneficiary management with automatic distribution
- Elimination of intermediaries for estate planning
- Transparent and trustless inheritance mechanism

---

## 🚨 Findings

| Severity | Title | Link |
|----------|-------|------|
| 🔴 | `inherit()` function lacks access control, allowing anyone to become owner | [View Issue](https://codehawks.cyfrin.io/c/2025-03-inheritable-smart-contract-wallet/s/427) |
| 🔴 | Ineffective reentrancy protection due to storage slot mismatch | [View Issue](https://codehawks.cyfrin.io/c/2025-03-inheritable-smart-contract-wallet/s/432) |
| 🔴 | Beneficiaries array management issues lead to incorrect fund distribution | [View Issue](https://codehawks.cyfrin.io/c/2025-03-inheritable-smart-contract-wallet/s/435) |
| 🔴 | The buyOutEstateNFT function has severe logic flaws causing incomplete asset distribution and failed NFT burning | [View Issue](https://codehawks.cyfrin.io/c/2025-03-inheritable-smart-contract-wallet/s/801) |
| 🟠 | Multiple owner-only functions do not reset inheritance deadline, violating core contract invariant | [View Issue](https://codehawks.cyfrin.io/c/2025-03-inheritable-smart-contract-wallet/s/438) |
| 🟢 | createEstateNFT()` overwrites the global `assetToPay` variable for ALL NFTs         | [View Issue](https://codehawks.cyfrin.io/c/2025-03-inheritable-smart-contract-wallet/s/437) |
