# The Vault

The Vault is the backbone of BaseTrove. It is a smart contract that holds ETH and guarantees every $TROVE holder a minimum redemption price — at all times, unconditionally.

---

## The Price Floor Formula

```
Price Floor = Total ETH in Vault ÷ Circulating $TROVE Supply
```

This is the minimum price at which anyone can sell $TROVE, directly to the Vault, at any time.

**Example:**
- Vault holds 10 ETH
- 5,000 $TROVE in circulation
- Price floor = **0.002 ETH per TROVE**

If 500 TROVE are sold to the Vault and burned:
- Vault pays out 1 ETH (500 × 0.002)
- Vault holds 9 ETH
- 4,500 TROVE in circulation
- New floor = 9 ÷ 4,500 = **0.002 ETH per TROVE**

The floor price stays the same after a sale — it only rises when new ETH enters the Vault without a corresponding increase in supply.

---

## What Grows the Vault

Three revenue streams continuously add ETH to the Vault:

| Source | Description |
|---|---|
| **Mining Revenue (50%)** | Half of all solar miner earnings, deposited on every cycle |
| **Buy Tax (1.5%)** | Applied to every $TROVE purchase on the DEX |
| **Sell Tax (1.5%)** | Applied to every $TROVE sale on the DEX |

No ETH is ever removed from the Vault except to pay out token holders who sell to it. The Vault does not pay salaries, fund operations, or cover marketing. It exists solely for holders.

---

## What Grows the Floor Price

The floor price rises whenever:

1. **ETH enters the Vault** (mining deposits, swap taxes)
2. **$TROVE is burned** (via buybacks or DApp sales) — same ETH now backs fewer tokens

Because both happen continuously and simultaneously, the floor price has a **structural upward bias** that does not depend on market price, sentiment, or volume.

---

## Selling to the Vault

Any $TROVE holder can sell directly to the Vault at the current floor price via the BaseTrove DApp:

1. Connect your wallet on Base
2. Enter the amount of $TROVE to sell
3. Receive ETH instantly at the guaranteed floor price
4. Your $TROVE tokens are permanently burned

There are **no taxes on Vault sales** — you receive the full floor price in ETH.

> Note: The floor price is a *minimum*. $TROVE will typically trade above floor on the open market due to speculation and premium. Selling to the Vault is only optimal when the DEX price has fallen below floor — which is when the arbitrage mechanism kicks in.

---

## Why the Floor Can Only Go Up

Even on a day with zero trading activity:
- Mining revenue continues depositing ETH into the Vault
- Supply stays constant (no one selling to the Vault = no burns)
- Floor price increases: more ETH ÷ same supply

And on active trading days:
- Swap taxes add ETH to the Vault
- Buybacks reduce supply
- Arb bot activity further adds to taxes
- Floor price increases faster

**There is no mechanism that reduces the floor price.** It only ever goes up.
