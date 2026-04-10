# Buyback & Burn Mechanism

The buyback engine is the mechanism through which mining revenue is converted into permanent supply reduction and Vault growth for $TROVE.

---

## The Split

Every time mining revenue is deployed, it is split automatically by the smart contract:

```
Mining Revenue (ETH)
        ↓
   ┌────┴────┐
  50%       50%
   ↓         ↓
 Vault    Buyback
```

**50% → Vault**
ETH is deposited directly into the Vault contract. This immediately raises the price floor:
```
New Floor = (Previous ETH + New ETH) ÷ Circulating Supply
```

**50% → Buyback & Burn**
ETH/USDC is used to purchase $TROVE from one of the two liquidity pools. The purchased $TROVE is immediately and permanently burned.

---

## Random Pool Selection

Each buyback execution randomly selects between Pool A (TROVE/USDC) and Pool B (TROVE/ETH).

**Why random?**

If the buyback always targeted the same pool, sophisticated MEV bots and front-runners would position ahead of every buyback, extracting value from the protocol before the purchase executes. Randomness eliminates this predictability.

The randomness also ensures both pools see regular buyback pressure, keeping arbitrage activity balanced across the full liquidity ecosystem.

---

## Execution Frequency

Thanks to Base's near-zero gas fees, buybacks execute **daily** or more frequently depending on mining revenue accumulation. There is no minimum threshold that needs to be reached before deployment — small amounts can be efficiently deployed as they arrive.

Compare this to Ethereum mainnet, where gas costs would demand batching revenue for days or weeks before execution makes economic sense.

---

## The Burn

$TROVE purchased in buybacks is sent to a dead address (`0x000...dEaD`) — permanently removing it from circulation. These tokens can never be recovered, unstaked, or re-introduced to supply.

Each burn:
1. Reduces circulating supply
2. Increases the ETH-per-token ratio in the Vault (same ETH ÷ fewer tokens = higher floor)
3. Creates a price gap between the two pools (triggering arb)

The cumulative burn total is displayed on the BaseTrove DApp in real time.

---

## Buyback Cadence Example

Assume the mining fleet generates 0.5 ETH/day:

| Allocation | Amount | Effect |
|---|---|---|
| Vault deposit | 0.25 ETH | Floor price rises |
| Buyback | 0.25 ETH | ~X TROVE purchased + burned |
| Arb volume triggered | ~0.5–1.5× of buyback | Additional taxes → Vault |

Over 30 days at this rate:
- **7.5 ETH** added to Vault
- Supply reduced by accumulated burns
- Floor price significantly higher than day 0

Over time, if mining revenue grows (hardware expansion) or BTC price rises, this cadence accelerates.
