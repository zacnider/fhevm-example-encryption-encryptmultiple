# EncryptMultiple

Encrypt and store multiple values using EntropyOracle

## 🚀 Quick Start

1. **Clone this repository:**
   ```bash
   git clone https://github.com/zacnider/fhevm-example-encryption-encryptmultiple.git
   cd fhevm-example-encryption-encryptmultiple
   ```

2. **Install dependencies:**
   ```bash
   npm install --legacy-peer-deps
   ```

3. **Setup environment:**
   ```bash
   npm run setup
   ```
   Then edit `.env` file with your credentials:
   - `SEPOLIA_RPC_URL` - Your Sepolia RPC endpoint
   - `PRIVATE_KEY` - Your wallet private key (for deployment)
   - `ETHERSCAN_API_KEY` - Your Etherscan API key (for verification)

4. **Compile contracts:**
   ```bash
   npm run compile
   ```

5. **Run tests:**
   ```bash
   npm test
   ```

6. **Deploy to Sepolia:**
   ```bash
   npm run deploy:sepolia
   ```

7. **Verify contract (after deployment):**
   ```bash
   npm run verify <CONTRACT_ADDRESS>
   ```

**Alternative:** Use the [Examples page](https://entrofhe.vercel.app/examples) for browser-based deployment and verification.

---

## 📋 Overview

@title EncryptMultiple
@notice Encrypt and store multiple values using EntropyOracle
@dev Example demonstrating FHEVM encryption concepts



## 🔍 Contract Code

```solidity
// SPDX-License-Identifier: BSD-3-Clause-Clear
pragma solidity ^0.8.27;

import {FHE, euint64, externalEuint64} from "@fhevm/solidity/lib/FHE.sol";
import {ZamaEthereumConfig} from "@fhevm/solidity/config/ZamaConfig.sol";

/**
 * @title EncryptMultiple
 * @notice Encrypt and store multiple values using EntropyOracle
 * @dev Example demonstrating FHEVM encryption concepts
 */
contract EncryptMultiple is ZamaEthereumConfig {
    // TODO: Add your contract implementation here
    
    constructor() {
        // TODO: Initialize your contract
    }
    
    // TODO: Add your functions here
}

```

## 🧪 Tests

See [test file](./test/EncryptMultiple.test.ts) for comprehensive test coverage.

```bash
npm test
```


## 📚 Category

**encryption**



## 🔗 Related Examples

- [All encryption examples](https://github.com/zacnider/entrofhe/tree/main/examples)

## 📝 License

BSD-3-Clause-Clear
