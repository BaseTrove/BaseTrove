# Token Supply

$TROVE has a fixed, small, and intentionally scarce supply. Scarcity is not a marketing claim — it is enforced by the smart contract with no mint function.

---

## Supply at a Glance

| Property | Value |
|---|---|
| **Total Supply** | 10,000 TROVE |
| **Mintable** | No — supply is fixed at deployment |
| **Burnable** | Yes — burned tokens are permanently removed |
| **Effective Supply** | Decreases over time, never increases |

---

## Why 10,000?

The supply size is chosen to make the **Vault price floor mathematically meaningful** from a small ETH base.

With 10,000 TROVE and an initial Vault seeding of 5 ETH:
```
Initial floor = 5 ETH ÷ 10,000 = 0.0005 ETH per TROVE
```

As mining revenue deposits ETH and buybacks reduce supply:
- 1,000 TROVE burned → 9,000 remaining → floor rises ~11% (same ETH)
- 1 ETH added to Vault → floor rises 11% (same supply)
- Both happen simultaneously

Small supply means each individual burn and each ETH deposit has a **visible, material impact** on the floor price. Holders can directly observe their holdings becoming more backed with each cycle.

---

## Supply Trajectory

Supply is designed to only decrease. The following actions reduce it permanently:

1. **Mining buybacks** — $TROVE purchased from LP and burned to dead address
2. **DApp sales** — holders sell $TROVE to the Vault; tokens are burned
3. **No new issuance** — no staking rewards, no vesting unlocks, no new mints

Over a 12-month horizon, the combination of daily buybacks and organic Vault selling will meaningfully compress the circulating supply, continuously raising the floor price.

---

## Supply vs Floor Price Relationship

The relationship between supply reduction and floor price is non-linear. The fewer tokens remain, the greater the impact of each additional burn:

| Circulating Supply | Vault ETH | Floor Price |
|---|---|---|
| 10,000 | 10 ETH | 0.001 ETH |
| 8,000 | 12 ETH | 0.0015 ETH |
| 5,000 | 15 ETH | 0.003 ETH |
| 2,000 | 20 ETH | 0.01 ETH |

As supply approaches zero and ETH continues accumulating, the floor price per token grows asymptotically. Early holders benefit most from holding through supply compression.
