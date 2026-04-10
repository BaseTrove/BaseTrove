# Dual Liquidity Pools

BaseTrove maintains two simultaneous liquidity pools for $TROVE — a deliberate design decision that amplifies the deflationary pressure from every buyback.

---

## The Two Pools

| Pool | Pair | Purpose |
|---|---|---|
| **Pool A** | TROVE / USDC | USD-denominated price discovery |
| **Pool B** | TROVE / ETH | ETH-denominated price discovery, aligns with Vault asset |

Both pools are deployed on Base's leading DEXes and are seeded with liquidity at launch.

---

## Why Two Pools?

A single liquidity pool means buybacks raise the price in that pool — full stop. With two pools, something more interesting happens.

When the mining engine buys $TROVE from **Pool A (TROVE/USDC)**:
- The TROVE/USDC price rises
- TROVE/ETH price hasn't moved yet
- A price gap opens between the two pools

Arbitrage bots — programs that scan dozens of pools per second for price discrepancies — detect this gap within milliseconds. They buy the cheaper TROVE (in Pool B) and sell the more expensive TROVE (in Pool A), closing the gap.

This arb trade:
- Generates swap taxes from **both** pools → Vault receives ETH
- Creates additional buy pressure across both pools
- Results in more $TROVE being bought and sold → more taxes → more Vault growth

**One buyback triggers a cascade.** The mining engine puts in $100 of buyback pressure. Arb bots amplify that into $300–$500 of total volume across both pools.

---

## Random Pool Selection

The buyback engine does **not** always target the same pool. On each execution, it selects randomly between Pool A and Pool B.

This serves two purposes:

1. **Prevents front-running** — if miners always bought from Pool A, sophisticated bots would anticipate it and extract value before the buyback executes. Random selection eliminates this predictability.

2. **Maximizes arb frequency** — alternating between pools keeps both price relationships active, ensuring arb bots remain engaged across both pools continuously.

---

## The Vault Connection

Pool B (TROVE/ETH) has a particularly elegant relationship with the Vault. Both denominate $TROVE's value in ETH. When Pool B's price rises above the Vault floor due to buybacks:

- No rational actor sells to the Vault (DEX price > floor price)
- The floor quietly rises from mining deposits in the background
- Eventually, in a market correction, floor price provides a hard support level

When Pool B's price temporarily dips near or below Vault floor:
- Holders can sell to the Vault at guaranteed floor
- This removes supply from circulation
- Floor rises, restoring the gap between floor and market price

The two pools and the Vault form a **self-correcting triangle** that continually pulls $TROVE's value upward.
