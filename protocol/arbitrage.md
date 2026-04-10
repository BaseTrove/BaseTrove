# Arbitrage Engine

Arbitrage is not a side effect of BaseTrove's design — it's a **core feature.** The protocol is architected to attract, reward, and continuously generate arbitrage activity.

---

## What is Arbitrage?

Arbitrage is the practice of exploiting price differences for the same asset across different markets. In DeFi, automated bots scan hundreds of liquidity pools per second looking for discrepancies. When they find one, they buy from the cheaper pool and sell to the more expensive one, pocketing the difference and closing the gap.

In most DeFi protocols, arbitrage is neutral at best — it benefits the arb bot and creates volume but doesn't necessarily help the protocol.

**In BaseTrove, every arb trade generates swap taxes that flow directly into the Vault.**

Arb bots are, effectively, involuntary contributors to the BaseTrove price floor.

---

## How the Arbitrage Loop Works

**Step 1: Buyback triggers a price gap**

The mining engine deposits ETH/USDC and buys $TROVE from one of the two pools (selected randomly). This raises the price of TROVE in that pool while the other pool remains unchanged. A price gap opens.

**Step 2: Arb bots respond**

Arbitrage bots detect the gap within milliseconds. They buy TROVE from the cheaper pool and sell it to the more expensive one. This generates:
- Swap taxes from the buy → Vault
- Swap taxes from the sell → Vault

**Step 3: Volume begets volume**

The arb trade itself slightly shifts both pools again. Other bots may detect secondary gaps. Each round of arb trades adds ETH to the Vault.

**Step 4: Gap closes, floor is higher**

Once prices equalize across pools, the arb cycle ends — until the next mining buyback triggers a new gap. Given daily or more frequent buybacks, this cycle runs continuously.

---

## The Arb Triangle

When market price dips toward the Vault's floor price, a third arbitrage opportunity opens:

```
Pool A (TROVE/USDC)
        ↕  arb bots
Pool B (TROVE/ETH)
        ↕  rational actors
The Vault (guaranteed floor)
```

If TROVE's DEX price falls below the Vault floor:
- Rational traders buy TROVE cheaply on the DEX
- Sell it to the Vault at the guaranteed floor price
- Pocket the difference in ETH
- TROVE sold to the Vault is permanently burned → supply shrinks → floor rises

This creates a **hard floor arbitrage** — a rational market force that prevents $TROVE from ever sustainably trading below its Vault floor.

---

## Why This Benefits Holders

Every market participant acting in their own interest — arb bots, floor arbitrageurs, regular traders — ends up contributing to the Vault and reducing supply. BaseTrove aligns selfish incentives with collective benefit.

| Actor | Motivation | Effect on $TROVE |
|---|---|---|
| Arb bot | Profit from price gap | Taxes → Vault, volume up |
| Floor arbitrageur | Buy cheap, sell to Vault | Burns supply, floor rises |
| Regular buyer | Speculate on price | Taxes → Vault |
| Regular seller | Take profit | Taxes → Vault |
| Miner | Generate mining yield | Buybacks + Vault deposits |

Everyone who interacts with $TROVE makes it more valuable for those who hold it.
