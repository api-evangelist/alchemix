# Alchemix FinOps

Financial operations considerations for developers and integrators building
on or querying the Alchemix protocol.

## Protocol Economics (As of June 2026)

| Metric | Value |
|--------|-------|
| Total Value Locked (TVL) | ~$30.12 million |
| Ethereum TVL | ~$28.19 million (93.6%) |
| Optimism TVL | ~$1.64 million (5.4%) |
| Arbitrum TVL | ~$285,449 (0.9%) |
| Annualized Fees | ~$1.14 million |
| Annualized Revenue | ~$113,791 |
| ALCX Market Cap | ~$8.86 million |
| ALCX Price | ~$3.51 |
| Treasury Value | ~$2.09 million |

Source: DeFiLlama (https://defillama.com/protocol/alchemix)

## Cost Centers for Integrators

### Gas Costs (Ethereum Mainnet)
Interactions with Alchemix smart contracts require ETH for gas. Key operations:
- `deposit()` — deposit collateral into a yield strategy vault
- `mint()` — borrow alAssets against deposited collateral
- `repay()` — repay loan with underlying or alAssets
- `liquidate()` — self-liquidate position
- `harvest()` — trigger yield harvest (triggers Transmuter exchange)
- `exchange()` — exchange alAssets for underlying via Transmuter

Optimism and Arbitrum offer significantly lower gas costs than Ethereum Mainnet.

### RPC Provider Costs
For production integrations, a paid RPC plan is recommended:
- dRPC: https://drpc.org/pricing
- Alchemy: https://www.alchemy.com/pricing
- Infura: https://www.infura.io/pricing

### Subgraph Query Costs
The Graph decentralized network charges GRT tokens per query. Budget
accordingly if querying yield history or harvest data at scale.

### CoinGecko API Costs
Free tier is sufficient for low-volume price lookups. High-frequency
price feeds should use a Pro plan ($129–$999/month) or a dedicated
on-chain price oracle (Chainlink).

## Chainlink Oracle Integration
Alchemix integrates Chainlink Keepers for automated vault harvesting and
Chainlink price feeds for DeFi price data. Developers building yield
automation may incur Chainlink Keeper costs (LINK tokens).

Reference: https://alchemixfi.medium.com/alchemix-integrates-chainlink-keepers-for-vault-harvesting-and-launches-new-price-feeds-for-defi-34ff62a07b43

## ALCX Token Contract Addresses

| Network | Token | Address |
|---------|-------|---------|
| Ethereum | ALCX | 0xdBdb4d16EdA451D0503b854CF79D55697F90c8DF |
| Ethereum | alETH | 0x0100546F2cD4C9D97f798fFC9755E47865FF7Ee6 |
| Optimism | ALCX (bridged) | 0xe974b9b31dbff4369b94a1bab5e228f35ed44125 |

Full deployment artifacts: https://github.com/alchemix-finance/deployments
