# Alchemix (alchemix)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
