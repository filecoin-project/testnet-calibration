# Calibration Testnet

Calibration was reset on `2022-11-01T18:13:00Z`.

This page contains meta info for Filecoin developers about the Calibration testnet.

Please visit the [Filecoin Docs - Networks - Calibration](https://docs.filecoin.io/networks/calibration) for the most up-to-date info.

## Overview

The Filecoin Calibration testnet is a stable testnet that follows Filecoin mainnet closely. It has fewer resets and is intended for longer-term testing efforts from storage providers and developers.

- Like mainnet, Calibration supports `32 GiB`, and `64 GiB` storage sectors.
- It has a Storage Provider auto-accepting new deals from developers (see [Resources](#resources) - *Calibration Storage Providers* below).

## Join Quickstart

- **Build:** <https://lotus.filecoin.io/lotus/manage/switch-networks>
- **Stats:** See [Resources](#resources) - *Block Explorers* below
- **Faucet:** <https://faucet.calibnet.chainsafe-fil.io>
- **Snapshots:** <https://forest-archive.chainsafe.dev/list>

## User Quickstart

1. Add the Calibration testnet to your wallet (e.g. MetaMask).
    - Go to <https://chainlist.org/chain/314159>
    - Click on "Connect wallet"
2. Create a new account in MetaMask to use with Filecoin.
3. Use <https://faucet.calibnet.chainsafe-fil.io> to request funds to your Ethereum address (it will be converted behind the scenes to a Filecoin f410 address)
4. Follow the transaction in one of the recommended Calibration testnet explorers:
    - <https://beryx.zondax.ch>
    - <https://fvm.starboard.ventures>
5. Your account is now funded and can be used in Ethereum tools such as Hardhat, Foundry, Remix, etc.

*Looking for a Storage Provider on Calibration?* - See <https://github.com/benjaminh83/fvm-calib-deal-miners>

&nbsp;

## Technical details

**Maintainer:** [ChainSafe](https://chainsafe.io)

#### **Genesis**:

- CAR File: `QmbHZuVjgtxvgtcE5H3FpE1ywEyawYmZcbx4Eh47WZ7YF8`
- Reset Timestamp: `2022-11-01T18:13:00Z`
- Genesis Block CID: `bafy2bzacecyaggy24wol5ruvs6qm73gjibs2l2iyhcqmvi7r7a4ph7zx3yqd4`
- sha1 Digest: `f9004d1266e0b023a018eb2fe6bb403cb8204df4`

#### **Network parameters**:

- Supported Sector Sizes: `32 GiB` and `64 GiB`
- Consensus Miner Min Power: `32 GiB`
- Epoch Duration Seconds: `30`
- Expected Leaders per Epoch: `5`
- WindowPoSt Proving Period: `2880`
- WindowPoSt Challenge Window: `60`
- WindowPoSt Period Deadlines: `48`
- Pre-Commit Challenge Delay: `150`

#### **Bootstrap peers**:

```
/dns/calibration.node.glif.io/tcp/1237/p2p/12D3KooWQPYouEAsUQKzvFUA9sQ8tz4rfpqtTzh2eL6USd9bwg7x
/dns/bootstrap-calibnet-0.chainsafe-fil.io/tcp/34000/p2p/12D3KooWABQ5gTDHPWyvhJM7jPhtNwNJruzTEo32Lo4gcS5ABAMm
/dns/bootstrap-calibnet-1.chainsafe-fil.io/tcp/34000/p2p/12D3KooWS3ZRhMYL67b4bD5XQ6fcpTyVQXnDe8H89LvwrDqaSbiT
/dns/bootstrap-calibnet-2.chainsafe-fil.io/tcp/34000/p2p/12D3KooWEiBN8jBX8EBoM3M47pVRLRWV812gDRUJhMxgyVkUoR48
/dns/bootstrap-archive-calibnet-0.chainsafe-fil.io/tcp/1347/p2p/12D3KooWLcRpEfmUq1fC8vfcLnKc1s161C92rUewEze3ALqCd9yJ
```

#### **Resources**:

- **Slack Channel for Updates:** [#fil-net-calibration-discuss](https://filecoinproject.slack.com/archives/C01D42NNLMS)
- **Network Status**: https://status.filecoin.io/
- **Calibration Docs**: [https://docs.filecoin.io/networks/calibration/details/](https://docs.filecoin.io/networks/calibration/details/)
- **Faucets**: 
  - <https://faucet.calibnet.chainsafe-fil.io>
    - This faucet currently emits 100 tFIL per request.
  - https://beryx.io/faucet
    - This faucet currently emits 5 tFIL per request every 12h.
- **Block Explorers**:
  - Beryx - [https://beryx.zondax.ch](https://beryx.zondax.ch) => select Calibration
  - Glif Explorer - [https://explorer.glif.io/?network=calibration](https://explorer.glif.io/?network=calibration)
  - Starboard - https://fvm.starboard.ventures/calibration/explorer
  - Filscan - [https://calibration.filscan.io/](https://calibration.filscan.io/)
- **RPC - Public Endpoints**:
  - See https://chainlist.org/chain/314159
  - **Glif Nodes RPC:**
    - https://api.calibration.node.glif.io/rpc/v1
    - web socket endpoint: wss://wss.calibration.node.glif.io/apigw/lotus/rpc/v1
    - For Lotus Lite use `FULLNODE_API_INFO=wss://wss.calibration.node.glif.io/apigw/lotus lotus daemon --lite`
- **Calibration Storage Providers (miners):**
  - See https://github.com/benjaminh83/fvm-calib-deal-miners - auto-accepts storage deals
- **SP Reputation Systems**
  - https://calibration.filrep.io
- **Filecoin CID Checker**:
  - [https://calibration.filecoin.tools/](https://calibration.filecoin.tools/) - check your storage deal or piece CID’s storage status
- **Calibration Fil+ Data Cap Requests**
  - Apply for Data Cap: <https://faucet.calibnet.chainsafe-fil.io>
    - (for Calibration only, on mainnet this is handled by https://filplus.storage/apply)
- **Zondax Filecoin Solidity Libs**
  - https://www.npmjs.com/package/@zondax/filecoin-solidity
  - https://github.com/Zondax/filecoin-solidity
  - https://github.com/Zondax/fevm-solidity-precompiles
- **Calibration Chain Index APIs**
  - https://beryx.zondax.ch/ 
    - API Docs: <https://docs.zondax.ch/beryx-api>
- **Calibration Chain Data**
  - http://calibration.filinfo.io/
- **MetaMask** (HowTo):
  - Open MetaMask and add a new network:
    - Name: Filecoin Calibration
    - RPC URL: https://api.calibration.node.glif.io/rpc/v1
    - ChainID: [**314159**](https://github.com/ethereum-lists/chains/blob/master/_data/chains/eip155-314159.json) (Filecoin - Calibration testnet)
    - Currency symbol: tFIL (Test FIL).
  - Create a new account in MetaMask to use with Filecoin.
  - (OPTIONAL - Go to any block explorer, and enter the account to see its native Filecoin f410 address.)
  - Use the [faucet](https://faucet.calibnet.chainsafe-fil.io) to draw funds to your 0x ir f410 address
  - Wait until the transaction gets processed by the network, and verify that the funds appear in MetaMask.
- **Docs and Developer Tools**:
  - [FVM Hackathon Cheatsheet](https://github.com/filecoin-project/community/discussions/585)
  - [Filecoin Hackathon Schedule](https://hackathons.filecoin.io/)
  - [Filecoin Docs on FVM](https://docs.filecoin.io/smart-contracts/fundamentals/the-filecoin-virtual-machine/)
- **Snapshots**
  - [Lightweight Calibration chain snapshot](https://forest-archive.chainsafe.dev/latest/calibnet/)

<hr>

