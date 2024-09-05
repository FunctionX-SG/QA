# Token Factory

## Operating System for Testing
- **Web (H5)**
  - Primary Testing OS
- **Web (Desktop)**
  - Primary Testing OS
- **API**
  - Secondary Testing OS

## Test Data
- **Test Chains**
  - F(x)core
  - Zetachain
- **Wallets**
  - MetaMask
  - TrustWallet
  - f(x)Wallet
- **Contract Key Roles**
  - Admin
  - Minter
  - Pauser
  - Upgrader

## Test Scenarios

### Create Token Page
- **Positive Test Scenarios**
  - Correct values entered for Token Name, Symbol, Initial Supply; Token Decimals, Admin Address, Minter Address, Upgrader Address, and Pauser Address left blank, then Send
    - The connected wallet receives the corresponding token with 18 decimals.
  - Correct values entered for Token Name, Symbol, Initial Supply; Token Decimals set to 10, Admin Address, Minter Address, Upgrader Address, and Pauser Address left blank, then Send
    - The connected wallet receives the corresponding token with 10 decimals.
  - Correct values entered for Token Name, Symbol, Initial Supply; Token Decimals set to 10, Admin Address not the connected wallet address, Minter Address, Upgrader Address, and Pauser Address left blank, then Send
    - The specified wallet receives the corresponding token with 10 decimals.
  - All fields are filled, and each permission role is assigned equivalently
    - Each corresponding address has the appropriate result.
- **Negative Test Scenarios**
  - Token Name, Symbol, Initial Supply not filled, then Send
    - Required field warning
  - Correct values for Token Name, Symbol, Initial Supply, but no wallet connected, then Send
    - No wallet connected warning
  - Non-positive integer entered for Initial Supply, then Send
    - Type error handling
  - Non-positive integer entered for Symbols, then Send
    - Type error handling
  - Invalid addresses entered for roles, tested through equivalence partitioning
    - Address error handling
  - Insufficient Gas Fee scenarios
- **Boundary Test Scenarios**
  - Token Decimals precision boundary values

### Provide Token Details Page
- **Positive Test Scenarios**
  - Upload format: PNG, file size: less than 20KB, dimensions: 256x256 pixels
  - Website URL starts with `http://` or `https://`
  - Twitter Page URL starts with `http://` or `https://`
- **Negative Test Scenarios**
  - Upload format is not PNG
  - File size larger than 20KB
  - Image dimensions not 256x256 pixels
  - Website URL does not start with `http://` or `https://`
  - Twitter Page URL does not start with `http://` or `https://`

### Interact with Token Page
- **Positive Test Scenarios**
  - Query token balance with correct address that has a balance
  - Query token balance with correct address that has no balance
  - Burn tokens equal to or less than the connected wallet's balance
  - Mint tokens with correct amount and sender address
  - Transfer tokens equal to or less than the connected wallet's balance to a correct address
- **Negative Test Scenarios**
  - Query token balance with incorrect address
  - Burn tokens greater than the connected wallet's balance
  - Mint tokens with non-positive integer
  - Mint tokens to an invalid sender address
  - Transfer tokens greater than the connected wallet's balance
  - Transfer tokens to an invalid address
  - Insufficient Gas Fee scenarios
- **Boundary Test Scenarios**
  - Query token balance with the smallest unit of token decimals
  - Mint token amount with the smallest unit of token decimals
  - Burn token amount with the smallest unit of token decimals
  - Transfer token amount with the smallest unit of token decimals

### Role Management Page
- **Positive Test Scenarios**
  - Select correct Access Role and Wallet address, then Read
    - Result = True
  - Select correct Access Role and Wallet address, then Send for Grant roles
    - Wallet address is granted the specified role
  - Select correct Access Role and Wallet address, then Send for Renounce roles
    - Wallet address renounces the specified role
  - Select correct Access Role and Wallet address, then Send for Revoke roles
    - Wallet address revokes the specified role
- **Negative Test Scenarios**
  - Check wallet roles without selecting Access role, then Read
  - Check wallet roles without entering Wallet Address, then Read
  - Grant roles without selecting Access role, then Send
  - Grant roles without entering Wallet Address, then Send
  - Renounce roles without selecting Access role, then Send
  - Renounce roles without entering Wallet Address, then Send
  - Revoke roles without selecting Access role, then Send
  - Revoke roles without entering Wallet Address, then Send
  - Check wallet roles with incorrect Wallet Address, then Read
    - Result = False
  - Grant roles with incorrect Wallet Address, then Send
  - Renounce roles with incorrect Wallet Address, then Send
  - Revoke roles with incorrect Wallet Address, then Send
- **Equivalence Partitioning Test Scenarios**
  - Single wallet address possesses multiple roles
  - Single wallet address with multiple roles deletes a specific role
  - Single wallet address with multiple roles renounces a specific role
  - Single wallet address with multiple roles adds a specific role

### Setting Items
- **Positive Test Scenarios**
  - Successfully Connect Wallet
    - All setting items are visible
  - Copy Address
    - Clipboard address is correct
  - View QR Code
    - Correct QR code and address are displayed
  - View on Block Explorer
    - Redirects to the correct StarScan URL
  - Switch Network
    - Successfully switches network and updates assets accordingly
  - Disconnect Wallet
- **Negative Test Scenarios**
  - Connect Wallet fails
  - Switch Network fails

## Acceptance Criteria
- UI Validation
- Functional Validation
- Interface Validation
- On-Chain Data Validation
- Compatibility Validation