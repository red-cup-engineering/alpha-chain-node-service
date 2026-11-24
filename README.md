# alpha-chain-node-service

<!-- 561-group-standards:badges:start -->
[![Red Cup Engineering](https://img.shields.io/badge/561%20Group-Red%20Cup%20Engineering-c0392b)](https://github.com/red-cup-engineering)
[![License: MIT](https://img.shields.io/badge/license-MIT-c0392b)](LICENSE)
[![Indigenous data: CARE](https://img.shields.io/badge/Indigenous%20data-CARE-4b6f44)](https://github.com/red-cup-engineering/.github/blob/main/GOVERNANCE.md)
[![Tips welcome](https://img.shields.io/badge/tips-welcome-d4a017)](https://github.com/561-group/.github/blob/main/TIPS.md)
<!-- 561-group-standards:badges:end -->

Forms one Besu QBFT validator or RPC node for the successor alpha chain; the predecessor chain remains historical. The live chain ID is the ALPHA_CHAIN_ID constant in src/alpha-chain.mjs.

The cloud VPS bootstrap producer consumes that same network ID and the declared
Besu version and archive digest from `src/alpha-chain.mjs`. Its `node.env` and
systemd unit therefore select the same network as the native genesis producer
and node arguments. `npm run verify` receives both the native formation and
the cloud bootstrap suites, including their cross-component identity agreement.

The units under `data/records/systemd/` retain historical installations. Select a
new bundle through the current producer and receive the actual genesis and peer
network before activating it; a generated bundle is not evidence of a running
chain, deployed exchange contract or settled internal transaction.
