# Alchemix GraphQL API

Alchemix uses The Graph protocol to index on-chain events from its smart contracts and expose protocol data via GraphQL. The subgraph tracks Alchemist vault positions (deposits, withdrawals, harvests, liquidations, mints, repayments), Transmuter and TransmuterBuffer state, Curve pool exchanges and liquidity, ThreePoolAssetManager and EthAssetManager activity, and associated historical timeseries. The subgraph is queried by the official Alchemix frontend to display user balances, debt positions, yield strategy performance, and transmuter APR estimates.

Authentication is performed via an API key passed in the Authorization header when using The Graph's decentralized gateway. The legacy hosted service at api.thegraph.com is deprecated and no longer available; developers must use the decentralized network gateway with a valid API key obtained from The Graph's dashboard at thegraph.com.

**Endpoint:** https://gateway.thegraph.com/api/[api-key]/subgraphs/id/[subgraph-id]
**Documentation:** https://thegraph.com/docs/en/subgraphs/querying/introduction/

**References:**
- Documentation: https://thegraph.com/docs/en/subgraphs/querying/introduction/
- GettingStarted: https://thegraph.com/docs/en/subgraphs/quick-start/
- SourceCode: https://github.com/alchemix-finance/subgraph
- Explorer: https://thegraph.com/explorer?search=alchemix
- APIKeys: https://thegraph.com/studio/
