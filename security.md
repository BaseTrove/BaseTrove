# 🛡️ Security

---

## Smart Contract Audit

The BaseTrove smart contracts are audited by an independent security firm before launch. The full report is published publicly.

> Audit report: **[Published at launch]**

An audit reduces risk — it does not eliminate it. Never invest more than you can afford to lose.

---

## Contract Architecture

| Contract | Function |
|---|---|
| **TROVE Token** | ERC-20 with dynamic 2–5% DEX fee routing |
| **Vault** | Holds ETH, calculates floor price, processes burns |
| **Buyback Engine** | Receives mining revenue, splits 50/50, executes LP buybacks |

All contracts are verified and open-source on Basescan.

---

## What the Team Can and Cannot Do

### Cannot do (immutable):
- Withdraw ETH from the Vault
- Change the floor price formula
- Mint new $TROVE tokens
- Modify buyback logic
- Set fee above the on-chain maximum

### Can do (operational):
- Adjust swap fee within the allowed range
- Update the development wallet address
- Pause the DApp frontend (not the contracts)
- Execute mining revenue deposits

The Vault and its ETH are untouchable by anyone, including the team.

---

## Liquidity Lock

The TROVE/ETH Uniswap v2 pool is locked via a third-party locker for a minimum of **12 months** from launch. Verifiable on-chain.

> Lock proof: [View on UNCX](https://app.uncx.network/lockers/univ2/chain/8453/address/0x7eb0d66652f8e6e94b9ddf989642312c6333c7b8/lock/1521)

---

## No Team Tokens

There are no team tokens to lock, vest, or dump. Zero. The team's only financial interest in $TROVE is through swap fee revenue — the same mechanism that benefits the Vault and all holders.

---

## Responsible Disclosure

Found a vulnerability? Contact us privately before going public:

> **Telegram:** [t.me/BaseTrove](https://t.me/BaseTrove)

---

## Community & Links

| | |
|---|---|
| **Website** | [basetrove.net](https://basetrove.net) |
| **Docs** | [docs.basetrove.net](https://docs.basetrove.net) |
| **Telegram** | [t.me/BaseTrove](https://t.me/BaseTrove) |
| **Twitter/X** | [x.com/BaseTrove](https://x.com/BaseTrove) |

---

## Known Risks

| Risk | Mitigation |
|---|---|
| Smart contract bug | Independent audit, conservative architecture |
| Mining hardware failure | Redundant units, battery backup for 24/7 uptime |
| Mining coin price decline | Profit-switching to most profitable algorithm at all times |
| Liquidity thin periods | Vault floor provides hard support; floor arb keeps price anchored |
| Fee set too high | Team incentivized to keep fees reasonable — high fees kill volume and team revenue |
| Regulatory | Operating in compliant jurisdictions; legal review of token structure |

No project is risk-free. BaseTrove is built to minimize protocol-level risk through immutability and transparency — but market and operational risks remain.
