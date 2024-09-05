# f(x) Wallet

## Testing OS
- APP (iOS)
  - Primary Testing OS
- APP (Android)
  - Primary Testing OS
- API
  - Primary Testing OS

## Testing Data
- Test Chains
  - f(x)core
  - PUNDI X
  - Ethereum
  - Avalanche
- Test Tokens
  - FX
  - PUNDIX
  - AVAX
  - ETH
  - USDT

## Test Scenarios
### Registration/Login
- **Create Wallet**
  - Successfully create wallet scenarios
- **Import Wallet**
  - Import 12 mnemonic words successfully
  - Import 12 mnemonic words failure scenarios
  - Import 24 mnemonic words successfully
  - Import 24 mnemonic words failure scenarios
  - Import non-12 or 24 mnemonic words failure scenarios
- **Register User**
  - Successful user registration scenario
  - Incorrect E-mail format warning
  - Incorrect password format warning
  - Duplicate user registration failure scenario

### Wallet
- **Chains**
  - Switch different chain scenarios
  - Add new wallet address scenario
  - Various chain network switch scenarios
  - Manually add chain link successfully
  - Manually add chain link failure
  - Enable chain link scenario
  - Cancel enabling chain link scenario
- **Assets**
  - Switch between different chain links and wallet addresses scenarios
  - Asset address confirmation
  - Total asset conversion confirmation
  - Asset chain explorer confirmation
  - Asset address QR code sharing functionality confirmation
  - Asset address QR code copy functionality confirmation
  - Wallet asset list information (icon, chain name, environment, address, amount) confirmation
  - Wallet NFT list information confirmation (OpenSea)
  - Add asset from the recommended list scenario
  - Manually import Token contract address correctly scenario
  - Manually import Token contract address incorrectly scenario
  - Automatic asset scan scenario
  - Delete asset scenario
  - Adjust asset sorting scenario
- **Transactions**
  - Normal same-chain transaction success scenario
  - Incorrect address transaction failure scenario
  - Different-chain address transaction failure scenario
  - Transaction failure scenario with more than asset amount
  - Adjust Gas fee successfully scenario
  - Input incorrect Gas fee failure scenario
  - Add common contact address successfully scenario
  - Add common contact address failure scenario
  - Change transaction currency calculation scenario
  - (Capture each step of the transaction for corresponding UI and function test cases)

### Notification Center
- **All Addresses**
  - Outbound notification
  - Inbound notification
- **Specific Addresses**
  - Outbound notification
  - Inbound notification

### f(x)DAPP
- f(x)Core Delegate
- PUNDI X Delegate
- f(x)Core Classic Delegate
- MarginX
  - Swap, Pool, Farm, Dashboard, Bridge page functionalities working correctly
  - Click DAPP to import the correct corresponding DAPP address
- Portfolio X
  - Asset Dashboard, Wallet, Portfolio, Defi Snapshot page functionalities working correctly
  - Click DAPP to import the correct corresponding DAPP address
- f(x)Core Proposals
  - Proposal list
  - Reject proposal
  - Approve proposal
- Crypto Gift
  - Gift currency sending
    - Can see the supported currencies (e.g., BNB, PURSE, MATIC)
  - Send gifts
    - Successfully send corresponding currency
  - Gift management
    - View received and sent gift records
- f(x) Bridge
  - **Positive Test Scenarios**
    - Transfer 25% of assets from chain A to chain B
    - Transfer 50% of assets from chain A to chain B
    - Transfer 75% of assets from chain A to chain B
    - Transfer MAX assets from chain A to chain B
  - **Negative Test Scenarios**
    - Transfer assets with value 0 from chain A to chain B
      - Cross-chain transaction not established
  - **Boundary Test Scenarios**
    - Transfer maximum precision value from chain A to chain B
      - Cross-chain transaction successful

### Non-f(x)DAPP
- Various DAPPs
  - UI and text descriptions displayed correctly
  - Click DAPP to import the correct corresponding DAPP address

### Settings
- **User**
  - Change wallet name successfully scenario
  - Change wallet name failure scenario
- **Security**
  - Enable TouchID/FaceID scenario
  - Disable TouchID/FaceID scenario
  - Change password scenario
  - Reset wallet scenario
  - Enable account protection scenario
  - Disable account protection scenario
- **Backup**
  - View and backup wallet mnemonic phrase scenario
- **Address Book**
  - Add common contact address successfully scenario
  - Add common contact address failure scenario
  - Edit common contact address successfully scenario
  - Edit common contact address failure scenario
  - Edit common contact address name successfully scenario
  - Edit common contact address name failure scenario
  - Delete common contact address scenario
- **NFT Blacklist**
  - View blacklist NFT list (NFT hide function)
- **Toggle Address Type**
  - Confirm change of Bitcoin address path type
- **Language**
  - Language list confirmation
  - Change language and corresponding UI text confirmation
- **Fiat Currency**
  - Fiat currency list confirmation
  - Change fiat currency setting and asset value confirmation
- **Notifications**
  - Turn notifications on and off confirmation
  - Confirm different notification types
- **Node Settings**
  - Switch different chain scenarios
  - Various chain network switch scenarios
  - Manually add chain link successfully
  - Manually add chain link failure
  - Enable chain link scenario
  - Cancel enabling chain link scenario
- **Support Center**
  - Click to jump to related articles confirmation
- **Create Request**
  - Click to jump to customer service chat confirmation
- **About f(x)wallet**
  - Click to view user agreement, version, official website, Twitter, write a review

## Acceptance Criteria
- UI Verification
- Function Verification
- Interface Verification
- On-chain Data Verification
- Compatibility Verification
- Performance Verification