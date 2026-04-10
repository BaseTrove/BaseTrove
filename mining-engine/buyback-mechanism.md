# 🔥 Buyback & Burn Mechanism

The buyback engine converts mining revenue into permanent supply reduction — feeding directly into the Vault's compounding acceleration effect.

---

## The Split

Every mining revenue cycle is split automatically:

```
Mining Revenue (ETH)
        ↓
   ┌────┴────┐
  50%       50%
   ↓         ↓
 Vault    Buyback & Burn
```

**50% → Vault**
ETH deposited directly. Floor rises immediately.
```
New Floor = (Vault ETH + New ETH) ÷ Circulating Supply
```

**50% → Buyback & Burn**
ETH used to purchase TROVE from a randomly selected pool. The purchased TROVE is permanently burned — removing it from the circulating supply forever.

---

## Why the Burn Accelerates the Vault

This is the core compounding mechanic.

When TROVE is burned, the supply shrinks. The same ETH already sitting in the Vault now backs fewer tokens — so the floor price rises **without any new ETH entering.** Then when the next mining deposit arrives, it's divided among even fewer tokens, moving the floor further than the last deposit did.

```
Burn → fewer tokens → same ETH hits harder
         ↓
Next deposit → moves floor further than before
         ↓
Next burn → even fewer tokens → next deposit hits even harder
         ↓
         ...accelerates indefinitely
```

The more TROVE gets burned, the faster the floor loads up. **The system is designed to compound on itself.**

---

## Random Pool Selection

Each buyback randomly selects between Pool A (TROVE/USDC) and Pool B (TROVE/ETH).

- Prevents MEV bots and front-runners from positioning ahead of known buybacks
- Keeps both pools under continuous buyback pressure
- Forces arbitrage activity across both pools unpredictably

---

## Execution Frequency

Base chain's sub-cent gas fees mean buybacks deploy as revenue arrives — daily or more. No batching required. Small amounts hit the market frequently rather than large amounts hitting infrequently, which creates more consistent arb activity and smoother floor growth.

---

## Profit-Switching

The miners don't just mine Bitcoin. They automatically switch to whichever Proof-of-Work coin is most profitable at any given time — Bitcoin, Zcash, Ethereum Classic, or others. All earnings convert to ETH on Base before deployment.

This means buyback revenue is always maximized, regardless of which coin is performing best in the market.

---

## Cadence Example

Assume the mining fleet generates 0.5 ETH/day at steady state:

| Allocation | Amount | Effect |
|---|---|---|
| Vault deposit | 0.25 ETH | Floor rises |
| Buyback | 0.25 ETH | TROVE purchased + burned |
| Arb volume triggered | ~0.5–1.5× buyback size | Additional fees → Vault |

Over 30 days: ~7.5 ETH added to Vault, supply meaningfully compressed, floor accelerating upward. As hardware expands with reinvested fee revenue, this cadence increases — more miners, more buybacks, faster burns.
