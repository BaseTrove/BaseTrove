# How It Works

BaseTrove operates through three interconnected systems that reinforce each other continuously.

---

## The Three Systems

### 1. The Vault

The Vault is a smart contract that holds ETH and backs $TROVE with a guaranteed price floor.

The floor price is always:
```
Price Floor = Total ETH in Vault ÷ Circulating $TROVE Supply
```

Any $TROVE holder can sell their tokens directly to the Vault at this price at any time — no slippage, no market impact. When they do, those tokens are **permanently burned**, reducing supply and raising the floor price for everyone remaining.

The Vault's ETH balance grows from two sources:
- **50% of all miner revenue** deposited directly
- **Swap taxes** from $TROVE trades on the DEX pools

The Vault's ETH balance never decreases except to pay out sellers. And as supply shrinks from burns, the floor per token rises even without new ETH coming in.

---

### 2. The Mining Engine

A fleet of solar-powered ASIC miners runs 24/7, generating Bitcoin mining revenue from pure sunlight and battery storage. This revenue is converted to ETH on Base and split:

- **50% → Vault** — floor price rises
- **50% → Buyback** — $TROVE is purchased from one of the two DEX pools and permanently burned

The key insight: **this happens regardless of whether anyone is trading $TROVE.** The floor rises even on days with zero volume. The supply shrinks even in a bear market.

---

### 3. Dual LP Arbitrage

$TROVE has liquidity in two pools simultaneously:
- **TROVE/USDC**
- **TROVE/ETH**

When the mining engine executes a buyback on one pool, it creates a price discrepancy between the two. Arbitrage bots — automated programs that scan for price gaps — immediately step in to correct it by buying on the cheaper pool and selling on the more expensive one.

Every arb trade generates swap taxes. Those taxes flow into the Vault. More arb volume = more ETH in Vault = higher floor price.

The buyback target pool is **selected randomly** on each execution to prevent front-running and maximize arb activity.

---

## The Full Flywheel

```
☀️  Solar Energy
      ↓
⛏️  ASIC Miners generate BTC revenue
      ↓
   Convert to ETH on Base
      ↓
   ┌──────────────────────────┐
   │  50%          50%        │
   ↓                ↓
🏦 Vault        🔥 Buyback from LP
   (ETH up)        (TROVE burned)
      ↓                ↓
   Floor rises    Supply shrinks
                       ↓
              ⚖️  Price gap opens between pools
                       ↓
              🤖  Arb bots trade to close gap
                       ↓
              💰  Swap taxes → Vault
                       ↓
              Floor rises (again)
```

Each revolution of this flywheel leaves $TROVE with a higher floor, lower supply, and more ETH backing every token.

> Deep dive: [The Vault](the-vault.md) · [Dual LP](dual-lp.md) · [Arbitrage Engine](arbitrage.md)
