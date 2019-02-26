chainlog
========

![Imgur](https://i.imgur.com/U4R2agi.png)

A beautifully simple CLI to log Solidity smart contract interactions.

 * logs function calls and events
 * detects new deployments of contracts
 * connects to any Ethereum JSON-RPC provider

Developed as part of our [interchain bridging protocol, ohdex](https://github.com/liamzebedee/ohdex).

## Usage
NOTE: only works with solc-compiler output (not Truffle).

Configure `chainwatch.yml`:

```
rpcUrl: http://localhost:10000
contracts:
  artifacts: ./../../packages/contracts/build/artifacts/*.json
  addresses:
    - EventEmitter: '0x2559d11bbcaf82b35848876e0bd66eddc8c337e5'
    - EventEmitter: '0xa50aB77b35DF04AE960C393610158102fb63283a'
  watch_new: true
```

Then run `yarn start`.