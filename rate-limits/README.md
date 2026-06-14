# Alchemix Rate Limits

Rate limits vary by the API layer used to interact with Alchemix data.

## Smart Contract (EVM JSON-RPC)

Rate limits are set by the RPC provider, not by Alchemix itself. The official
Alchemix frontend uses dRPC as its provider (configured via
`VITE_DRPC_MAINNET_API_KEY`, `VITE_DRPC_OPTIMISM_API_KEY`,
`VITE_DRPC_ARBITRUM_API_KEY`).

| Provider | Free Tier Limit | Notes |
|----------|----------------|-------|
| dRPC | Varies by plan | https://drpc.org |
| Alchemy | 330M compute units/month free | https://www.alchemy.com |
| Infura | 100,000 requests/day free | https://infura.io |
| Public RPC | Unpublished, throttled | Not recommended for production |

## The Graph Subgraph

Alchemix uses a subgraph key (`VITE_SUBGRAPH_API_KEY`) for querying yield
history and harvest data. The Graph's decentralized network charges query
fees in GRT tokens. The Graph Studio hosted service is deprecated.

| Access | Limit | Notes |
|--------|-------|-------|
| Decentralized Network | Pay-per-query in GRT | https://thegraph.com |
| Free allocation | Limited monthly queries | Via The Graph Studio |

## DeFiLlama API

| Access | Limit | Notes |
|--------|-------|-------|
| Public API | No rate limits for normal traffic | https://api.llama.fi |
| High volume | Contact DeFiLlama | Billions of requests/month served |

## CoinGecko API (ALCX, alUSD, alETH price data)

| Tier | Rate Limit | Notes |
|------|-----------|-------|
| Free (no key) | 30 calls/minute | https://api.coingecko.com/api/v3 |
| Demo key | 30 calls/minute | Register at coingecko.com/api |
| Analyst ($129/mo) | 500 calls/minute | Pro plan |
| Lite ($499/mo) | 500 calls/minute | Pro plan |
| Pro ($999/mo) | 1,000 calls/minute | Pro plan |
| Enterprise | Custom | Contact CoinGecko |

## Pinata/IPFS (Yield Snapshots)

| Access | Limit | Notes |
|--------|-------|-------|
| Public IPFS Gateway | Unpublished, throttled | gateway.ipfs.io |
| Pinata Free | 1 GB storage, 100 GB bandwidth/mo | https://pinata.cloud |
| Pinata Picnic ($20/mo) | 10 GB storage, 500 GB bandwidth | Commercial use |
