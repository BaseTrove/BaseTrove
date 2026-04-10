# 🔄 How It Works

BaseTrove is built on a single relentless mechanic: **burn supply, fill the Vault, repeat — faster every time.**

Three systems drive this flywheel simultaneously, each one feeding the others.

---

## The Three Systems

### 1. The Vault

A smart contract holding ETH. The floor price is always:
```
Price Floor = Total ETH in Vault ÷ Circulating $TROVE Supply
```

ETH fills the Vault from two directions at once: mining revenue deposits and swap fees from every trade. Supply shrinks from buyback burns and Vault sales. Both movements raise the floor — and they compound on each other.

The fewer tokens remain, the faster each new ETH deposit moves the floor. **The system accelerates as it runs.**

---

### 2. The Mining Engine

Solar-powered ASIC miners run 24/7, profit-switching between Bitcoin, Zcash, Ethereum Classic, and other Proof-of-Work coins to always maximize revenue. All earnings convert to ETH on Base and split:

- **50% → Vault** — floor rises immediately
- **50% → Buyback** — TROVE bought from a random LP, burned forever

This happens regardless of market conditions. No trading volume required. The floor rises and supply shrinks even in a bear market, even on days with zero community activity.

---

### 3. Dual LP Arbitrage

Two live liquidity pools: **TROVE/USDC** and **TROVE/ETH** on Uniswap v2.

Every buyback creates a price gap between pools. Arbitrage bots close it within milliseconds — and every arb trade generates swap fees that flow into the Vault. One buyback triggers a cascade of volume the protocol didn't have to pay for.

The buyback pool is randomly selected each time, preventing front-running and keeping both pools perpetually active.

---

## The Full Flywheel

```
☀️  Solar Energy
      ↓
⛏️  ASIC Miners (profit-switch: BTC / ZEC / ETC / ...)
      ↓
   Convert to ETH on Base
      ↓
   ┌─────────────────────────┐
  50%                       50%
   ↓                         ↓
🏦 Vault               🔥 Buyback from random LP
   (ETH up)                (TROVE burned)
      ↓                         ↓
  Floor rises            Supply shrinks
      ↓                         ↓
  Each future burn     Each future deposit
  hits harder  ←———→  hits harder
      ↓
  ⚖️ Price gap opens between pools
      ↓
  🤖 Arb bots trade to close gap
      ↓
  💰 Swap fees (2–5%) → 50% Vault · 50% Team
      ↓
  Team reinvests → more miners → more revenue
      ↓
  🔁 Flywheel spins faster
```

Every revolution: higher floor, lower supply, more ETH per token. And each revolution is faster than the last.

---

## Multiple Utilities, One Direction

BaseTrove's floor price is powered by multiple independent revenue streams — not one:

| Utility | What it does |
|---|---|
| ASIC Mining | Buybacks + Vault deposits, 24/7, market-independent |
| Swap Fees | 50% to Vault on every trade |
| Arbitrage Bots | Free volume → more fees → more Vault ETH |
| Vault Sales | Burns supply → floor rises, ETH paid out |
| Future Tech | Additional revenue streams added to the same flywheel over time |

Any one of these alone would be a reasonable deflationary mechanic. Together, compounding on a supply of 1,000 tokens, they create an accelerating system where the floor price rising is not a goal — it's a mathematical certainty.

> Deep dive: [The Vault](the-vault.md) · [Dual LP](dual-lp.md) · [Arbitrage Engine](arbitrage.md)
