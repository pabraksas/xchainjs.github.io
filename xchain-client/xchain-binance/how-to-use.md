---
sort: 2
---

# How to use

## Installation

```
yarn add @xchainjs/xchain-binance
```

Following peer dependencies have to be installed into your project. These are not included in `@xchainjs/xchain-binance`.

```
yarn add @binance-chain/javascript-sdk
```

## Binance Client Testing

```
yarn install
yarn test
```

## Create a client instance.

Set `phrase` and `network` when creating an instance.

```
const client = new Client({ phrase, network })
```

## Available functions

### Config and Setup

#### `setNetwork(net: Network): void`
Sets the network: `mainnet` or `testnet`.

#### `setPhrase(phrase: string): Address`
Sets the phrase. The phrase will be used to generate the address.

#### `getBncClient(): BncClient`
Returns the instance of [`binance-chain client`](https://github.com/binance-chain/javascript-sdk).

#### `getNetwork(): Network`
Returns the network: `mainnet` or `testnet`

#### `getAddress(): Address`
Returns the Address generated from the `BIP39` phrase.

It supports the [`BIP44 path derivations`](https://github.com/satoshilabs/slips/blob/master/slip-0044.md).

#### `validateAddress(address: string): boolean`
Checks if the address is valid.

### Explorer URL

#### `getExplorerUrl(): string`
Returns explorer URL.

#### `getExplorerAddressUrl(address: Address): string`
Returns explorer URL for the address.

#### `getExplorerTxUrl(txID: string): string`
Returns explorer URL for the transaction.

### Querying

#### `getBalance(address?: Address, asset?: Asset): Promise<Balances>`
Returns the balances of the address.

* `address` is optional, if not set, it will use the one generated from the phrase.
* `asset` is optional, if not set, it will return all balances of assets available.

#### `getTransactions(params?: TxHistoryParams): Promise<TxsPage>`
Returns a simplied array of recent transactions for an address. 

`params` is optional, if not set, it will return the latest transactions of the address generated from the phrase.

Following parameters are available:
* `address`: the address which will be used to fetch transctions
* `offset`: optional, used for the pagination
* `limit`: optional, used for the pagination
* `startTime`: optional, used for specifying the start time
* `asset`: optional, used for specifying a asset

#### `getTransactionData(txId: string): Promise<Tx>`
Returns a transaction information from the transaction ID/hash. 

### Get fee info

#### `getDefaultFees(): Promise<Fees>`
Returns default fees for normal transfer.

#### `getFees(): Promise<Fees>`
Returns fees for normal transfer.

#### `getMultiSendFees(): Promise<Fees>`
Returns fees for multi transfer.

### Transfer

#### `transfer(params: TxParams): Promise<TxHash>`
Used to send a normal transfer.

Following parameters are available:
* `asset`: optional, `AssetBNB` will be used by default
* `amount`: the amount of tokens that will be transfered
* `recipient`: the address that will send tokens to
* `memo`: optional, additional memo for the transaction

#### `multiSend(params: MultiSendParams): Promise<TxHash>`
Used to send a multi transfer.

Following parameters are available:
* `asset`: optional, `AssetBNB` will be used by default
* `transactions`: array of transfers. each transfer has the recipient address and the amount of tokens
* `memo`: optional, additional memo for the transaction

### Purge

#### `purgeClient(): void`

Used to remove `privateKey`, `phrase` and `address` from memory.