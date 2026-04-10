# FAQ

---

### What is $TROVE?

$TROVE is the native token of BaseTrove — a deflationary ERC-20 token on Base chain backed by a Vault of ETH and fueled by solar-powered Bitcoin miners.

---

### What backs the price floor?

The Vault — a smart contract holding ETH. The floor price equals total Vault ETH divided by circulating $TROVE supply. This floor is guaranteed by code, not by promises.

---

### Can the floor price go down?

No. The floor price can only go up or stay the same. The Vault ETH only increases (from mining deposits and swap taxes). The supply only decreases (from burns). Both movements push the floor price upward.

The floor price stays flat only if no ETH enters the Vault and no burns occur — which effectively never happens while miners are running.

---

### What happens if the DEX price falls below the Vault floor?

If $TROVE's market price on the DEX falls below the Vault floor, rational traders will buy TROVE on the DEX (cheap) and sell it to the Vault (at the guaranteed higher floor price), pocketing the difference in ETH. This closes the gap automatically without any team intervention.

---

### What are the risks?

Honest risks:

- **Mining downtime** — hardware failures, extended cloud cover, or regulatory issues could reduce mining revenue
- **BTC price decline** — if Bitcoin price drops significantly, mining revenue in ETH terms decreases
- **Smart contract risk** — audited code can still have vulnerabilities; no audit is a 100% guarantee
- **Liquidity risk** — if liquidity is thin, large Vault sells could move the DEX price significantly

We mitigate these with hardware redundancy, battery backup, professional audits, and locked liquidity. No project is risk-free — we prefer you understand the risks clearly.

---

### Is there a team token dump risk?

The team's 1,000 TROVE (10%) are locked with a 6-month cliff and 24-month linear vesting. No team tokens are accessible at launch. The vesting contract is deployed on-chain and verifiable.

---

### How do I know the miners are actually running?

The buyback wallet address is public. You can watch BTC arrive, get converted to ETH on Base, and get deployed into the Vault and buybacks — all on-chain. We also publish hash rate data and regular mining reports in community channels.

---

### How often do buybacks happen?

Daily or more frequently, depending on mining revenue accumulation. Base chain's sub-cent gas fees allow small amounts to be deployed efficiently without waiting for large batches.

---

### Can the tax rate change?

No. The 3% tax rate is hardcoded in the smart contract and cannot be modified by anyone, including the team.

---

### Where can I trade $TROVE?

$TROVE trades on Uniswap on Base via two pools: TROVE/USDC and TROVE/ETH. Pool addresses are published at launch. You can also sell directly to the Vault via the DApp at the floor price with zero taxes.

---

### Is this a rug pull?

We understand why you'd ask. The red flags of a rug pull are: anonymous team with no accountability, no liquidity lock, team tokens available at launch, no audit, no transparency.

BaseTrove has: doxxed team (via community channels), locked liquidity, locked team tokens with vesting, a published audit, and a public buyback wallet. We can't stop anyone from being skeptical — we can only provide evidence. Do your own research.

---

### What chain is BaseTrove on?

Base — Coinbase's Ethereum L2. Chain ID: 8453.
