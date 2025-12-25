# EncryptMultiple

Learn how to encrypt multiple values using FHE.fromExternal

## 🎓 What You'll Learn

This example teaches you how to use FHEVM to build privacy-preserving smart contracts. You'll learn step-by-step how to implement encrypted operations, manage permissions, and work with encrypted data.

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

## 📚 Overview

This example teaches you how to use FHEVM to build privacy-preserving smart contracts.

@title EncryptMultiple
@notice Encrypt and store multiple values using encrypted randomness
@dev Example demonstrating FHEVM encryption concepts



## 🔐 Learn Zama FHEVM Through This Example

This example teaches you how to use the following **Zama FHEVM** features:

### What You'll Learn About

- **ZamaEthereumConfig**: Inherits from Zama's network configuration
  ```solidity
  contract MyContract is ZamaEthereumConfig {
      // Inherits network-specific FHEVM configuration
  }
  ```

- **FHE Operations**: Uses Zama's FHE library for encrypted operations
  - `FHE.fromExternal()` - Zama FHEVM operation
  - `FHE.allowThis()` - Zama FHEVM operation
  - `FHE.xor()` - Zama FHEVM operation

- **Encrypted Types**: Uses Zama's encrypted integer types
  - `euint64` - 64-bit encrypted unsigned integer
  - `externalEuint64` - External encrypted value from user

- **Access Control**: Uses Zama's permission system
  - `FHE.allowThis()` - Allow contract to use encrypted values
  - `FHE.allow()` - Allow specific user to decrypt
  - `FHE.allowTransient()` - Temporary permission for single operation
  - `FHE.fromExternal()` - Convert external encrypted values to internal

### Zama FHEVM Imports

```solidity
// Zama FHEVM Core Library - FHE operations and encrypted types
import {FHE, euint64, externalEuint64} from "@fhevm/solidity/lib/FHE.sol";

// Zama Network Configuration - Provides network-specific settings
import {ZamaEthereumConfig} from "@fhevm/solidity/config/ZamaConfig.sol";
```

### Zama FHEVM Code Example

```solidity
// Handling user-provided encrypted values (Zama FHEVM)
euint64 internalValue = FHE.fromExternal(encryptedInput, inputProof);
FHE.allowThis(internalValue);

// Mixing with entropy using Zama FHEVM operations
euint64 entropy = entropyOracle.getEncryptedEntropy(requestId);
FHE.allowThis(entropy);
euint64 enhancedValue = FHE.xor(internalValue, entropy);
FHE.allowThis(enhancedValue);
```

### FHEVM Concepts You'll Learn

1. **External Encryption**: Learn how to use Zama FHEVM for external encryption
2. **Input Proofs**: Learn how to use Zama FHEVM for input proofs
3. **Permission Management**: Learn how to use Zama FHEVM for permission management
4. **Entropy Integration**: Learn how to use Zama FHEVM for entropy integration

### Learn More About Zama FHEVM

- 📚 [Zama FHEVM Documentation](https://docs.zama.org/protocol)
- 🎓 [Zama Developer Hub](https://www.zama.org/developer-hub)
- 💻 [Zama FHEVM GitHub](https://github.com/zama-ai/fhevm)



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
