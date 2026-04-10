# Taxes & Fees

$TROVE has a simple, low tax structure applied to DEX trades. All taxes flow directly to the Vault or fund operations — there is no staking pool, no reflection, and no complexity.

---

## Tax Structure

| Transaction | Total Tax | Vault | Marketing |
|---|---|---|---|
| **Buy on DEX** | 3% | 1.5% | 1.5% |
| **Sell on DEX** | 3% | 1.5% | 1.5% |
| **Sell to Vault (DApp)** | 0% | — | — |

---

## Vault Tax

**1.5% of every DEX trade** is automatically routed to the Vault in ETH. This compounds with mining revenue to continuously grow the floor price.

On a day with $10,000 of combined trading volume:
```
$10,000 × 1.5% = $150 → Vault
```

On Base chain, where gas costs are negligible, even small trades contribute meaningfully to the Vault without friction.

---

## Marketing Tax

**1.5% of every DEX trade** funds operations and marketing. This covers:

- Smart contract development and maintenance
- Security audits
- Community management
- Exchange listings
- Mining infrastructure operational costs not covered by mining revenue

The marketing wallet is publicly disclosed. The team commits to transparent reporting of how these funds are deployed.

---

## Zero Tax on Vault Sales

When selling $TROVE directly to the Vault via the DApp, **no tax is applied.** You receive the full floor price in ETH.

This is intentional. The Vault sale mechanism is a fundamental right of every $TROVE holder — it shouldn't be taxed. Sellers to the Vault are also permanently burning their tokens, which benefits all remaining holders, so there is no reason to penalize this action.

---

## Why 3%?

EtherSafe, the inspiration for BaseTrove, used 3% (1.5/1.5). This rate is:

- Low enough not to deter trading or create significant arb friction
- High enough to generate meaningful Vault accumulation at scale
- Familiar to DeFi users — not a surprise or a trap

There are no hidden fees, no dynamic tax adjustments, and no owner function that can increase the tax rate post-launch. The 3% is written into the contract and cannot be changed.
