# Compound COMP Token Distribution Bug — PoC

> **Educational Purpose Only** — This PoC is created for security research and education
> purposes only. It runs against a fork, not mainnet.

## Quick Start

```bash
git clone https://github.com/NomosLabs-Security/poc-compound-reward-2021
cd poc-compound-reward-2021
forge test -vvvv
```

## Details

- **Exploit Date:** 2021-09-30
- **Fork Block:** #13379753
- **Expected Output:** Demonstration of excess COMP token distribution
- **Full Analysis:** [NomosLabs Security Intelligence Archive](https://nomoslabs.io/archive/compound-reward-2021)

## Description

The _setCompSpeeds() function in the Comptroller, updated via Proposal 062,
reset the compSupplyState index for existing markets, causing excess COMP
to be distributed to users.

This PoC demonstrates:
1. compSupplyState index reset
2. Claiming excess COMP via claimComp()
3. Governance timelock delaying the fix

## RPC Providers

```
Alchemy:   https://eth-mainnet.alchemyapi.io/v2/YOUR_KEY
Infura:    https://mainnet.infura.io/v3/YOUR_KEY
QuickNode: https://YOUR_ENDPOINT.quiknode.pro/YOUR_KEY
```

## License

MIT — For educational use only.
