# 🔄 How It Works

BaseTrove is built on a single relentless mechanic: **burn supply, fill the Vault, repeat — faster every time.**

Two systems drive this flywheel simultaneously, each one feeding the other.

---

## The Two Systems

### 1. The Vault

A smart contract holding ETH. The floor price is always:
```
Price Floor = Total ETH in Vault ÷ Circulating $TROVE Supply
```

ETH fills the Vault from two directions at once: mining revenue deposits and swap fees from every trade. Supply shrinks from buyback burns and Vault sales. Both movements raise the floor — and they compound on each other.

The fewer tokens remain, the faster each new ETH deposit moves the floor. **The system accelerates as it runs.**

---

### 2. The Mining Engine

Solar-powered ASIC miners run 24/7, profit-switching between Bitcoin, Zcash, Ethereum Classic, and other Proof-of-Work coins to always maximize revenue. All earnings convert to ETH on Base and are deployed dynamically:

- **→ Vault** — when market price trades at a significant premium to floor, revenue fills the Vault, growing the ETH reserve
- **→ Buyback & Burn** — when market price approaches the floor, revenue buys TROVE from the TROVE/ETH pool and burns it permanently, as buybacks are most efficient at low premiums

This happens regardless of market conditions. No trading volume required. The floor rises and supply shrinks even in a bear market, even on days with zero community activity.

---

## The Full Flywheel

```
☀️  Solar Energy
      ↓
⛏️  ASIC Miners (profit-switch: BTC / ZEC / ETC / ...)
      ↓
   Convert to ETH on Base
      ↓
   ┌──────────────────────────────────────┐
  Dynamic allocation (market-dependent)
   ↓                                    ↓
🏦 Vault (high premium)     🔥 Buyback & Burn (near floor)
   (ETH up)                    (TROVE burned)
      ↓                         ↓
  Floor rises            Supply shrinks
      ↓                         ↓
  Each future burn     Each future deposit
  hits harder  ←———→  hits harder
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

BaseTrove's floor price is powered by multiple independent revenue streams:

| Utility | What it does |
|---|---|
| ASIC Mining | Revenue to Vault or buybacks dynamically, 24/7, market-independent |
| Swap Fees | Portion of every TROVE/ETH DEX trade flows to Vault |
| Floor Arbitrage | DEX price dips near floor → rational buyers step in, burn supply |
| Vault Sales | Burns supply → floor rises, ETH paid out |
| Trading Bots | Protocol-run bots generating revenue directed to Vault |
| Partnerships | Revenue-sharing with Base ecosystem projects |
| Games & Apps | Onchain products where fees flow back to Vault |
| Warehouse Scale | Long-term: dedicated mining facility for maximum continuous output |

Any one of these alone would be a reasonable deflationary mechanic. Together, compounding on a supply of 100,000 tokens, they create an accelerating system where the floor price rising is not a goal — it's a mathematical certainty.

> Deep dive: [The Vault](the-vault.md) · [The Acceleration Effect](acceleration.md) · [Arbitrage](arbitrage.md)
