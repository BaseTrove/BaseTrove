# Security

---

## Smart Contract Audit

The BaseTrove smart contracts (Vault, ERC-20, Buyback Engine) are audited by an independent security firm prior to launch. The full audit report is published publicly and linked here at launch.

> Audit report: **[Published at launch]**

An audit reduces risk but does not eliminate it. Even audited contracts can have vulnerabilities. Never invest more than you can afford to lose.

---

## Contract Architecture

BaseTrove consists of three core contracts:

| Contract | Function |
|---|---|
| **TROVE Token** | ERC-20 with 3% DEX tax routing |
| **Vault** | Holds ETH, calculates floor price, processes burns |
| **Buyback Engine** | Receives mining revenue, splits 50/50, executes random LP buys |

All contracts are verified and published on Basescan. Source code is readable by anyone.

---

## What the Team Can and Cannot Do

### Cannot do (non-upgradeable):
- Withdraw ETH from the Vault
- Change the floor price formula
- Increase the tax rate
- Mint new $TROVE tokens
- Modify buyback logic

### Can do (operational):
- Update marketing wallet address (for operational flexibility)
- Pause the DApp frontend (not the contracts)
- Execute mining revenue deposits

The core financial mechanics are immutable once deployed.

---

## Liquidity Lock

Initial liquidity in both pools is locked via a third-party locker for a minimum of **12 months** from launch.

Lock proof: **[Published at launch]**

The team cannot remove liquidity or rug-pull the pools during this period.

---

## Team Token Lock

Team allocation (1,000 TROVE) is locked in a vesting contract:
- 6-month cliff (0 tokens available)
- 24-month linear vesting starting at month 6
- Deployed on-chain, verifiable on Basescan

---

## Responsible Disclosure

If you discover a security vulnerability in BaseTrove's smart contracts or DApp, please report it privately before public disclosure:

> Security contact: **[Published at launch]**

We take security reports seriously and will acknowledge and address valid findings promptly.

---

## Known Risks

| Risk | Mitigation |
|---|---|
| Smart contract bug | Independent audit, conservative architecture |
| Mining hardware failure | Redundant hardware, battery backup |
| BTC price collapse | Protocol functions at any BTC price; lower revenue, not zero |
| Liquidity thin periods | Floor price provides hard support; arb mechanism keeps pools active |
| Regulatory | Legal review of token structure; operating in compliant jurisdictions |

No investment is without risk. BaseTrove is designed to minimize protocol-level risk through transparency and immutability, but market and operational risks remain.
