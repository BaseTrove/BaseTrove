# 🔥 Buyback & Burn Mechanism

The buyback engine converts mining revenue into permanent supply reduction — feeding directly into the Vault's compounding acceleration effect.

---

## Dynamic Allocation

Mining revenue is allocated based on market conditions — not a fixed split. The team monitors the relationship between market price and the Vault floor and deploys revenue where it has the most impact:

```
Mining Revenue (ETH)
        ↓
   Market price HIGH          Market price near floor
   (large premium)            (small premium)
        ↓                           ↓
   → Vault                    → Buyback & Burn
   ETH accumulates            TROVE bought + burned
   Floor rises                Supply compresses
```

**→ Vault**
ETH deposited directly into the Vault. Floor rises immediately.
```
New Floor = (Vault ETH + New ETH) ÷ Circulating Supply
```

**→ Buyback & Burn**
ETH is used to purchase TROVE from the TROVE/ETH pool on Uniswap v2. The purchased TROVE is permanently burned — removing it from circulating supply forever.

When market price trades at a large premium to the floor, buybacks are less efficient — each ETH buys fewer tokens. In this case revenue is directed to the Vault instead, growing the ETH reserve. When market price approaches the floor, buybacks become highly efficient and revenue is redirected to burning supply aggressively. Both modes raise the floor. The allocation simply adjusts to whichever path moves it faster.

---

## Why the Burn Accelerates the Vault

When TROVE is burned, the supply shrinks. The same ETH already in the Vault now backs fewer tokens — so the floor price rises **without any new ETH entering.** Then when the next mining deposit arrives, it's divided among fewer tokens, moving the floor further than the last deposit did.

```
Burn → fewer tokens → same ETH hits harder
         ↓
Next deposit → moves floor further than before
         ↓
Next burn → even fewer tokens → next deposit hits even harder
         ↓
         ...accelerates indefinitely
```

The more TROVE gets burned, the faster the floor loads up.

---

## Market Price & Burn Rate

The number of tokens burned per buyback depends on the market price at the time of purchase:

```
TROVE burned = Buyback ETH ÷ DEX Market Price
```

When TROVE trades at a high premium above floor, each buyback burns fewer tokens — but the Vault still fills at the same ETH rate. When price is near floor, buybacks are highly efficient and burn more tokens per ETH spent.

Both scenarios raise the floor. The composition just differs.

---

## Execution Frequency

Base chain's sub-cent gas fees mean buybacks deploy as revenue arrives — daily or more. No batching required. Small amounts hit the market frequently, creating consistent buy pressure and smooth floor growth.

---

## Profit-Switching

The miners don't just mine Bitcoin. They switch to whichever Proof-of-Work coin is most profitable at any given time — Bitcoin, Zcash, Ethereum Classic, or others. All earnings convert to ETH on Base before deployment.

Buyback revenue is always maximized regardless of which coin is performing best.

---

## Cadence Example

Assume the mining fleet generates 0.5 ETH/day during a period where market price is near floor:

| Allocation | Amount | Effect |
|---|---|---|
| Vault deposit | variable | Floor rises |
| Buyback | variable | TROVE purchased from pool + burned |

Over 30 days at this rate: ~15 ETH deployed across Vault and buybacks, supply compressed from daily burns, floor accelerating upward. As hardware expands with reinvested fee revenue, this cadence grows — more miners, more revenue, faster floor growth regardless of allocation mode.
