# MarginX

## Testing OS

### APP (iOS)

- Primary testing OS

### APP (Android)

- Primary testing OS

### Web (H5)

- Primary testing OS

### Web (Desktop)

- Primary testing OS

### API

- Primary testing OS

## Test Data

### Test Chains

- f(x)core
- ZetaChain
- BSC
- Polygon
- Ethereum

### Wallet

- MetaMask
- TrustWallet
- f(x)Wallet
- OKX Wallet

### Test Tokens

- FX
- Zeta
- USDC
- USDT
- BNB
- POL
- ETH

## Test Scenarios

### Swap

- Setup

  - Positive Test Scenarios
    - Slippage tolerance input greater than or equal to zero
      - Complete the transaction within the set slippage tolerance, or the transaction will be canceled.
    - Slippage tolerance input greater than 1
      - A prompt will appear indicating the transaction will prioritize completion.
    - Slippage tolerance set to Auto
      - The system automatically sets the optimal slippage percentage and completes the transaction.
    - No Slippage tolerance value entered
      - The system automatically selects Auto.
    - Transaction deadline input greater than 1
      - Complete the transaction within the set minutes, or the transaction will be canceled.
    - No Transaction deadline value entered
      - The system defaults to 30 minutes.
    - Toggle Expert Mode set to True
      - A two-step confirmation appears, skipping the confirmation screen and resulting in higher slippage tolerance.
    - Disable Multihops set to True
      - Tokens are swapped directly within the pair.

  - Negative Test Scenarios
    - Slippage tolerance input less than zero
      - Invalid setup prompt.
    - Slippage tolerance input of 0
      - A warning appears indicating potential transaction failure.
    - Slippage tolerance input greater than 50
      - Invalid setup prompt.
    - Transaction deadline input less than 1
      - Invalid setup prompt.
    - Transaction deadline input greater than 180
      - Invalid setup prompt.

  - Boundary Test Scenarios
    - Slippage tolerance input with more than two decimal places
      - The system automatically discards values beyond two decimal places.

- Source Tokens

  - Positive Test Scenarios
    - Input token amount less than the balance
      - The transaction can proceed.
    - Select Max for token amount
      - The transaction amount is set to the maximum held amount.
    - Click the token
      - Displays the search box, suggested tokens for exchange, and a token list.
    - Enter the correct token keyword in the search box
      - The corresponding token is displayed.
    - Enter the correct token contract address in the search box
      - The corresponding token is displayed.
    - Click any suggested token for exchange
      - Successfully changes the token pair.
    - Click Manage Token List
      - Displays the toggle for switching tokens, list search box, and token search box.
    - Select a list in Manage Token List
      - Displays the list search box and token list.
    - Enter the correct URL in the List search box
      - The corresponding list is displayed.
    - Enter the correct ENS name in the List search box
      - The corresponding list is displayed.
    - Set any list to On in Manage Token List
      - All tokens from that list are displayed.
    - Set any list to Off in Manage Token List
      - Tokens from that list are hidden.
    - Delete any list in Manage Token List
      - Tokens from that list cannot be selected.
    - Click View List in Manage Token List
      - Redirects to the list page on [tokenlists.org](https://tokenlists.org/).
    - Select Tokens in Manage Token List
      - Displays the search box for contract addresses and corresponding tokens.
    - Enter the correct contract address in the search box
      - The corresponding token is displayed along with an import button.
    - Import a token after entering the correct contract address
      - The token is added to the list.
    - Enter the contract address of an already imported token
      - The token’s status and information are displayed.
    - Delete any imported token
      - The token cannot be selected from the list.
    - Click Clear All in Tokens
      - All imported tokens are removed from the list.

  - Negative Test Scenarios
    - Input token amount greater than the balance
      - Insufficient balance warning appears.
    - Select a token not owned by the wallet
      - Insufficient balance warning appears.
    - Enter an incorrect token keyword in the search box
      - No token found warning appears.
    - Enter an incorrect token contract address in the search box
      - No token found warning appears.
    - Enter an incorrect URL in List search box
      - No list found warning appears.
    - Enter an incorrect ENS name in List search box
      - No list found warning appears.
    - Enter an incorrect contract address in the search box
      - No token found warning appears.

  - Boundary Test Scenarios
    - Token amount input with maximum precision.

- Swap Tokens

  - Positive Test Scenarios
    - Input token amount less than the balance
      - The transaction can proceed.
    - Select Max for token amount
      - The transaction amount is set to the maximum held amount.
    - Click the token
      - Displays a search box, suggested tokens for exchange, and a token list.
    - Enter the correct token keyword in the search box
      - The corresponding token is displayed.
    - Enter the correct token contract address in the search box
      - The corresponding token is displayed.
    - Click any suggested token for exchange
      - Successfully changes the token pair.
    - Click Manage Token List
      - Displays the toggle for switching tokens, list search box, and token search box.
    - Select a list in Manage Token List
      - Displays the list search box and token list.
    - Enter the correct URL in the List search box
      - The corresponding list is displayed.
    - Enter the correct ENS name in the List search box
      - The corresponding list is displayed.
    - Set any list to On in Manage Token List
      - All tokens from that list are displayed.
    - Set any list to Off in Manage Token List
      - Tokens from that list are hidden.
    - Delete any list in Manage Token List
      - Tokens from that list cannot be selected.
    - Click View List in Manage Token List
      - Redirects to the list page on [https://tokenlists.org](https://tokenlists.org).
    - Select Tokens in Manage Token List
      - Displays a search box for contract addresses and corresponding tokens.
    - Enter the correct contract address in the search box
      - The corresponding token is displayed along with an import button.
    - Import a token after entering the correct contract address
      - The token is added to the list.
    - Enter the contract address of an already imported token
      - The token’s status and information are displayed.
    - Delete any imported token
      - The token cannot be selected from the list.
    - Click Clear All in Tokens
      - All imported tokens are removed from the list.

  - Negative Test Scenarios
    - Input token amount greater than the balance
      - Insufficient balance warning appears.
    - Enter an incorrect token keyword in the search box
      - No token found warning appears.
    - Enter an incorrect token contract address in the search box
      - No token found warning appears.
    - Enter an incorrect URL in List search box
      - No list found warning appears.
    - Enter an incorrect ENS name in List search box
      - No list found warning appears.
    - Enter an incorrect contract address in the search box
      - No token found warning appears.

  - Boundary Test Scenarios
    - Input token amounts with maximum precision.

- Swap Functionality

  - Positive Test Scenarios
    - Input a value within the asset for the source token
      - The system automatically calculates the equivalent amount for the swap token and displays the exchange rate.
    - Input a value within the asset for the source token but no swap token selected
      - A prompt to select the swap token appears.
    - Click the "V" (swap) button
      - The source token and swap token are exchanged.
    - Select FX as the source token and proceed with Swap
      - The chosen amount of swap token is received.
    - Select a non-FX token as the source token and perform the first Swap
      - Redirects to the wallet protocol agreement page.
    - Select a non-FX token as the source token and perform a subsequent Swap
      - The chosen amount of swap token is received.
    - After Swap is successful
      - Assets are updated, and the screen displays:
        1. "View on FX StarScan" button
        2. "Add Token to Wallet" button
        3. "Close" button.
    - After Swap is successful, click "View on FX StarScan"
      - Redirects to FX StarScan and displays the transaction details.
    - After Swap is successful, click "Add to Wallet"
      - The swap token is added to the linked wallet.

  - Negative Test Scenarios
    - The source token and swap token have no liquidity
      - A warning appears indicating no liquidity for the token pair.
    - After a failed Swap
      - Assets remain unchanged.

### Pool

- Create a Pair & Add Liquidity

  - Setup

    - Positive Test Scenarios
      - Slippage tolerance input greater than or equal to zero
        - Complete the transaction within the set slippage tolerance, or the transaction will be canceled.
      - Slippage tolerance input greater than 1
        - A prompt will appear indicating the transaction will prioritize completion.
      - Slippage tolerance set to Auto
        - The system automatically sets the optimal slippage percentage and completes the transaction.
      - No Slippage tolerance value entered
        - The system automatically selects Auto.
      - Transaction deadline input greater than 1
        - Complete the transaction within the specified minutes, or the transaction will be canceled.
      - No Transaction deadline value entered
        - The system defaults to 30 minutes.
      - Toggle Expert Mode set to True
        - A two-step confirmation appears, skipping the confirmation screen and resulting in higher slippage tolerance.
      - Disable Multihops set to True
        - Tokens are swapped directly within the pair.

    - Negative Test Scenarios
      - Slippage tolerance input less than zero
        - Invalid setup prompt.
      - Slippage tolerance input of 0
        - A warning appears indicating potential transaction failure.
      - Slippage tolerance input greater than 50
        - Invalid setup prompt.
      - Transaction deadline input less than 1
        - Invalid setup prompt.
      - Transaction deadline input greater than 180
        - Invalid setup prompt.

    - Boundary Test Scenarios
      - Slippage tolerance input with more than two decimal places
        - The system automatically discards values beyond two decimal places.

  - Source Token A

    - Positive Test Scenarios
      - Input token amount less than the balance
        - The transaction can proceed.
      - Select Max for token amount
        - The transaction amount is set to the maximum held amount.
      - Click the token
        - Displays the search box, suggested tokens for exchange, and a token list.
      - Enter the correct token keyword in the search box
        - The corresponding token is displayed.
      - Enter the correct token contract address in the search box
        - The corresponding token is displayed.
      - Click any suggested token for exchange
        - Successfully changes the token pair.
      - Click Manage Token List
        - Displays the toggle for switching tokens, list search box, and token search box.
      - Select a list in Manage Token List
        - Displays the list search box and token list.
      - Enter the correct URL in the List search box
        - The corresponding list is displayed.
      - Enter the correct ENS name in the List search box
        - The corresponding list is displayed.
      - Set any list to On in Manage Token List
        - All tokens from that list are displayed.
      - Set any list to Off in Manage Token List
        - Tokens from that list are hidden.
      - Delete any list in Manage Token List
        - Tokens from that list cannot be selected.
      - Click View List in Manage Token List
        - Redirects to the list page on [https://tokenlists.org](https://tokenlists.org).
      - Select Tokens in Manage Token List
        - Displays a search box for contract addresses and corresponding tokens.
      - Enter the correct contract address in the search box
        - The corresponding token is displayed along with an import button.
      - Import a token after entering the correct contract address
        - The token is added to the list.
      - Enter the contract address of an already imported token
        - The token’s status and information are displayed.
      - Delete any imported token
        - The token cannot be selected from the list.
      - Click Clear All in Tokens
        - All imported tokens are removed from the list.

    - Negative Test Scenarios
      - Input token amount greater than the balance
        - Insufficient balance warning appears.
      - Select a token not owned by the wallet
        - Insufficient balance warning appears.
      - Enter an incorrect token keyword in the search box
        - No token found warning appears.
      - Enter an incorrect token contract address in the search box
        - No token found warning appears.
      - Enter an incorrect URL in the List search box
        - No list found warning appears.
      - Enter an incorrect ENS name in the List search box
        - No list found warning appears.
      - Enter an incorrect contract address in the search box
        - No token found warning appears.

    - Boundary Test Scenarios
      - Input token amounts with maximum precision.

  - Source Token B

    - Positive Test Scenarios
      - Input token amount less than the balance
        - The transaction can proceed.
      - Select Max for token amount
        - The transaction amount is set to the maximum held amount.
      - Click the token
        - Displays the search box, suggested tokens for exchange, and a token list.
      - Enter the correct token keyword in the search box
        - The corresponding token is displayed.
      - Enter the correct token contract address in the search box
        - The corresponding token is displayed.
      - Click any suggested token for exchange
        - Successfully changes the token pair.
      - Click Manage Token List
        - Displays the toggle for switching tokens, list search box, and token search box.
      - Select a list in Manage Token List
        - Displays the list search box and token list.
      - Enter the correct URL in the List search box
        - The corresponding list is displayed.
      - Enter the correct ENS name in the List search box
        - The corresponding list is displayed.
      - Set any list to On in Manage Token List
        - All tokens from that list are displayed.
      - Set any list to Off in Manage Token List
        - Tokens from that list are hidden.
      - Delete any list in Manage Token List
        - Tokens from that list cannot be selected.
      - Click View List in Manage Token List
        - Redirects to the list page on [https://tokenlists.org](https://tokenlists.org).
      - Select Tokens in Manage Token List
        - Displays a search box for contract addresses and corresponding tokens.
      - Enter the correct contract address in the search box
        - The corresponding token is displayed along with an import button.
      - Import a token after entering the correct contract address
        - The token is added to the list.
      - Enter the contract address of an already imported token
        - The token’s status and information are displayed.
      - Delete any imported token
        - The token cannot be selected from the list.
      - Click Clear All in Tokens
        - All imported tokens are removed from the list.

    - Negative Test Scenarios
      - Input token amount greater than the balance
        - Insufficient balance warning appears.
      - Select a token not owned by the wallet
        - Insufficient balance warning appears.
      - Enter an incorrect token keyword in the search box
        - No token found warning appears.
      - Enter an incorrect token contract address in the search box
        - No token found warning appears.
      - Enter an incorrect URL in the List search box
        - No list found warning appears.
      - Enter an incorrect ENS name in the List search box
        - No list found warning appears.
      - Enter an incorrect contract address in the search box
        - No token found warning appears.

    - Boundary Test Scenarios
      - Input token amounts with maximum precision.

  - Create a Pair

    - Positive Test Scenarios
      - Access the "Create a Pair" page
        - Displays the non-set Source Tokens A and B, along with the input fields.
      - Input token amounts within the balance for both A and B, but do not approve either
        - "Approve A" and "Approve B" buttons are shown.
      - Input token amounts within the balance for both A and B, but do not approve A
        - "Approve A" button is shown.
      - Input token amounts within the balance for both A and B, but do not approve B
        - "Approve B" button is shown.
      - Input token amounts within the balance for both A and B, and approve both
        - You can directly click "Supply" and view the Initial prices and pool share values.
      - Input token amounts within the balance for both A and B, approve both, and click Supply
        - Liquidity is successfully added, and assets are updated. The screen displays:
          1. "View on FX StarScan" button
          2. "Close" button.
      - After adding liquidity, click "View on FX StarScan"
        - Redirects to FX StarScan and displays the transaction details.
      - After successfully adding liquidity
        - You can view the position details of the liquidity pair.

    - Negative Test Scenarios
      - No tokens selected for either A or B
        - An "Invalid pair" prompt appears.
      - No token selected for A
        - An "Invalid pair" prompt appears.
      - No token selected for B
        - An "Invalid pair" prompt appears.
      - A and B tokens are selected but no amounts are entered
        - A prompt to input an amount appears.
      - Token A is selected but no amount is entered
        - A prompt to input an amount appears.
      - Token B is selected but no amount is entered
        - A prompt to input an amount appears.

    - Boundary Test Scenarios
      - Token A and B values entered at maximum precision.

  - Add Liquidity

    - Positive Test Scenarios
      - Access the "Add Liquidity" page
        - The following elements are displayed:
          1. A non-set Source Token B
          2. Source Token A set to FX
          3. Input fields for adding liquidity.
      - Input token amounts within the balance for both A and B, but do not approve either
        - "Approve A" and "Approve B" buttons are shown.
      - Input token amounts within the balance for both A and B, but do not approve A
        - "Approve A" button is shown.
      - Input token amounts within the balance for both A and B, but do not approve B
        - "Approve B" button is shown.
      - Input token amounts within the balance for both A and B, and approve both
        - You can directly click "Supply" and view the Initial prices and pool share values.
      - Input token amounts within the balance for both A and B, approve both, and click Supply
        - Liquidity is successfully added, and assets are updated. The screen displays:
          1. "View on FX StarScan" button
          2. "Close" button
          3. LP Tokens are issued.
      - After adding liquidity, click "View on FX StarScan"
        - Redirects to FX StarScan and displays the transaction details.
      - After successfully adding liquidity
        - You can view the position details of the liquidity pair.

    - Negative Test Scenarios
      - No token selected for B
        - An "Invalid pair" prompt appears.
      - A and B tokens are selected but no amounts are entered
        - A prompt to input an amount appears.
      - Token A is selected but no amount is entered
        - A prompt to input an amount appears.
      - Token B is selected but no amount is entered
        - A prompt to input an amount appears.

    - Boundary Test Scenarios
      - Token A and B values entered at maximum precision.

- Import Pool

  - Positive Test Scenarios
    - Token A and B liquidity is created but not yet imported
      - Automatically imports to the "Your Liquidity" page
    - Token A and B liquidity is created and already imported
      - You can see the position details of the liquidity for this trading pair. Click "Manage this pool" to enter the "Your Liquidity" page.

  - Negative Test Scenarios
    - No external liquidity for Token A and B
      - "You don’t have liquidity in this pool yet." Click "Add liquidity" to enter the add liquidity page.
    - No liquidity for Token A, but Token B has liquidity
      - "No pool found" warning. Click "Create pool" to enter the add liquidity page.
    - No liquidity for Token B, but Token A has liquidity
      - "No pool found" warning. Click "Create pool" to enter the add liquidity page.
    - Token B not selected
      - Prompts to select Token B.

- Your Liquidity

  - Positive Test Scenarios
    - A pool with newly added token liquidity
      - Displays pools of trading pairs with liquidity.
    - Select any pool and click "Manage"
      - Shows pool details and "Add" & "Remove" buttons.
    - Select any pool, click "Manage," and then click "Add"
      - Enters the add liquidity page with tokens auto-filled.
    - Select any pool, click "Manage," and then click "Remove"
      - Enters the remove liquidity page with tokens auto-filled.
    - Enter the remove liquidity page, and if the trading pair is not approved for liquidity
      - Needs to approve first before proceeding with "Remove."
    - Enter the remove liquidity page, and if the trading pair is approved for liquidity
      - Can proceed with "Remove."
    - Enter the remove liquidity page, select an amount greater than 0 up to Max, and proceed with "Remove"
      - Removes the corresponding liquidity provided for Tokens A and B.
      
  - Negative Test Scenarios
    - No pools with newly added token liquidity
      - No token liquidity prompt.
    - Enter the remove liquidity page without inputting a removal amount
      - Prompts to enter an amount.
      
  - Equivalence Partitioning Scenarios
    - Enter the remove liquidity page and click "Detailed" to switch between Token A and B.
    - Enter the remove liquidity page and click "Detailed" to change the amount for Token A and B.

### Farm

- Farm List

  - Positive Test Scenarios

    - Enter the Farm page

      - You can see the feature description, search function, list of liquidity that can be staked, and related data.

    - Use the search function and select "Sort by Total Deposited"

      - Sorts by Total Deposited amount in descending order.

    - Use the search function and select "Sort by APR%"

      - Sorts by APR% in descending order.

    - Enter token keyword in the search field

      - Performs a fuzzy search and displays trading pairs containing the keyword.

  - Negative Test Scenarios

    - Enter a non-existing keyword in the search field

      - Displays "No items found" warning.

  - Equivalence Partitioning Scenarios

    - Different search conditions with "Sort" and keyword search in the search function.

- Farm

  - Positive Test Scenarios

    - If the selected trading pair has added liquidity but is not staked, click "Deposit"

      - You can see the stake token button and related staking data for the trading pair, but it does not show the staked amount and reward data.

    - If the selected trading pair has added liquidity but is not staked, click "Deposit" and stake LP Tokens

      - Displays: 1. Amount available for staking 2. Related staking data 3. "Max" button 4. "Approve" button 5. "Deposit" button.

    - Enter an LP Token amount less than the balance when staking

      - Can proceed with staking.

    - Click the "Max" button when staking

      - Automatically fills in the maximum amount available for staking.

    - Enter an LP Token amount less than the balance and click "Approve" when staking

      - "Deposit" button becomes clickable.

    - After completing the staking process

      - Liquidity for this trading pair cannot be changed or LP Tokens redeemed.

    - If the selected trading pair has staked liquidity, click "Manage"

      - Shows "Deposit" and "Withdraw" buttons along with staking data, including staked amount and reward data for the trading pair.

    - If the selected trading pair has staked liquidity, click "Manage" and then "Deposit"

      - Allows you to stake more LP Tokens.

    - If the selected trading pair has staked liquidity, click "Manage" and then "Withdraw"

      - Allows you to redeem LP Tokens and staking rewards.

    - If staking exceeds one week

      - You can "Claim" staking rewards.

  - Negative Test Scenarios

    - If the selected trading pair has no staked liquidity, click "Deposit"

      - Shows the "Add Liquidity" button and related staking data for the trading pair, but does not show staked amount and reward data.

    - Enter an LP Token amount less than the balance when staking

      - Staking is not allowed.

    - If staking is less than one week

      - Unable to "Claim" staking rewards.

- Liquidity Mining

  - Setup

    - Positive Test Scenarios
      - Input slippage tolerance greater than or equal to zero
        - Complete the transaction within the set slippage tolerance, otherwise, the transaction will be canceled.
      - Input slippage tolerance greater than 1
        - A prompt appears indicating the transaction will prioritize completion.
      - Slippage tolerance set to Auto
        - The system automatically sets the optimal slippage percentage and completes the transaction.
      - No slippage tolerance value entered
        - The system defaults to Auto.
      - Input transaction deadline greater than 1
        - Complete the transaction within the specified minutes, otherwise, the transaction will be canceled.
      - No transaction deadline value entered
        - The system defaults to 30 minutes.
      - Toggle Expert Mode set to True
        - A two-step confirmation appears. After confirmation, the screen is skipped, and higher slippage is allowed.
      - Disable Multihops set to True
        - Direct token-to-token swaps are allowed.

    - Negative Test Scenarios
      - Input slippage tolerance less than zero
        - Invalid setting prompt appears.
      - Input slippage tolerance equal to 0
        - A warning appears indicating potential transaction failure.
      - Input slippage tolerance greater than 50
        - Invalid setting prompt appears.
      - Input transaction deadline less than 1
        - Invalid setting prompt appears.
      - Input transaction deadline greater than 180
        - Invalid setting prompt appears.

    - Boundary Test Scenarios
      - Input slippage tolerance with more than two decimal places
        - The system automatically discards the values after two decimal places.

  - Source Token A

    - Positive Test Scenarios
      - Input token amount less than the balance
        - The transaction can proceed.
      - Select Max for token amount
        - The transaction amount is set to the maximum held amount.
      - Click the token
        - Displays the search box, suggested tokens for exchange, and a token list.
      - Enter the correct token keyword in the search box
        - The corresponding token is displayed.
      - Enter the correct token contract address in the search box
        - The corresponding token is displayed.
      - Click any suggested token for exchange
        - Successfully changes the token pair.
      - Click Manage Token List
        - Displays the toggle for switching tokens, list search box, and token search box.
      - Select a list in Manage Token List
        - Displays the list search box and token list.
      - Enter the correct URL in the List search box
        - The corresponding list is displayed.
      - Enter the correct ENS name in the List search box
        - The corresponding list is displayed.
      - Set any list to On in Manage Token List
        - All tokens from that list are displayed.
      - Set any list to Off in Manage Token List
        - Tokens from that list are hidden.
      - Delete any list in Manage Token List
        - Tokens from that list cannot be selected.
      - Click View List in Manage Token List
        - Redirects to the list page on [https://tokenlists.org](https://tokenlists.org).
      - Select Tokens in Manage Token List
        - Displays a search box for contract addresses and corresponding tokens.
      - Enter the correct contract address in the search box
        - The corresponding token is displayed along with an import button.
      - Import a token after entering the correct contract address
        - The token is added to the list.
      - Enter the contract address of an already imported token
        - The token’s status and information are displayed.
      - Delete any imported token
        - The token cannot be selected from the list.
      - Click Clear All in Tokens
        - All imported tokens are removed from the list.

    - Negative Test Scenarios
      - Input token amount greater than the balance
        - Insufficient balance warning appears.
      - Select a token not owned by the wallet
        - Insufficient balance warning appears.
      - Enter an incorrect token keyword in the search box
        - No token found warning appears.
      - Enter an incorrect token contract address in the search box
        - No token found warning appears.
      - Enter an incorrect URL in the List search box
        - No list found warning appears.
      - Enter an incorrect ENS name in the List search box
        - No list found warning appears.
      - Enter an incorrect contract address in the search box
        - No token found warning appears.

    - Boundary Test Scenarios
      - Input token amounts with maximum precision.

  - Source Token B

    - Positive Test Scenarios
      - Input token amount less than the balance
        - The transaction can proceed.
      - Select Max for token amount
        - The transaction amount is set to the maximum held amount.
      - Click the token
        - Displays the search box, suggested tokens for exchange, and a token list.
      - Enter the correct token keyword in the search box
        - The corresponding token is displayed.
      - Enter the correct token contract address in the search box
        - The corresponding token is displayed.
      - Click any suggested token for exchange
        - Successfully changes the token pair.
      - Click Manage Token List
        - Displays the toggle for switching tokens, list search box, and token search box.
      - Select a list in Manage Token List
        - Displays the list search box and token list.
      - Enter the correct URL in the List search box
        - The corresponding list is displayed.
      - Enter the correct ENS name in the List search box
        - The corresponding list is displayed.
      - Set any list to On in Manage Token List
        - All tokens from that list are displayed.
      - Set any list to Off in Manage Token List
        - Tokens from that list are hidden.
      - Delete any list in Manage Token List
        - Tokens from that list cannot be selected.
      - Click View List in Manage Token List
        - Redirects to the list page on [https://tokenlists.org](https://tokenlists.org).
      - Select Tokens in Manage Token List
        - Displays a search box for contract addresses and corresponding tokens.
      - Enter the correct contract address in the search box
        - The corresponding token is displayed along with an import button.
      - Import a token after entering the correct contract address
        - The token is added to the list.
      - Enter the contract address of an already imported token
        - The token’s status and information are displayed.
      - Delete any imported token
        - The token cannot be selected from the list.
      - Click Clear All in Tokens
        - All imported tokens are removed from the list.

    - Negative Test Scenarios
      - Input token amount greater than the balance
        - Insufficient balance warning appears.
      - Select a token not owned by the wallet
        - Insufficient balance warning appears.
      - Enter an incorrect token keyword in the search box
        - No token found warning appears.
      - Enter an incorrect token contract address in the search box
        - No token found warning appears.
      - Enter an incorrect URL in the List search box
        - No list found warning appears.
      - Enter an incorrect ENS name in the List search box
        - No list found warning appears.
      - Enter an incorrect contract address in the search box
        - No token found warning appears.

    - Boundary Test Scenarios
      - Input token amounts with maximum precision.

  - Add Liquidity

    - Positive Test Scenarios
      - Access the "Add Liquidity" page
        - The following elements are displayed:
          1. A non-set Source Token B
          2. Source Token A set to FX
          3. Input fields for adding liquidity.
      - Input token amounts within the balance for both A and B, but do not approve either
        - "Approve A" and "Approve B" buttons are shown.
      - Input token amounts within the balance for both A and B, but do not approve A
        - "Approve A" button is shown.
      - Input token amounts within the balance for both A and B, but do not approve B
        - "Approve B" button is shown.
      - Input token amounts within the balance for both A and B, and approve both
        - You can directly click "Supply" and view the Initial prices and pool share values.
      - Input token amounts within the balance for both A and B, approve both, and click Supply
        - Liquidity is successfully added, and assets are updated. The screen displays:
          1. "View on FX StarScan" button
          2. "Close" button.
      - After adding liquidity, click "View on FX StarScan"
        - Redirects to FX StarScan and displays the transaction details.
      - After successfully adding liquidity
        - You can view the position details of the liquidity pair.

    - Negative Test Scenarios
      - No token selected for B
        - An "Invalid pair" prompt appears.
      - A and B tokens are selected but no amounts are entered
        - A prompt to input an amount appears.
      - Token A is selected but no amount is entered
        - A prompt to input an amount appears.
      - Token B is selected but no amount is entered
        - A prompt to input an amount appears.

    - Boundary Test Scenarios
      - Input token values at maximum precision.

### Dashboard

- Redirect to [https://trade.marginx.io/home](https://trade.marginx.io/home)

### Bridge

- Source Token

  - Positive Test Scenarios

    - Click on the chain dropdown menu

      - Displays the list of supported chains.

    - Select any chain from the dropdown list

      - Switches to the selected chain.

    - Click on the token

      - Displays the list of supported tokens for the selected chain along with their corresponding balances.

    - Click on any token in the list

      - Successfully changes the source token and displays its balance.

    - Enter a token amount less than the available balance

      - The transaction can proceed.

    - Select "Max" for the token amount

      - The transaction amount will be set to the maximum available balance.

  - Negative Test Scenarios

    - If no chain is selected

      - A required field alert pops up.

    - If the selected chain is not the one currently connected to the wallet

      - A "Switch to correct chain" alert pops up.

    - If a chain is selected but no token is chosen

      - A required field alert pops up.

    - If no value is entered for the token amount

      - A required value alert pops up.

    - If the token amount entered is greater than the available balance

      - An insufficient balance warning is displayed.

    - If a token not owned by the wallet is selected

      - An insufficient balance warning is displayed.

  - Boundary Test Scenarios

    - Enter the token amount with maximum precision

      - Values exceeding the token precision will be rounded.

    - Select "Max" for the token amount, and if the token is the gas token for that chain

      - The transaction amount will equal the available balance minus the minimum required gas fee.

- Destination Token

  - Positive Test Scenarios

    - Click on the chain dropdown menu

      - Displays the list of supported chains.

    - Select any chain from the dropdown list

      - Switches to the selected chain.

    - Click on the token

      - Displays the list of supported tokens for the selected chain along with their corresponding balances.

    - Click on any token in the list

      - Successfully changes the destination token and displays its balance.

  - Negative Test Scenarios

    - If no chain is selected

      - A required field alert pops up.

    - If a chain is selected but no token is chosen

      - A required field alert pops up.

    - If the source token is not yet supported on the destination token list

      - Bridge cannot proceed, and selecting a non-source token shows a "Coming soon" alert.

- Bridge Functionality

  - Positive Test Scenarios

    - Enter any amount within the source token's available balance

      - The destination token automatically updates with the same value and becomes uneditable.

    - Click the "V" (swap button)

      - The source token and destination token chains are swapped.

    - If the source token is A-chain USDT and the destination token is B-chain USDT, then change the source token's chain to B-chain

      - The destination token automatically changes to A-chain, effectively swapping chains.

    - If the source token is A-chain USDT and the destination token is B-chain USDT and proceed with Bridge, but the A-chain USDT has not yet been approved for contract

      - Redirects to the wallet's protocol approval page.

    - If the source token is A-chain USDT and the destination token is B-chain USDT and proceed with Bridge

      - The "Confirm Bridge" window pops up, displaying transaction details and a "Bridge" button. If bridging from Zeta to another chain, it also shows the required gas fee token and amount.

    - If the source token is A-chain USDT and the destination token is B-chain USDT and the Bridge is successful

      - 1. A-chain gas token is deducted.
        2. The A-chain USDT balance is reduced by the transaction amount.
        3. The B-chain USDT balance increases by the transaction amount.
        4. The interface shows: 1. "View on A-chain Explorer" 2. "View on B-chain Explorer" 3. "Add token to wallet" button 4. Close window button.
        5. Transaction history shows the record along with the chain's transaction hash.

    - If the source token is A-chain USDT and the destination token is B-chain USDT and the Bridge is successful, click "View on A-chain Explorer"

      - Redirects to the A-chain explorer and displays transaction details.

    - If the source token is A-chain USDT and the destination token is B-chain USDT and the Bridge is successful, click "View on B-chain Explorer"

      - Redirects to the B-chain explorer and displays transaction details.

    - If the source token is A-chain USDT and the destination token is B-chain USDT and the Bridge is successful, click "Add to Wallet"

      - The destination token is added to the bound wallet.

  - Negative Test Scenarios

    - If the source and destination tokens are different

      - The Bridge cannot proceed, and selecting a non-source token shows a "Coming soon" alert.

    - If the transaction is rejected by the wallet during Bridge

      - Displays transaction failure alert, and assets remain unchanged.

    - If the source chain's gas token balance is insufficient to pay the gas fee during Bridge

      - Displays transaction failure alert, and assets remain unchanged.

    - If the source token is A-chain USDT and the destination token is B-chain USDT and proceed with Bridge, but the A-chain USDT contract approval is rejected

      - Displays transaction failure alert, and assets remain unchanged.

    - If miners are still confirming the block during Bridge

      - The transaction is marked as "Pending," and the transaction history shows the record along with the chain's transaction hash.

    - When bridging from Zeta chain to an external chain, if the transaction amount plus the gas fee exceeds the balance

      - Transaction fails, and an insufficient balance warning is displayed.

  - Equivalence Partitioning Scenarios

    - Test different chains and tokens for equivalence partitioning

      - 1. Chain: 1. External chain → Zeta chain 2. Zeta chain → External chain
        2. Token: 1. Native 2. ERC20


### Setting

- Connect Wallet

- Disconnect Wallet

- Copy Wallet Address

- Switch Network

- Check Transaction History

- Clear Transaction History

- View on Blockchain Explorer

## Acceptance Criteria

### UI Verification

### Functional Verification

### API Verification

### On-Chain Data Verification

### Compatibility Verification

### Performance Verification