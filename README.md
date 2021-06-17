# @lto-network/lto-marshall [![npm version](https://badge.fury.io/js/%40lto-network%2Flto-marshall.svg)](https://badge.fury.io/js/%40lto-network%2Flto-marshall) [![Build Status](https://travis-ci.com/ltonetwork/lto-marshall.svg?branch=master)](https://travis-ci.com/ltonetwork/lto-marshall)

Marshall can serialize and parse LTO blockchain data structures

# Note

> This package has been **deprecated.** It has since been merged with [@lto-network/lto-transactions](https://github.com/ltonetwork/lto-transactions), as a folder: `parseSerialize`. This repository will *no longer be maintained.*

---

### Includes:
- Serialization primitives
- Parsing primitives
- Binary to js converters
- Js to binary converters
- JSON to js converters
- Js to JSON converters

### Usage:
```javascript
import { binary, json } from 'parse-serialize'

const tx = {
  type: 4,
  version: 2,
  fee: 100000,
  senderPublicKey: '7GGPvAPV3Gmxo4eswmBRLb6bXXEhAovPinfcwVkA2LJh',
  timestamp: 1542539421461,
  proofs:
  ['22J76sGhLRo3S5pkqGjCi9fijpEeGGRmnv7canxeon2n2MNx1HhvKaBz2gYTdpJQohmUusRKR3yoCAHptRnJ1Fwe'],
  id: 'EG3WvPWWEU5DdJ7xfB3Y5TRJNzMpt6urgKoP7docipvW',
  recipient: '3N3Cn2pYtqzj7N9pviSesNe8KG9Cmb718Y1',
  amount: 10000,
  attachment: '',
};

// Binary converter
const bytes = binary.serializeTx(tx);

const txb = binary.parseTx(bytes)

// json converted
const jsonString = json.stringifyTx(tx)

const txj = json.parseTx(jsonString)

```
