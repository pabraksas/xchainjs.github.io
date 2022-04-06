# Crypto

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## generatePhrase

Generate a new phrase.

### Parameters

-   `size` **[string][1]** The new phrase size. (optional, default `12`)

Returns **[string][1]** The generated phrase based on the size.

## validatePhrase

Validate the given phrase.

### Parameters

-   `phrase` **[string][1]** 

Returns **[boolean][2]** `true` or `false`

## getSeed

Get the seed from the given phrase.

### Parameters

-   `phrase` **[string][1]** 


-   Throws **`"Invalid BIP39 phrase"`** Thrown if phrase is an invalid one.

Returns **[Buffer][3]** The seed from the given phrase.

## encryptToKeyStore

Get the Keystore interface from the given phrase and password.

### Parameters

-   `phrase` **[string][1]** 
-   `password` **[string][1]** 


-   Throws **`"Invalid BIP39 phrase"`** Thrown if phrase is an invalid one.

Returns **Keystore** The keystore interface generated from the given phrase and password.

## decryptFromKeystore

Get the phrase from the keystore

### Parameters

-   `keystore` **Keystore** 
-   `password` **[string][1]** 


-   Throws **`"Invalid password"`** Thrown if password is an incorrect one.

Returns **Keystore** The phrase from the keystore.

[1]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String

[2]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean

[3]: https://nodejs.org/api/buffer.html