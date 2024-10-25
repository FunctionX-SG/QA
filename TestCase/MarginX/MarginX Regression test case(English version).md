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

	- Positive Test Cases

		- Click on the chain dropdown menu

			- Supported chain options are displayed

		- Select any chain from the dropdown

			- Switches to the selected chain

		- Click on the token

			- Shows the list of supported tokens on the selected chain along with corresponding balances

		- Select any token from the list

			- Successfully changes the source token and displays the balance of that token

		- Enter a token amount less than the available balance

			- Allows the transaction

		- Select Max for token amount

			- Transaction amount is set to the maximum available balance

	- Negative Test Cases

		- If no chain is selected

			- A required field warning is displayed

		- If the selected chain does not match the currently connected wallet chain

			- Displays a "Switch to correct chain" warning

		- If a chain is selected but no token is chosen

			- A required field warning is displayed

		- If no value is entered for token amount

			- A required amount warning is displayed

		- If token amount entered exceeds available balance

			- Displays an insufficient balance warning

		- If a token is selected that is not owned in the wallet

			- Displays an insufficient balance warning

	- Boundary Test Cases

		- Enter token amount with maximum precision

			- Rounds to appropriate precision if it exceeds token’s precision limit

		- Select Max for token amount, and the token is used as gas on the chain

			- Transaction amount will equal balance minus minimum gas fee

- Destination Token

	- Positive Test Cases

		- Click on the chain dropdown menu

			- Supported chain options are displayed

		- Select any chain from the dropdown

			- Switches to the selected chain

		- Click on the token

			- Shows the list of supported tokens on the selected chain along with corresponding balances

		- Select any token from the list

			- Successfully changes the destination token and displays the balance of that token

	- Negative Test Cases

		- If no chain is selected

			- A required field warning is displayed

		- If a chain is selected but no token is chosen

			- A required field warning is displayed

		- If the source token is not supported in the destination token list

			- Bridge cannot proceed, displaying "Insufficient liquidity for this trade" warning

- Bridge Function

	- Positive Test Cases

		- Enter any value within available asset amount for source token

			- Destination token automatically updates with corresponding value and is not editable

		- Click the "V" (switch button)

			- Swaps the source and destination tokens along with respective chains

		- If the source token is USDT on Chain A and destination token is USDT on Chain B, change source chain to Chain B

			- Destination chain automatically updates to Chain A, switching the chains

		- If the source token is USDT on Chain A and destination token is USDT on Chain B, and Bridge is initiated without approving the contract on Chain A

			- Redirects to wallet approval page

		- If the source token is USDT on Chain A and destination token is USDT on Chain B and Bridge is initiated

			- Displays Confirm bridge window, showing transaction details and Bridge button. If bridging from Zeta chain to another chain, displays gas fee token and amount.

		- After successful bridge from USDT on Chain A to USDT on Chain B

			- 1. Deducts gas token on Chain A
            - 2. Deducts bridged amount of USDT on Chain A
            - 3. Adds bridged amount to USDT on Chain B
            - 4. Screen shows 1. View on Chain A Explorer 2. View on Chain B Explorer 3. Add token to wallet button 4. Close button
            - 5. Transaction history shows transaction record with chain's tx hash

		- After successful bridge from USDT on Chain A to USDT on Chain B, click View on Chain A Explorer

			- Redirects to Chain A Explorer displaying transaction details

		- After successful bridge from USDT on Chain A to USDT on Chain B, click View on Chain B Explorer

			- Redirects to Chain B Explorer displaying transaction details

		- After successful bridge from USDT on Chain A to USDT on Chain B, click Add to Wallet

			- Adds the destination token to the connected wallet

	- Negative Test Cases

		- If there is insufficient liquidity for source or destination token

			- Bridge cannot proceed, displaying "Insufficient liquidity for this trade" warning

		- If the wallet rejects the transaction during Bridge

			- Shows transaction failure warning, and assets remain unchanged

		- If gas token is insufficient to cover the gas fee on the source chain

			- Shows transaction failure warning, and assets remain unchanged

		- If the source token on Chain A (e.g., USDT) requires approval but is denied

			- Shows transaction failure warning, and assets remain unchanged

		- If miners are still confirming the block during Bridge

			- Transaction appears as Pending, with transaction history showing transaction record and tx hash

		- If bridging from Zeta chain to an external chain and transaction amount plus gas fee exceeds balance

			- Transaction fails, displaying insufficient balance warning

	- Equivalence Partitioning Test Cases

		- Perform equivalence partitioning tests for different chains and tokens

			- Chain: 1. External chain >> Zeta chain 2. Zeta chain >> External chain
            - Token: 1. Native 2. ERC20

	- Boundary Test Cases

		- Perform cross-chain tests for different tokens and chains, e.g., ETH.USDT <-> ZETA.ZETA

			- Successfully converts token and accurately calculates exchange rate and gas fee

		- Test different tokens with different precision during cross-chain transfers, e.g., Token A supports up to 18 decimals, Token B supports up to 6 decimals

			- If Token A exceeds 6 decimal places, conversion uses the appropriate exchange rate and rounds to the max supported decimals of Token B

### Setting

- Connect Wallet

	- Enables Swap, Bridge, etc., and transaction history and balance are visible

- Disconnect Wallet

	- Disables Swap, Bridge, etc., and transaction history and balance are not visible


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