# Sochain Api

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## getAddress

-   **See: [https://sochain.com/api#get-display-data-address][1]
    **

Get address information.

### Parameters

-   `baseUrl` **[string][2]** The sochain node url.
-   `network` **[string][2]** 
-   `address` **[string][2]** 

Returns **LtcAddressDTO** 

## getTx

-   **See: [https://sochain.com/api#get-tx][3]
    **

Get transaction by hash.

### Parameters

-   `baseUrl` **[string][2]** The sochain node url.
-   `network` **[string][2]** network id
-   `hash` **[string][2]** The transaction hash.

Returns **Transactions** 

## getBalance

-   **See: [https://sochain.com/api#get-balance][4]
    **

Get address balance.

### Parameters

-   `baseUrl` **[string][2]** The sochain node url.
-   `network` **[string][2]** 
-   `address` **[string][2]** 

Returns **[number][5]** 

## getUnspentTxs

-   **See: [https://sochain.com/api#get-unspent-tx][6]
    **

Get unspent txs

### Parameters

-   `baseUrl` **[string][2]** The sochain node url.
-   `network` **[string][2]** 
-   `address` **[string][2]** 

Returns **LtcAddressUTXOs** 

## broadcastTx

-   **See: [https://sochain.com/api#send-transaction][7]
    **

Broadcast transaction.

### Parameters

-   `baseUrl` **[string][2]** The sochain node url.
-   `network` **[string][2]** 
-   `txHex` **[string][2]** 

Returns **[string][2]** Transaction ID.

## litecoinStats

Get Litecoin stats.

### Parameters

-   `baseUrl` **[string][2]** The sochain node url.

Returns **ChainStatsLtc** The Litecoin stats.

[1]: https://sochain.com/api#get-display-data-address

[2]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String

[3]: https://sochain.com/api#get-tx

[4]: https://sochain.com/api#get-balance

[5]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number

[6]: https://sochain.com/api#get-unspent-tx

[7]: https://sochain.com/api#send-transaction