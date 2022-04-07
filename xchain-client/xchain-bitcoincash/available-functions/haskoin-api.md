# Haskoin Api

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## isErrorResponse

Check error response.

### Parameters

-   `response` **any** The api response.

Returns **[boolean][1]** 

## getAccount

Get account from address.

### Parameters

-   `$0` **[Object][2]** 
    -   `$0.haskoinUrl`  
    -   `$0.address`  
-   `haskoinUrl` **[string][3]** The haskoin API url.
-   `address` **[string][3]** The BCH address.


-   Throws **`"failed to query account by a given address"`** thrown if failed to query account by a given address

Returns **AddressBalance** 

## getTransaction

Get transaction by hash.

### Parameters

-   `$0` **[Object][2]** 
    -   `$0.haskoinUrl`  
    -   `$0.txId`  
-   `haskoinUrl` **[string][3]** The haskoin API url.
-   `txId` **[string][3]** The transaction id.


-   Throws **`"failed to query transaction by a given hash"`** thrown if failed to query transaction by a given hash

Returns **Transaction** 

## getRawTransaction

Get raw transaction by hash.

### Parameters

-   `$0` **[Object][2]** 
    -   `$0.haskoinUrl`  
    -   `$0.txId`  
-   `haskoinUrl` **[string][3]** The haskoin API url.
-   `txId` **[string][3]** The transaction id.


-   Throws **`"failed to query transaction by a given hash"`** thrown if failed to query raw transaction by a given hash

Returns **Transaction** 

## getTransactions

Get transaction history.

### Parameters

-   `$0` **[Object][2]** 
    -   `$0.haskoinUrl`  
    -   `$0.address`  
    -   `$0.params`  
-   `haskoinUrl` **[string][3]** The haskoin API url.
-   `address` **[string][3]** The BCH address.
-   `params` **TransactionsQueryParam** The API query parameters.


-   Throws **`"failed to query transactions"`** thrown if failed to query transactions

Returns **[Array][4]&lt;Transaction>** 

## getUnspentTransactions

Get unspent transactions.

### Parameters

-   `$0` **[Object][2]** 
    -   `$0.haskoinUrl`  
    -   `$0.address`  
-   `haskoinUrl` **[string][3]** The haskoin API url.
-   `address` **[string][3]** The BCH address.


-   Throws **`"failed to query unspent transactions"`** thrown if failed to query unspent transactions

Returns **[Array][4]&lt;TxUnspent>** 

## getSuggestedFee

Get suggested fee amount for Bitcoin cash. (fee per byte)

Returns **[number][5]** The Bitcoin cash stats.

## broadcastTx

-   **See: [https://app.swaggerhub.com/apis/eligecode/blockchain-api/0.0.1-oas3#/blockchain/sendTransaction][6]
    **

Broadcast transaction.

### Parameters

-   `params` **BroadcastTxParams** 
    -   `params.txHex`  
    -   `params.haskoinUrl`  

Returns **TxHash** Transaction hash.

[1]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean

[2]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object

[3]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String

[4]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array

[5]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number

[6]: https://app.swaggerhub.com/apis/eligecode/blockchain-api/0.0.1-oas3#/blockchain/sendTransaction