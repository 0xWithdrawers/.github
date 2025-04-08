![banner](images/banner.png)

# 🧬 Inheritable Smart Contract Wallet Audit

  * **Audit Date:** March 2025
  * **Platform:** [Cyfrin CodeHawks](https://codehawks.cyfrin.io)
  * **Contract Repo:** [Source Code](https://github.com/CodeHawks-Contests/2025-03-rustfund)
  * **nSLOC:** 170

---

## 📄 Summary

RustFund is a decentralized crowdfunding platform built on the Solana blockchain It enables creators to launch fundraising campaigns and contributors to support projects they believe in, all in a trustless and transparent manner.

Key features:
- Create Fundraising Campaigns: Creators can launch campaigns with custom names, descriptions, and funding goals
- Contribute to Projects: Users can contribute SOL to any active campaign
- Refund Mechanism: Contributors can get refunds if deadlines are reached and goals aren't met
- Secure Withdrawals: Creators can withdraw funds once their campaign succeeds

---

## 🚨 Findings

| Severity | Title | Link |
|----------|-------|------|
| 🔴 | Missing Contribution Amount Update | [View Issue](https://codehawks.cyfrin.io/c/2025-03-rustfund/s/348) |
| 🔴 | Lack of campaign success (goal and deadline) verification in withdraw function | [View Issue](https://codehawks.cyfrin.io/c/2025-03-rustfund/s/350) |
| 🟠 | Withdrawal doesn't reset amount_raised, leading to locked funds | [View Issue](https://codehawks.cyfrin.io/c/2025-03-rustfund/s/349) |
| 🟠 | The set_deadline function does not set the dealine_set flag to true | [View Issue](https://codehawks.cyfrin.io/c/2025-03-rustfund/s/333) |
| 🟢 | Refund function allows withdrawals when deadline is not set (deadline = 0) | [View Issue](https://codehawks.cyfrin.io/c/2025-03-rustfund/s/335) |
