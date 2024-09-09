# Table of contents

* [Function X Technical Document](README.md)

## f(x)Core <a href="#fxcore" id="fxcore"></a>

* [What is f(x)Core](fxcore/what-is-fxcore.md)
* [Installation f(x)Core](fxcore/installation.md)
* [Setup Node](fxcore/setup-node/README.md)
  * [Full node with Binaries](fxcore/setup-node/full-node-with-binaries.md)
  * [Full node with Docker](fxcore/setup-node/full-node-with-docker.md)
  * [Snapshot Guide](fxcore/setup-node/use-snapshot.md)
  * [Node Monitoring Device](fxcore/setup-node/node-monitor.md)

## Validators

* [Validator Overview](validators/validator-overview.md)
* [Setting Up a Validator for f(x)Core](validators/validator-setup.md)
* [Validator Recovery](validators/validator-recovery.md)
* [Validator FAQ](validators/validator-faq.md)
* [Validator Security Notice](validators/validator-security-notice.md)
* [Migration Best Practices](validators/migration-best-practices.md)
* [Transfer Validator Permissions](validators/transfer-validator-permissions.md)

## Delegators

* [Delegators FAQ](delegators/delegators-faq.md)
* [Delegator CLI Guide](delegators/delegator-cli-guide.md)
* [Delegator Security Notice](delegators/delegator-security-notice.md)

## f(x)Core Tutorials <a href="#fxcore-tutorials" id="fxcore-tutorials"></a>

* [f(x)Cored CLI Commands](fxcore-tutorials/fxcored-commands-documentation.md)
* [Cloud Setup](fxcore-tutorials/cloud-setup.md)
* [Testnet faucet](fxcore-tutorials/testnet-faucet.md)
* [Ledger Integration for fxcored](fxcore-tutorials/ledger-integration-for-fxcored.md)
* [Sentry Nodes](fxcore-tutorials/sentry-nodes.md)
* [Account Migration Guide (CLI)](fxcore-tutorials/account-migration-guide.md)

## Upgrade Instructions

* [Cosmovisor Upgrade Guide v7.5.x](upgrade-instructions/cosmovisor/README.md)
  * [Cosmovisor Integration - Binaries](upgrade-instructions/cosmovisor/tutorial-binaries.md)
  * [Cosmovisor Integration - Docker](upgrade-instructions/cosmovisor/tutorial-docker.md)
* [Manual Upgrade Guide v7.5.x](upgrade-instructions/manual/README.md)
  * [Binaries - Upgrading Your Node](upgrade-instructions/manual/tutorial-binaries.md)
  * [Docker - Upgrading Your Node](upgrade-instructions/manual/tutorial-docker.md)
* [Upgrade Versions](upgrade-instructions/versions/README.md)
  * [v2.2.0 Upgrade Instructions](upgrade-instructions/versions/v2.2.0.md)
  * [v3.1.0 Upgrade Instructions](upgrade-instructions/versions/v3.1.0.md)
  * [v4.2.1 Upgrade Instructions](upgrade-instructions/versions/v4.2.1.md)
  * [v5.0.0 Upgrade Instructions](upgrade-instructions/versions/v5.0.0.md)
* [Upgrade FAQ](upgrade-instructions/upgrade-faq.md)

## Deploying on f(x)core EVM <a href="#deploying-on-fxcore-evm" id="deploying-on-fxcore-evm"></a>

* [Products](deploying-on-fxcore-evm/deployed-dapps.md)
* [MetaMask](deploying-on-fxcore-evm/metamask/README.md)
  * [Download and Install MetaMask](deploying-on-fxcore-evm/metamask/download-and-install-metamask.md)
  * [Add f(x)Core Network](deploying-on-fxcore-evm/metamask/add-fxcore-network.md)
  * [Configure Custom Tokens](deploying-on-fxcore-evm/metamask/configure-custom-tokens.md)
  * [Create and Import Accounts](deploying-on-fxcore-evm/metamask/create-and-import-accounts.md)
* [Connect Wallet to Dapps](deploying-on-fxcore-evm/connect-wallet-to-dapps/README.md)
  * [Connect using MetaMask](deploying-on-fxcore-evm/connect-wallet-to-dapps/connect-using-metamask.md)
  * [Connect using f(x)Wallet (Wallet Connect)](deploying-on-fxcore-evm/connect-wallet-to-dapps/connect-using-fxwallet-wallet-connect.md)
* [With Remix](deploying-on-fxcore-evm/with-remix.md)
* [With Truffle](deploying-on-fxcore-evm/with-truffle.md)
* [With Hardhat](deploying-on-fxcore-evm/with-hardhat.md)
* [Cross-Chain Bridges](deploying-on-fxcore-evm/cross-chain-bridges/README.md)
  * [Bridging Tokens from other networks](deploying-on-fxcore-evm/cross-chain-bridges/bridging-tokens-from-other-networks.md)
  * [f(x)Core Gravity Bridge](deploying-on-fxcore-evm/cross-chain-bridges/fxcore-gravity-bridge.md)

## DAPPS & INFRASTRUCTURE

* [Margin X Swap](dapps-and-infrastructure/fx-swap.md)
* [FX Wallet](dapps-and-infrastructure/fx-wallet.md)
* [PundiScan](dapps-and-infrastructure/pundiscan.md)
* [Baklava Space](dapps-and-infrastructure/baklava-space.md)
* [Safe Multisig](dapps-and-infrastructure/safe-multisig.md)
* [PortfolioX](dapps-and-infrastructure/portfoliox.md)
* [Token Factory](dapps-and-infrastructure/token-factory.md)

## Developers

* [f(x)Core Network](developers/network.md)
* [f(x)Core Modules](developers/modules.md)
* [f(x)Core JSON RPC](developers/jsonrpc-api.md)
* [f(x)Core REST API](developers/rest-api.md)
* [Web3 JSON RPC](developers/web3/README.md)
  * [JSON RPC Server](developers/web3/server.md)
  * [Namespaces](developers/web3/namespaces.md)
  * [JSON RPC Methods](developers/web3/endpoints.md)
  * [Events](developers/web3/events.md)
* [Support Keplr](developers/support-keplr.md)
* [Support Leap](developers/support-leap.md)
* [Third Party Price Oracles](developers/third-party-price-oracles.md)
* [Contract Deployments](developers/contract-deployments.md)
* [f(x)Core Cross Chain](developers/cross-chain/README.md)
  * [sendToFx](developers/cross-chain/send-to-fx.md)
  * [f(x)Core](developers/cross-chain/fx-core.md)
  * [ibc](developers/cross-chain/ibc.md)
  * [Target](developers/cross-chain/target.md)
* [Precompiled Contracts](developers/precompiles/README.md)
  * [CrossChain Precompiled](developers/precompiles/cross-chain.md)
  * [Staking Precompiled](developers/precompiles/staking.md)
  * [Staking-V2 Precompiled](developers/precompiles/staking-v2.md)
* [f(x)Core SDKs](developers/f-x-core-sdks/README.md)
  * [Python SDK](developers/f-x-core-sdks/python-sdk.md)
  * [JavaScript SDK](developers/f-x-core-sdks/javascript-sdk.md)
* [Contract Monitoring](developers/contract-monitoring.md)

## Governance

* [Governance Proposal Information](governance/governance-proposal-information/README.md)
  * [EGF Info](governance/governance-proposal-information/egf-info.md)
  * [EGF Grants Program](governance/governance-proposal-information/egf-grants-program.md)
  * [Application Template](governance/governance-proposal-information/application-template.md)
  * [Successful Grant Applicants](governance/governance-proposal-information/successful-grant-applicants.md)
  * [Launching an EGF Proposal](governance/governance-proposal-information/launching-an-egf-proposal.md)

***

* [Go to FunctionX](https://functionx.io)
