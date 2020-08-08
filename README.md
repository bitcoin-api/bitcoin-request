# bitcoin-request
Do Bitcoin Request on Bitcoin Node

[![npm version](https://badge.fury.io/js/bitcoin-request.svg)](https://badge.fury.io/js/bitcoin-request)

bitcoin-request - Do Bitcoin Request on Bitcoin Node


## About

Do Bitcoin Request on a Bitcoin Node. Set `process.env.BITCOIN_REQUEST_ENV` to the string `livenet` to make livenet requests to your Bitcoin node. Here's a list of commands you can use on your bitcoin node: [Chain Query list of commands for bitcoin-cli](https://chainquery.com/bitcoin-cli).


## Example

```.js
'use strict';

const bitcoinRequest = require( 'bitcoin-request' );


(async () => {

    const balance = await bitcoinRequest({

        command: [
            'getbalance'
        ],
        livenet: false, // overrides BITCOIN_REQUEST_ENV env setting
    });

    console.log( balance );

    // logs 0
})();
```