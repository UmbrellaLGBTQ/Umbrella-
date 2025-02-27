# Umbrella-

# UMB Token - Smart Contract

## Overview
UMB Token is an **ERC-20 compliant** cryptocurrency built on the Ethereum blockchain. It includes advanced features such as transaction taxation, burning, pausing, and ownership control using OpenZeppelin libraries.

## Features
- **ERC-20 Standard**: Fully compliant with the Ethereum token standard.
- **Burnable**: Token holders can burn their tokens to reduce total supply.
- **Pausable**: The contract owner can pause transactions when necessary.
- **Tax Mechanism**: A transaction tax is applied, and funds are transferred to a designated collector.
- **Admin Controls**: The owner can modify tax settings, update the tax collector, and exclude addresses from taxation.

## Tokenomics
- **Token Name**: UMB Token  
- **Token Symbol**: UMB  
- **Decimals**: 18  
- **Maximum Supply**: 100,000,000 UMB  

## Smart Contract Details
- **Solidity Version**: `^0.8.4`
- **Libraries Used**:
  - OpenZeppelin `ERC20.sol`
  - OpenZeppelin `ERC20Burnable.sol`
  - OpenZeppelin `ERC20Pausable.sol`
  - OpenZeppelin `Ownable.sol`

## Installation & Deployment

### Prerequisites
Ensure you have the following installed:
- **Node.js** & **npm/yarn**
- **Hardhat** or **Truffle**
- **MetaMask** (for interacting with the contract)

### Steps to Deploy
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/umb-token.git
   cd umb-token
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Compile the smart contract:
   ```sh
   npx hardhat compile
   ```
4. Deploy the contract:
   ```sh
   npx hardhat run scripts/deploy.js --network rinkeby
   ```

## Functions
| Function | Description |
|----------|-------------|
| `setTransactionTax(uint256 _tax)` | Sets the transaction tax percentage (Max 10%) |
| `setTaxCollector(address _collector)` | Updates the tax collector address |
| `excludeFromTax(address account, bool status)` | Excludes an address from taxation |
| `burn(uint256 amount)` | Allows a user to burn their tokens |
| `pause()` | Pauses all token transfers |
| `unpause()` | Resumes token transfers |

## Security & Auditing
- Uses **OpenZeppelin** standards for security.
- Owner **cannot exceed 10% tax** to prevent abuse.
- **Pausable feature** ensures contract safety.

## License
This project is licensed under the **MIT License**.

## Contact
For inquiries, reach out to [Your Email] or visit [Your Website].
