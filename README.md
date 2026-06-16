# Alchemix (alchemix)

Alchemix is a self-repaying DeFi protocol that allows users to take out interest-free, non-liquidating loans against yield-bearing collateral. Users deposit assets such as ETH, DAI, USDC, or USDT into yield-bearing vaults, and the generated yield automatically repays the loan over time. The protocol issues synthetic alAssets (alUSD, alETH) representing future yield, and provides a Transmuter mechanism to stabilize alAsset prices by gradually exchanging alAssets for underlying collateral. Alchemix operates on Ethereum Mainnet, Optimism, and Arbitrum, with V3 in active development targeting 90% LTV and Meta-Yield Tokens.

**APIs.json:** [https://alchemix.fi/](https://alchemix.fi/)

## Tags

- DeFi
- Self-Repaying Loans
- Synthetic Assets
- Yield
- Ethereum
- Blockchain
- Lending
- alUSD
- alETH
- ALCX

## Timestamps

- **Modified:** 2026-06-14

## APIs

### Alchemix Smart Contract API

The primary developer interface for Alchemix is its on-chain smart contracts deployed on Ethereum Mainnet, Optimism, and Arbitrum. Core contracts include the Alchemist (vault deposits, borrowing, repayment, liquidation, and harvesting), the Transmuter (alAsset-to-underlying exchange), and the TransmuterBuffer (flow rate control between Alchemist and Transmuter). Developers interact with these contracts via standard EVM JSON-RPC using libraries such as ethers.js or viem.

- **Human URL:** [https://docs.alchemix.fi](https://docs.alchemix.fi)
- **Base URL:** `https://ethereum.drpc.org`

#### Tags

- Smart Contracts
- EVM
- Ethereum
- Optimism
- Arbitrum
- Alchemist
- Transmuter
- Vault

#### Properties

- [Documentation](https://docs.alchemix.fi)
- [GitHub Organization](https://github.com/alchemix-finance)
- [Contract Deployments](https://github.com/alchemix-finance/deployments)
- [Source Code](https://github.com/alchemix-finance/v2-foundry)
- [Graph Q L](graphql/alchemix-graphql.md)

### Alchemix Subgraph API

Alchemix uses The Graph protocol to index on-chain events and expose yield data, harvest history, transmuter APR, and vault position data via GraphQL. The subgraph is queried by the official Alchemix frontend using an API key configured via VITE_SUBGRAPH_API_KEY. Developers can query the subgraph through The Graph's decentralized network gateway to access alAsset positions, transmuter state, yield strategy performance, and historical protocol analytics.

- **Human URL:** [https://thegraph.com/explorer?search=alchemix](https://thegraph.com/explorer?search=alchemix)
- **Base URL:** `https://gateway.thegraph.com`

#### Tags

- GraphQL
- Subgraph
- The Graph
- Yield Data
- Harvest History
- Analytics

#### Properties

- [Documentation](https://thegraph.com/docs/en/subgraphs/querying/introduction/)
- [Explorer](https://thegraph.com/explorer?search=alchemix)

### Alchemix Protocol Analytics API (DeFiLlama)

DeFiLlama provides a free, public REST API for Alchemix protocol analytics including TVL history, fee revenue, chain breakdowns, and token data. The protocol slug for Alchemix is "alchemix". The API returns current and historical TVL across Ethereum, Optimism, and Arbitrum, annualized fees, cumulative revenue, market cap, and token price data. No API key is required for normal usage, and the API serves billions of requests per month with no rate limits for standard traffic.

- **Human URL:** [https://defillama.com/protocol/alchemix](https://defillama.com/protocol/alchemix)
- **Base URL:** `https://api.llama.fi`

#### Tags

- Analytics
- TVL
- Revenue
- Fees
- Protocol Metrics
- DeFiLlama

#### Properties

- [Documentation](https://api-docs.defillama.com/)
- [Protocol Page](https://defillama.com/protocol/alchemix)

### Alchemix Token Price API (CoinGecko)

CoinGecko provides real-time and historical price data for all Alchemix protocol tokens including ALCX (governance token), alUSD (synthetic USD stablecoin), and alETH (synthetic ETH). Prices are aggregated across multiple exchanges using global volume-weighted averages. The CoinGecko API supports ALCX at coin ID "alchemix", alUSD at "alchemix-usd", and alETH at "alchemix-eth". A free-tier API is available with rate limits; a Pro API key removes limits.

- **Human URL:** [https://www.coingecko.com/en/coins/alchemix](https://www.coingecko.com/en/coins/alchemix)
- **Base URL:** `https://api.coingecko.com`

#### Tags

- Price
- Market Data
- ALCX
- alUSD
- alETH
- CoinGecko

#### Properties

- [Documentation](https://www.coingecko.com/api/documentation)
- [Token Page](https://www.coingecko.com/en/coins/alchemix)
- [Al U S D Page](https://www.coingecko.com/en/coins/alchemix-usd)
- [Al E T H Page](https://www.coingecko.com/en/coins/alchemix-eth)

### Alchemix Yield Snapshot Storage API (Pinata/IPFS)

Alchemix stores yield historic snapshots and transmuter APR data on IPFS via Pinata. The Alchemix frontend retrieves this data using the VITE_PINATA_KEY environment variable to access pinned JSON files containing yield strategy performance history and transmuter timing estimates. Developers can access the same IPFS-stored data through public IPFS gateways or the Pinata API for building applications that display historical yield data or estimate transmuter completion times.

- **Human URL:** [https://www.pinata.cloud](https://www.pinata.cloud)
- **Base URL:** `https://api.pinata.cloud`

#### Tags

- IPFS
- Pinata
- Yield History
- Transmuter APR
- Decentralized Storage

#### Properties

- [Documentation](https://docs.pinata.cloud)
- [Gateway U R L](https://gateway.pinata.cloud)

## Maintainers

**FN:** Alchemix Finance
**Email:** admin@alchemix.fi
**URL:** https://alchemix.fi
