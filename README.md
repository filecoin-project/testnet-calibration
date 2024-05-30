# Calibration Testnet

Calibration was reset on Feb 19, 2021.

This page contains meta info for Filecoin developers about the Calibration testnet.

![spacex--p-KCm6xB9I-unsplash](https://github.com/filecoin-project/testnet-calibration/blob/ded02ebe39ab7e9dd76e8afef84d29245e53ea4c/spacex--p-KCm6xB9I-unsplash.jpg)
<br><sup><sub>photo by [SpaceX on Unsplash]([https://unsplash.com/@davidclode](https://unsplash.com/@spacex))<sup><sub>  


## Overview

The Filecoin Calibration testnet is a stable testnet that follows Filecoin mainnet closely. It has fewer resets and is intended for longer-term testing efforts from storage providers and developers.

- Like mainnet, Calibration supports `32 GiB`, and `64 GiB` storage sectors.
- It has a Storage Provider auto-accepting new deals from developers (see [Resources](#resources) - *Calibration Storage Providers* below).

## Join Quickstart

- **Build:** https://lotus.filecoin.io/lotus/manage/switch-networks/
- **Stats:** https://stats.calibration.fildev.network or see [Resources](#resources) - *Block Explorers* below
- **Faucet:** https://faucet.calibnet.chainsafe-fil.io
- **Snapshot:** https://snapshots.calibrationnet.filops.net/minimal/latest

## User Quickstart

1. Add the Calibration testnet to your wallet (e.g. MetaMask).
    - Go to https://chainlist.org/chain/314159
    - Click on "Connect wallet"
2. Create a new account in MetaMask to use with Filecoin.
3. Use [https://faucet.calibnet.chainsafe-fil.io/](https://faucet.calibnet.chainsafe-fil.io/) to request funds to your Ethereum address (it will be converted behind the scenes to a Filecoin f410 address)
4. Follow the transaction in one of the recommended Calibration testnet explorers:
    - https://calibration.filfox.info/en 
    - https://beryx.zondax.ch 
    - https://explorer.glif.io/?network=calibration
5. Your account is now funded and can be used in Ethereum tools such as Hardhat, Foundry, Remix, etc.

*Looking for a Storage Provider on Calibration?* - See https://github.com/benjaminh83/fvm-calib-deal-miners

&nbsp;

## Technical details

**Maintainer:** [Protocol Labs](https://protocol.ai)

#### **Genesis**:

- CAR File: `QmY581cXXtNwHweiC69jECupu9EBx274huHjSgxPNv1zAAj`
- Reset Timestamp: `2021-02-19T23:10:00Z`
- Genesis Block CID: `bafy2bzaceapb7hfdkewspic7udnogw4xnhjvhm74xy5snwa24forre5z4s2lm`
- sha1 Digest: `944c0c13172b9f552dfed5dfaffaba95113c8254`

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
/dns4/bootstrap-0.calibration.fildev.network/tcp/1347/p2p/12D3KooWRLZAseMo9h7fRD6ojn6YYDXHsBSavX5YmjBZ9ngtAEec
/dns4/bootstrap-1.calibration.fildev.network/tcp/1347/p2p/12D3KooWJFtDXgZEQMEkjJPSrbfdvh2xfjVKrXeNFG1t8ioJXAzv
/dns4/bootstrap-2.calibration.fildev.network/tcp/1347/p2p/12D3KooWP1uB9Lo7yCA3S17TD4Y5wStP5Nk7Vqh53m8GsFjkyujD
/dns4/bootstrap-3.calibration.fildev.network/tcp/1347/p2p/12D3KooWLrPM4WPK1YRGPCUwndWcDX8GCYgms3DiuofUmxwvhMCn
```

#### **Resources**:

- **Slack Channel for Updates:** [#fil-net-calibration-discuss](https://filecoinproject.slack.com/archives/C01D42NNLMS)

- **Network Status**: https://status.filecoin.io/
- **Calibration Docs**: [https://docs.filecoin.io/networks/calibration/details/](https://docs.filecoin.io/networks/calibration/details/)
- **Faucets**: 
  - [https://faucet.calibnet.chainsafe-fil.io/](https://faucet.calibnet.chainsafe-fil.io/)
    - This faucet currently emits 100 tFIL per request.
  - https://beryx.zondax.ch/faucet
- **Block Explorers**:
  - Filfox - [https://calibration.filfox.info/en](https://calibration.filfox.info/en)
  - Beryx - [https://beryx.zondax.ch](https://beryx.zondax.ch) => select Calibration
  - Glif Explorer - [https://explorer.glif.io/?network=calibration](https://explorer.glif.io/?network=calibration)
  - Starboard - [https://fvm.starboard.ventures/](https://fvm.starboard.ventures/) => select Calibration
  - Filscan - [https://calibration.filscan.io/](https://calibration.filscan.io/)
- **RPC - Public Endpoints**:
  - See https://chainlist.org/chain/314159
  - **Glif Nodes RPC:**
    - https://api.calibration.node.glif.io/rpc/v1
    - web socket endpoint: wss://wss.calibration.node.glif.io/apigw/lotus/rpc/v1
    - For Lotus Lite use `FULLNODE_API_INFO=wss://wss.calibration.node.glif.io/apigw/lotus lotus daemon --lite`
  - **ChainStack RPC:**
    - https://filecoin-calibration.chainstacklabs.com/rpc/v1
    - web socket endpoint: wss://ws-filecoin-calibration.chainstacklabs.com/rpc/v1
    - Info page: https://chainstack.com/labs/#filecoin
  - **Ankr RPC:**
    - https://rpc.ankr.com/filecoin_testnet
- **Calibration Storage Providers (miners):**
  - See https://github.com/benjaminh83/fvm-calib-deal-miners - auto-accepts storage deals
- **SP Reputation Systems**
  - https://calibration.filrep.io/ 
     - API example: https://api.calibration.filrep.io/api/v1/miners?region=Europe
- **Filecoin CID Checker**:
  - [https://calibration.filecoin.tools/](https://calibration.filecoin.tools/) - check your storage deal or piece CID’s storage status
- **Calibration Fil+ Data Cap Requests**
  - Apply for Data Cap: https://faucet.calibnet.chainsafe-fil.io/
    - (for Calibration only, on mainnet this is handled by https://filplus.storage/apply)
  - [Fil+ Data Cap Dashboard for Calibration](https://calibration.filplus.d.interplanetary.one/)
    - [API reference](https://documenter.getpostman.com/view/131998/Tzsim4NU#introhttps://documenter.getpostman.com/view/131998/Tzsim4NU#intro) but use http://api.calibration.filplus.d.interplanetary.one
- **Zondax Filecoin Solidity Libs**
  - https://www.npmjs.com/package/@zondax/filecoin-solidity
  - https://github.com/Zondax/filecoin-solidity
  - https://github.com/Zondax/fevm-solidity-precompiles
- **Calibration Chain Index APIs**
  - https://beryx.zondax.ch/ 
    - API Docs: https://docs.zondax.ch/Beryx
    - GraphQL UI: https://docs.zondax.ch/beryx/graphql
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
  - Use the [faucet](https://faucet.calibnet.chainsafe-fil.io/) to draw funds to your 0x ir f410 address
  - Wait until the transaction gets processed by the network, and verify that the funds appear in MetaMask.
- **Docs and Developer Tools**:
  - [FVM Hackathon Cheatsheet](https://github.com/filecoin-project/community/discussions/585)
  - [Filecoin Hackathon Schedule](https://hackathons.filecoin.io/)
  - [Filecoin Docs on FVM](https://docs.filecoin.io/smart-contracts/fundamentals/the-filecoin-virtual-machine/)
- **Snapshots**
  - [Lightweight Calibration chain snapshot](https://forest-archive.chainsafe.dev/latest/calibnet/)

<hr>

