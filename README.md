# Immortals

Staking frontend for IMTX on Celo mainnet. A single static `index.html`, no build step.
It talks directly to the contracts below. It holds no funds and no keys.

Hosted at https://imtx.sterntalerapp.xyz

## Features

- Connect wallet, check for Celo, switch network
- Shows IMTX in wallet, staked IMTX, Multiplier Points, msIMTX and claimable rewards
- Claim rewards and stake (`claimRewardsAndStakeMP`)
- Stake IMTX (exact-amount approval, then `stakeIMTX`)
- Unstake IMTX (`unstakeIMTX`)
- Amounts are typed by the user and every transaction is signed in the wallet
- Each transaction is simulated first, so a rejected call is never sent

## Contracts (Celo, chain id 42220)

| Name | Address |
|---|---|
| StakingRewardRouter | `0x5E9a114ccE258fc20aA3C8af3933f926F8c1506A` |
| IMTX | `0x84084B3a9fF2cb1f617355D0773Eb37722BA1D49` |
| sIMTX (staking tracker, approval spender) | `0xDFF42a578F8126ea1A8DDE3d144A83Bcc71c3232` |
| msIMTX | `0x981caDA0d62254c5244402Eb39bd5E1A50a22468` |
| Multiplier Points | `0x03548C511706A0392C5013C7ee75385191739B44` |

## Deploy (GitHub Pages)

1. Settings > Pages > Deploy from a branch > `main` / root.
2. DNS: CNAME record `imtx` -> `frerehugi.github.io`.
3. Enable "Enforce HTTPS" once the certificate is issued.

The `CNAME` file in this repo sets the custom domain.

## Status

Untested against a live wallet. Try a small amount first.
