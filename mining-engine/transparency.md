# Transparency & Verification

BaseTrove operates on a simple principle: **don't trust, verify.** Every claim the protocol makes about its mining operations and finances is independently verifiable on-chain.

---

## The Public Buyback Wallet

A single, publicly disclosed wallet address is responsible for all mining revenue reception and deployment. This wallet:

- Receives BTC mining rewards (Bitcoin address disclosed)
- Converts BTC → ETH on Base (swap transactions visible on-chain)
- Executes Vault deposits (Base transactions visible)
- Executes LP buybacks (Base transactions visible)

Anyone can monitor this wallet at any time using a Base block explorer. Every deposit, every swap, every buyback — timestamped and permanent.

> Buyback wallet address: **[Published at launch]**

---

## What You Can Verify On-Chain

| Data Point | How to Verify |
|---|---|
| Vault ETH balance | Read Vault contract on Basescan |
| Circulating supply | ERC-20 totalSupply minus burned |
| Total burned | Balance of dead address (0x000...dEaD) |
| Buyback history | Buyback wallet transaction history |
| Vault deposits | Vault contract event logs |
| Mining wallet BTC earnings | Bitcoin address explorer |

No spreadsheet, no blog post, no Discord announcement is needed. The data lives on immutable blockchains that anyone in the world can read.

---

## Live Dashboard

The BaseTrove DApp includes a **live statistics dashboard** displaying:

- Current Vault ETH balance
- Current $TROVE floor price
- Circulating supply
- Total $TROVE burned (all time)
- Last buyback: amount, pool, timestamp
- Mining wallet balance (BTC + ETH)
- Estimated daily Vault growth rate

This dashboard refreshes automatically and pulls data directly from on-chain sources — not from a team-controlled backend.

---

## Mining Hardware Verification

The team commits to providing:

- Photos and specs of the physical mining hardware
- Panel/battery array documentation
- Hash rate reporting (verifiable against pool dashboard)
- Regular operational updates on [Telegram](https://t.me/BaseTrove) and [X](https://x.com/BaseTrove)

We will never claim mining revenue we can't demonstrate on-chain.

---

## The Commitment

BaseTrove's team holds no special privileges over the Vault. Once the Vault contract is deployed, it operates according to its code. The team cannot:

- Withdraw ETH from the Vault
- Pause or modify the floor price formula
- Override buyback execution

The smart contract is the rule. Everything else is commentary.

> Contract audit report: **[Published at launch]**
