# MarginX

## Test OS#

## APP (iOS) 

- Main Test OS#

## APP (Android) 

- Test OS

### Web(H5) 

- Test OS

### Web(Desktop) 

- Main Test OS#

## API 

- Main Test OS

## Test Data

### Test Chain

 - f(x)core

 - ZetaChain

### Test Currency

 - FX

- Zeta

- USDC

- USDT

## Test Scenario

### Swap

- Setup

 - Forward Test Scenario

 - Slippage tolerance: Enter a number greater than or equal to zero

          - Complete the transaction within the set error value, otherwise the transaction will be cancelled

 - Slippage tolerance: Enter a number greater than 1

 - Jumping out of the transaction will be prompted to complete first

. - Slippage toleranceSelect Auto

 - The system automatically sets the optimal slippage error % and trades

 - No value is entered for Slippage tolerance - Auto is 

 automatically selected by the system -

 Transaction deadline Enter a number greater than 1

 - Complete the transaction within the set number of minutes, otherwise the transaction will be cancelled

 - No value is entered for Transaction deadline

 - The system automatically brings in 30 minutes

 - Toggle Expert Mode is set to True

 - A two-step confirmation will be displayed, and the confirmation screen will be skipped after confirmation, and a high slippage error will be

 generated  . - Disable Multihops set to True

 - Direct exchange of trading pairs

 - Negative Test Scenario

 - Enter a number that is not greater than or equal to zero in Slippage tolerance

 - Invalid setting prompt

 - Enter a number equal to 0 in Slippage tolerance

 - Alert that the transaction may fail

       - Slippage tolerance: Enter a number greater than 50

 - Invalid setting prompt

 - Transaction deadline: Enter a number other than 1

 - Invalid setting prompt

 - Enter a number greater than 180 for transaction deadline

          - Invalid setting prompt

 - Boundary Test Scenario

 - Slippage tolerance: Enter a number greater than two decimal places

. - Automatically discard values that exceed two decimal places

- Source currency

 - Forward Test Scenario

 - The number of coins entered is less than the number held

 - Tradable

 - Currency Quantity Select Max

 - The number of transactions is brought into the maximum holding value

 - Click on the currency

 - Display the search Kuang, suggested exchange currency, currency list

 - Search Kuang enter the correct key word for the currency

          - Show mapped currency

 - Search Kuang and enter the correct currency contract address

 - Display the corresponding currency

 - Click on any of the proposed exchange currencies

 - Successfully change trading pair

 - Click on the Manage Currencies list

          - Show List & Currency Toggle, List Search, Currency Search

 - Click on the Manage Currency List and select List

 - Show List Search & List 

 - Click on the Manage Currency List and select List, enter the correct URL

 - Display the corresponding List

       - Click on the list of managed currencies and select List, enter the correct ENS name

 - Show the corresponding List

 - Click on the list of managed currencies and select List, set any List to On

 - Show all tokens of the list

 - Click on the list of managed currencies and select List to set any list to Off

          - Do not show all tokens in the list

 - Click on the list of managed currencies and select List to delete any of the lists

 - The list of currencies cannot be selected for all the currencies of the list

 - Click on the list of managed currencies and select List to add any list and click View List

          - Go to the https://tokenlists.org/ page of the list

 - Click on the list of managed currencies and select Tokens

 - Display the contract address search and the corresponding currency

 - Click on the list of managed currencies and select Tokens to enter the correct contract address

 - Display the corresponding currency and the import button

 - Click on the list of managed currencies and select Tokens, enter the correct contract address and import

 - Add the currency to the list of currencies

 - Click on the list of managed currencies and select Tokens, enter the address of the imported currency

 - See the currency status and currency message

       - Click on the list of managed currencies and select Tokens, select any imported currency to delete

 - The currency cannot be selected in the currency list

 - Click on the list of managed currencies and select Tokens, click clear all

 - The list of currencies cannot be selected for all imported currencies

 - Negative test scenario

       - The amount of currency input is greater than the holding amount

 - Insufficient Balance Alert

 - Currency: Select a currency that is not owned by the wallet

 - Insufficient Balance Alert

 - Search Kuang entered the wrong currency keyword

. - Check no currency alert

       - Search for Mistyped Currency Futures Address

 - Check No Currency Alert

 - Click on the Manage Currency List and select List to enter the wrong URL

 - Check No List Alert

 - Click on the Manage Currency List and select List to enter the wrong ENS name

          - No List Alert

 - Click on the list of managed currencies and select Tokens to enter the wrong contract address

. - Check no currency alert

 - Boundary test scenario

 - Maximum precision scenario for entering the number of currencies

 - Swap currency

 - Forward test scenario

 - The number of coins entered is less than the holding amount

 - Tradable

 - Select Max for Currency Quantity

 - The number of transactions is brought into the maximum holding value

 - Click on the currency

 - Display the search Kuang, suggested exchange currency, and currency list

       - Search Kuang, enter the correct currency keyword

, - Show the corresponding currency, 

 - Search Kuang, enter the correct currency contract address

, - Display the corresponding currency

, - Click on any of the suggested exchange currencies

 - Successfully change the trading pair

       - Click on the Manage Currency List

 - Show List and Currency Toggle, List Search, Currency Search - 

 Click on the Manage Currency List and select List

 - Show List Search and List

 - Click on the Manage Currency List and select List, enter the correct URL

          - Show the corresponding List

 - Click on the list of managed currencies and select List to enter the correct ENS name

 - Show the corresponding List

 - Click on the list of managed currencies and select List to set any List to On

 - Displays all tokens of the list

       - Click on the list of managed currencies and select List to set any list to Off

 - Do not show all tokens of the list

 - Click on the list of managed currencies and select List to delete any list

 - The currency list cannot select all the currencies of the list

       - Click on the Manage Currency List and select ListAdd any of the Lists and click View List

 - Go to the https://tokenlists.org/ page of the list

 - Click on the Manage Currencies list and select Tokens

 - Display the contract address, search for the corresponding currency

       - Click on the list of managed currencies and select Tokens to enter the correct contract address

;  - Display the corresponding currency and import button

 - Click on the list of managed currencies and select Tokens, enter the correct contract address and import

 - add the currency to the currency list

       - Click on the list of managed currencies and select Tokens, enter the address of the imported currency

 - See the currency status and currency message

 - Click on the list of managed currencies and select Tokens, select any of the imported currencies to delete

 - The currency cannot be selected in the currency list

       - Click on the list of managed currencies and select Tokens, click clear all

 - You cannot select all the imported currencies in the currency list

. - Negative Test Scenario

 - The number of coins entered is greater than the number of holdings

 - Insufficient Balance Warning

 - The search for the keyword of the currency is incorrectly entered

 - Check No Currency Alert

 - Search Kuang Entered the Wrong Currency Futures Address

 - Check No Currency Alert

 - Click Manage Currency List and select List to enter the wrong URL

 - Check No List Alert

       - Click on the list of managed currencies and select List, and enter an error in ENS name

 - No List alert

 - Click on the list of managed currencies and select Tokens to enter the wrong contract address

. - Check no currency alert

 - Boundary Test Scenario

 - Enter the maximum precision scenario for the number of currencies

- Swap function

 - Forward Test Scenario

 - Enter the value within any asset in the source currency

 - The exchange currency is automatically converted to the exchangeable quantity and the exchange rate is displayed

.  - Enter the value within any asset in the source currency but do not select the exchange currency

.  - Reminder that you need to select the currency to be exchanged

 - Click "V" (Convert button)

 - Exchange of source currency and exchange currency

 - Source currency: FX and swap - 

 Get the selected amount of exchange currency

 - Source currency: Select non-FX and make an initial swap

 - Redirect to the wallet agreement consent page

 - Select non-FX as the source currency and perform a non-initial swap

 - Get the selected amount of exchange currency

 - After the swap is successful

 - The asset is successfully changed, and the screen will display 1. View on FX StarScan. 

2. Add Currency to Wallet button 3. Close window button - After the swap is successful, click View on FX StarScan

 - Go to StarScan and display the transaction details

 - After the swap is successful, click Add to Wallet

 - Convert currency to the bound wallet

 - Negative test scenario

       - No liquidity of the source currency and the exchange currency

 - No liquidity alert for the trading pair

 - After the swap fails

 - No change in assets

### Pool

- Create a pair & Add Liquidity

 - Settings

       - Forward Test Scenario

 - Slippage toleranceEnter a number greater than or equal to zero

 - Complete the transaction within the set transaction error value, otherwise the transaction will be cancelled

 - Slippage toleranceEnter a number greater than 1

 - Jump out of the transaction will be prompted to complete first

          - Slippage toleranceSelect Auto

 - The system automatically sets the optimal slippage error % and trades -

 Slippage tolerance is not entered

 - the system automatically selects Auto

          - Transaction deadline: Enter a number greater than 1

 - The transaction is completed within the set number of minutes, otherwise the transaction will be cancelled

 - Transaction deadline does not enter a value

 - The system automatically brings in 30 minutes

          - Toggle Expert Mode set to True

 - A two-step confirmation will be displayed, and the confirmation screen will be skipped after confirmation, and a high slippage error will be

 generated  . - Disable Multihops set to True

 - Direct exchange of trading pairs

 - Negative test scenario

          - Slippage tolerance: Enter a number that is not greater than or equal to zero

. - Invalid setting prompt

 - Slippage tolerance: Enter a number equal to 0

 - Alert that the transaction may fail

 - Slippage tolerance: Enter a number greater than 50

 - Invalid setting prompt

 - Enter a number greater than 1 in transaction deadline

 - Invalid setting prompt

 - Enter a number greater than 180 in transaction deadline

 - Invalid setting prompt

 - Boundary Test Scenarios

 - Slippage toleranceEnter a number greater than two decimal places

 - Automatically discard values that exceed two decimal places

 - Currency A in circulation

 - Forward Test Scenario

 - The number of coins entered is less than the number of holdings

             - Tradable

 - Currency Quantity Select Max

 - The number of transactions is brought into the maximum holding value

 - Click on the currency

 - Display the search Kuang, suggested exchange currency, currency list

 - Search Kuang enter the correct key word for the currency

             - Show mapped currency

 - Search Kuang and enter the correct currency contract address

 - Display the corresponding currency

 - Click on any of the proposed exchange currencies

 - Successfully change trading pair

 - Click on the Manage Currencies list

             - Show List & Currency Toggle, List Search, Currency Search

 - Click on the Manage Currency List and select List

 - Show List Search & List 

 - Click on the Manage Currency List and select List, enter the correct URL

 - Display the corresponding List

 - Click on the list of managed currencies and select List, enter the correct ENS name

 - Show the corresponding List

 - Click on the list of managed currencies and select List, set any list to On

 - Displays all tokens of the list

          - Click on the list of managed currencies and select List to set any list to Off

 - Do not show all tokens of the list

 - Click on the list of managed currencies and select List to delete any list

 - The currency list cannot select all the currencies of the list

          - Click on the list of managed currencies and select ListAdd any list and click View List

 - Go to the https://tokenlists.org/ page of the list

 - Click on the list of managed currencies and select Tokens

 - Show the contract address, search for the corresponding currency

          - Click on the list of managed currencies and select Tokens to enter the correct contract address

;  - Display the corresponding currency and import button

 - Click on the list of managed currencies and select Tokens, enter the correct contract address and import

 - add the currency to the currency list

          - Click on the list of managed currencies and select Tokens, enter the address of the imported currency

 - See the currency status and currency message

 - Click on the list of managed currencies and select Tokens, select any of the imported currencies to delete

 - The currency cannot be selected in the currency list

          - Click on the list of managed currencies and select Tokens, click clear all

 - You cannot select all the imported currencies in the currency list

. - Negative test scenario

 - The number of coins entered is greater than the number of holdings

 - Insufficient balance warning

          - Currency: Select a currency that the wallet does not own

.  - Insufficient Balance Alert

 - Search Kuang entered the wrong currency keyword

. - Check no currency alert

 - Search Kuang entered the wrong currency contract address

 - Check no currency alert

          - Click on the list of managed currencies and select List to enter the wrong URL

 - No List Alert

 - Click on the list of managed currencies and select List to enter the wrong ENS name

 - No List Alert

 - Click on the list of managed currencies and select Tokens to enter the wrong contract address

 - No Currency Alert

 - Boundary Test Scenario

 - Maximum Accuracy Scenario for Currency Quantity Input

 - Currency B in circulation

 - Forward Test Scenario

 - The input currency quantity is less than the holding amount

             - Tradable

 - Currency Quantity Select Max

 - The number of transactions is brought into the maximum holding value

 - Click on the currency

 - Display the search Kuang, suggested exchange currency, currency list

 - Search Kuang enter the correct key word for the currency

 - Show mapped currency

 - Search for Kuang and enter the correct currency contract address

 - Display the corresponding currency

 - Click on any of the proposed exchange currencies

 - Successfully change the trading pair

          - Click on the Manage Currency List

 - Show List and Currency Toggle, List Search, Currency Search - 

 Click on the Manage Currency List and select List

 - Show List Search and List

 - Click on the Manage Currency List and select List, enter the correct URL

 - Show Corresponding List

 - Click on the list of managed currencies and select List, enter the correct ENS name

 - Show the corresponding list

 - Click on the list of managed currencies and select List to set any list to On

             - Show all tokens in the list

 - Click on the list of managed currencies and select List to set any list to Off

 - Do not show all tokens in the list

 - Click on the list of managed currencies and select List to delete any of the 

lists             - Currency list: You can't select all the currencies of the list

 - Click on the Manage Currencies list and select ListAdd any of the Lists and click View List

 - Go to the https://tokenlists.org/ page of the list

 - Click on the Manage Currencies list and select Tokens

             - Display the contract address search and the corresponding currency

 - Click on the list of managed currencies and select Tokens to enter the correct contract address

 - Display the corresponding currency and import button

 - Click on the list of managed currencies and select Tokens, enter the correct contract address and import

             - Add this currency to the list of currencies

 - Click on the list of managed currencies and select Tokens, and enter the address of the imported currency

 - See the currency status and currency information

 - Click on the list of managed currencies and select Tokens, and select any of the imported currencies to delete

             - The currency cannot be selected in the currency list

 - Click on the Manage Currency List and select Tokens, click clear all

 - The currency list cannot select all the imported currencies

 - Negative Test Scenario

 - The input number of coins is greater than the holding amount

             - Insufficient Balance Alert

 - Currency: Select a currency that is not owned by the wallet

 - Insufficient Balance Alert

 - Search Kuang entered the wrong currency keyword

. - Check no currency alert

 - Search Kuang entered the wrong currency off contract address

 - Check No Currency Alert

 - Click on the list of managed currencies and select List to enter the wrong URL

 - Check no List alert

 - Click on the list of managed currencies and select List to enter the wrong ENS name

 - Check no List alert

 - Click on the list of managed currencies and select Tokens to enter the wrong contract address

. - No Currency Alert

 - Boundary Test Scenario

 - Maximum Accuracy Scenario for Currency Quantity

 Input - Create a pair - Forward

 test scenario

 - Go to Create a pair

 - See the circulating A, B currency and setting button without setting

 - A and B currencies are both entered within the asset limit, but A and B currencies are not Approved

 - Apps button is required to display A and B currencies

          - Currency A and B are both entered within the asset limit, but currency A is not approved

 - Approve is required for currency A - Currency A and 

 currency B are both entered within the asset limit, but currency B is not approved

 - Approve button is required to display currency B

          - A and B currencies are both entered into the value within the asset limit, and both A and B currencies have been approved

 - You can directly Supply and see the Initial prices and pool share values

 - A and B currencies are both input within the asset limit, and A and B currencies have been Applied and Supply

             - Liquidity is successfully added and the asset is successfully changed, and the screen displays1. View on FX StarScan. 2. Close the window button

 - After the increase in liquidity is successful, click View on FX StarScan

 - jump to StarScan and display the details of the transaction

 - After the new liquidity is successfully added

 - you can see the Position details of the liquidity of this trading pair

       - Negative test scenario

 - Currency A and currency B are not selected

. - Invalid pair is displayed. 

 - Currency A is not selected

. - Invalid pair is displayed. 

 - Currency B is not selected

 - Invalid pair prompt pops up

 - Currency A and currency B are selected but no value is entered

 - Input value prompt is displayed

 - Currency A and currency B are selected but A does not enter a value

 - A value prompt is displayed

          - Currency A and currency B are both selected, but no value is entered in B

.  - A numerical value prompt pops up

.  - Boundary Test Scenario

 - Maximum Accuracy Scenario for Currency A and B

 - Add Liquidity

 - Forward testing scenario

          - Go to Add Liquidity

 - see the following components: 1.Currency B in circulation without setting2.Currency A with FX set to 3.Set button

:  - Currency A and B are both entered within the asset limit, but Neither A nor B is Approve

 - Approve is required for A and B currencies

          - Currency A and B are both entered within the asset limit, but currency A is not approved

 - Approve is required for currency A - Currency A and 

 currency B are both entered within the asset limit, but currency B is not approved

 - Approve button is required to display currency B

          - A and B currencies are both entered into the value within the asset limit, and both A and B currencies have been approved

 - You can directly Supply and see the Initial prices and pool share values

 - A and B currencies are both input within the asset limit, and A and B currencies have been Applied and Supply

             - Liquidity is successfully added and the asset is successfully changed, and the screen displays1. View on FX StarScan. 

2. Close the window button 3. Get LP Tokens - After successfully increasing the liquidity of this transaction, click View on FX StarScan

 - jump to StarScan and display the details of the transaction

 - After the new liquidity is successfully added

 - you can see the Position details of the liquidity of this trading pair

       - Negative test scenario

 - Currency B is not selected

 - Invalid pair prompt is displayed. 

 - Currency A and currency B are selected but no value is entered

.  - Input value prompt

 is displayed - Currency A and currency B are selected but A does not enter a value

             - Pop up the input value prompt

 - Currency A and currency B are both selected, but B does not enter a value

 - Pop up the input value prompt

 - Boundary test scenario

 - Maximum precision scenario of A and B currencies

 - Import Pool

 - Forward test scenario

 - Currencies A and B have established liquidity but have not yet been imported

 - Automatically import to the Your liquidity page

 - Currencies A and B have established liquidity and have been imported

 - You can see the details of the liquidity position of this trading pair, click Manage this pool

 - Negative test scenario

 - Currency A and currency B have no liquidity

 - You don't have liquidity in this pool yet.

 - Currency A has no liquidity, currency B has liquidity

          - No pool found.Alert, click Create pool. to enter the new liquidity page

 - Currency B has no liquidity, Currency A has

 liquidity  - No pool found. Alert, click Create pool. to enter the new liquidity page

 - Currency B is not selected

          - Prompt to select currency B

 - Your liquidity

 - Forward test scenario

 - Pool with new currency liquidity

 - Pool with liquidity - Pool with liquidity -

 Select any pool and click Manage

          - You can see the details of the pool content and the Add & Remove button

 - Select any pool and click Manage, then click Add

 - Go to the Add Liquidity page and automatically bring in the currency

 - Select any Pool and click Manage, then click Remove

 - Go to the Remove Liquidity page and automatically bring in the currency

 - Go to the Delete Liquidity page, if the trading pair has not obtained a liquidity license

,  - Remove -

 Go to the Delete Liquidity page, if the trading pair has obtained a liquidity license

, - 

 Remove - Go to the Delete Liquidity page, select the quantity greater than 0 to Max, and remove

 - Delete the liquidity of the corresponding A and B currencies

 - Negative test scenario

 - Pool with no new currency liquidity

 - No currency liquidity prompt - Enter the 

 delete liquidity page without entering the deletion quantity

 - Enter the  quantity prompt

    - Equivalence Partition Scenario

 - Go to the Delete Liquidity page and click Detailed to convert A and B currencies

 - Go to the Delete Liquidity page and click Detailed to convert the number of A and B currencies

### Farm

- Farm List

 - Forward Test Scenario

 - Go to the Farm page

 - You can see the function description, query function, stakeable liquidity list and related data

 - Select Sort by Total Deposited for the query function

 - Sort by Total Deposited

 - Select Sort by Total Deposited for the query function

 - Sort by APR% - Search 

 for the currency keyword - 

 Fuzzy search contains this key trading pair

 - Negative test scenario

 - Search for search function Kuang input no keywords

 - Show no item alert

    - Equivalence division scenario

 - Query function: Sort and keywords are different, search conditions, and search conditions

 - Farm

 - Forward test scenario

 - If the selected trading pair has new liquidity but is not pledged, click Deposit

 - You can see the staking token button and the staking data related to the trading pair, but the staking amount and reward data cannot be displayed

       - If there is new liquidity in the selected trading pair, but not pledged, click Deposit and stake LP Tokens

 - You can see 1.Staking amount, 2.Relevant staking data, 3.Max button, 4.Export button, 5.Deposit button

;  - When making a pledge, enter less than the balance of LP Tokens

 - can be staked

       - Click the Max button when staking

 - Automatically bring in the maximum amount that can be staked

 - When making a pledge, enter less than the balance of LP Tokens and click Approve

 - Click Deposit

 - After the staking is completed

          - You can no longer make changes to the liquidity of this trading pair to redeem LP Tokens

. - If the liquidity of the selected trading pair is pledged, click Manage

 - You can see the Deposit and Withdraw buttons and the staking data related to the trading pair, including the pledge amount and reward data

.  - If the liquidity of the selected trading pair has stake, click Manage and click Deposit

          - You can continue to stake more LP Tokens

 - If the selected trading pair has staking liquidity, click Manage and click Withdraw

 - Redeemable LP Tokens and Staking Rewards

 - If staking for more than one week

 - Claim Staking Rewards

 - Negative test scenario

 - If there is no collateral liquidity for the selected trading pair, click Deposit

 - you can see the new liquidity button and the staking data related to the trading pair, but the staking amount and reward data cannot be displayed.

 - When making a pledge, enter less than the balance of LP Tokens

 - Non-staking

 - If the staking is less than one week

          - Unable to Claim Staking Rewards

 - Liquidity Mining

 - Settings 

 - Forward Test Scenario

 - Slippage tolerance input is greater than or equal to zero

 - Complete the transaction within the set transaction error value, otherwise the transaction will be cancelled

 - Slippage tolerance: Enter a number greater than 1

 - Jumping out of the trade will be prioritized to complete the prompt

 - Slippage toleranceSelect Auto

 - The system automatically sets the optimal slippage error % and

 trades          - No value is entered for Slippage tolerance

 - Auto is  automatically selected as Auto

 - Transaction deadline Enter a number greater than 1

 - Complete the transaction within the set number of minutes, otherwise the transaction will be cancelled

          - No value is entered for Transaction deadline

 - 30 minutes are automatically brought in

 by the system  - Toggle Expert Mode is set to True

 - A two-step confirmation will be displayed, and the confirmation screen will be skipped after confirmation, and a high slippage error will be generated

          - Disable Multihops set to True

 - Direct exchange of trading pairs

 - Negative test scenario

 - Slippage tolerance: Enter a non-greater than or equal to zero number

 - Invalid setting prompt

          - Slippage toleranceEnter a number equal to 0

 - Alert that the transaction may fail

 - Slippage toleranceEnter a number greater than 50

 - Invalid setting prompt

          - Enter a number greater than 1 in Transaction deadline

 - Invalid setting prompt

 - Enter a number greater than 180 in Transaction deadline

 - Invalid setting prompt

 - Boundary test scenarios

          - Slippage tolerance: Enter a number greater than two decimal places

 - Automatically discard values that exceed two decimal places

 - Currency in circulation

 - Forward Test Scenario

 - The number of coins entered is less than the holding amount

 - Trades can be made

 - Select Max for the number of currencies

 - The number of transactions is brought into the maximum holding value

 - Click on the currency

 - Display the search Kuang, suggested exchange currency, currency list

 - Search Kuang and enter the correct keyword

             - Show mapped currency

 - Search Kuang and enter the correct currency contract address

 - Display the corresponding currency

 - Click on any of the proposed exchange currencies

 - Successfully change trading pair

 - Click on the Manage Currencies list

 - Show List & Currency Toggle, List Search, Currency Search

 - Click on the Manage Currency List and select List

 - Show List Search & List

 - Click on Manage Currency List and select List, enter the correct URL

             - Show the corresponding List

 - Click on the list of managed currencies and select List to enter the correct ENS name

 - Show the corresponding List

 - Click on the list of managed currencies and select List to set any List to On

 - Displays all tokens of the list

 - Click on the list of managed currencies and select List to set any list to Off

 - Do not show all tokens of the list

 - Click on the list of managed currencies and select List to delete any list

 - The currency list cannot select all the currencies of the list

          - Click on the Manage Currency List and select ListAdd any List and click View List

 - Go to the https://tokenlists.org/ page of the list

 - Click on the Manage Currency List and select Tokens

 - Show the contract address, search Kuang and the corresponding currency

          - Click on the list of managed currencies and select Tokens to enter the correct contract address

;  - Display the corresponding currency and import button

 - Click on the list of managed currencies and select Tokens, enter the correct contract address and import

 - add the currency to the currency list

          - Click on the list of managed currencies and select Tokens, enter the address of the imported currency

 - See the currency status and currency message

 - Click on the list of managed currencies and select Tokens, select any of the imported currencies to delete

 - The currency cannot be selected in the currency list

          - Click on the list of managed currencies and select Tokens, click clear all

 - You cannot select all the imported currencies in the currency list

. - Negative test scenario

 - The number of coins entered is greater than the number of holdings

 - Insufficient balance warning

          - Currency: Select a currency that the wallet does not own

.  - Insufficient Balance Alert

 - Search Kuang entered the wrong currency keyword

. - Check no currency alert

 - Search Kuang entered the wrong currency contract address

 - Check no currency alert

 - Click on the list of managed currencies and select List to enter the wrong URL

 - Check no list alert

 - Click on the list of managed currencies and select List to enter the wrong ENS name

 - Check no list alert

          - Click on the list of managed currencies and select Tokens to enter the wrong contract address

.  - No Currency Alert

 - Boundary Test Scenario

 - Maximum precision scenario for entering the number of coins

 - Circulating B Currency

 - Forward testing scenario

          - The number of coins entered is less than the holding amount

 - Tradable

 - Select Max for Currency Quantity

 - The number of transactions is brought into the maximum holding value

 - Click on the currency

 - Display the search Kuang, suggested exchange currency, and currency list

 - Search Kuang, enter the correct currency keyword

, - Show the corresponding currency

, - Search Kuang, enter the correct currency, enter the contract address

,  - Show the corresponding currency, 

 - Click on any of the proposed exchange currencies

             - Successfully change trading pair

 - Click on the Manage Currency List

 - Show List and Currency Toggle, List Search, Currency Search

 - Click on the Manage Currency List and select List

 - Show the List Search List and List List

          - Click on the list of managed currencies and select List, enter the correct URL

 - Show the corresponding List

 - Click on the list of managed currencies and select List, enter the correct ENS name

 - Show the corresponding List

 - Click on the list of managed currencies and select List to set any of the Lists to On

 - Show all tokens in the list

 - Click on the list of managed currencies and select List to set any list to Off

 - Do not show all tokens in the list

 - Click on the list of managed currencies and select List to delete any of the 

lists             - The currency list cannot select all the currencies of the list

 - Click on the Manage Currencies list and select List, then add any list and click View List

 - Go to the https://tokenlists.org/ page of the list

 - Click on the Manage Currencies list and select Tokens

             - Display the contract address search and the corresponding currency

 - Click on the list of managed currencies and select Tokens to enter the correct contract address

 - Display the corresponding currency and import button

 - Click on the list of managed currencies and select Tokens, enter the correct contract address and import

             - Add this currency to the list of currencies

 - Click on the list of managed currencies and select Tokens, and enter the address of the imported currency

 - See the currency status and currency information

 - Click on the list of managed currencies and select Tokens, and select any of the imported currencies to delete

 - The currency cannot be selected in the currency list

 - Click on the Manage Currency List and select Tokens, click clear all

 - The currency list cannot select all the imported currencies

 - Negative Test Scenario

 - The input number of coins is greater than the holding amount

             - Insufficient Balance Alert

 - Currency: Select a currency that is not owned by the wallet

 - Insufficient Balance Alert

 - Search Kuang entered the wrong currency keyword

. - Check no currency alert

 - Search Kuang entered the wrong currency off contract address

             - Check No Currency Alert

 - Click on the list of managed currencies and select List to enter the wrong URL

 - Check no List alert

 - Click on the list of managed currencies and select List to enter the wrong ENS name

 - Check no List alert

          - Click on the list of managed currencies and select Tokens to enter the wrong contract address

.  - No Currency Alert

 - Boundary Test Scenario

 - Maximum Accuracy Scenario for Currency Quantity Input

 - Add Liquidity - Forward

 Test Scenario

          - Go to Add Liquidity

 - see the following components: 1.Currency B in circulation without setting2.Currency A with FX set to 3.Set button

:  - Currency A and B are both entered within the asset limit, but Neither A nor B is Approve

 - Approve is required for A and B currencies

          - Currency A and B are both entered within the asset limit, but currency A is not approved

 - Approve is required for currency A - Currency A and 

 currency B are both entered within the asset limit, but currency B is not approved

 - Approve button is required to display currency B

          - A and B currencies are both entered into the value within the asset limit, and both A and B currencies have been approved

 - You can directly Supply and see the Initial prices and pool share values

 - A and B currencies are both input within the asset limit, and A and B currencies have been Applied and Supply

             - Liquidity is successfully added and the asset is successfully changed, and the screen displays1. View on FX StarScan. 2. Close the window button

 - After the increase in liquidity is successful, click View on FX StarScan

 - jump to StarScan and display the details of the transaction

 - After the new liquidity is successfully added

 - you can see the Position details of the liquidity of this trading pair

       - Negative test scenario

 - Currency B is not selected

 - Invalid pair prompt is displayed. 

 - Currency A and currency B are selected but no value is entered

.  - Input value prompt

 is displayed - Currency A and currency B are selected but A does not enter a value

 - Pop up the input value prompt

 - Currency A and currency B are both selected, but B does not enter the value

 - Pop up the input value prompt

 - Boundary Test Scenario

 - Maximum precision scenario of currency A and B

### Dashboard

- Go to https://trade.marginx.io/home page

### Bridge

- Go to https://pundiscan.io/fxbridge page

### Setting

- Link Wallet

- Unlink Wallet

- Copy Wallet Address

- Change Link

- Transaction Log Check

- Clear Transaction Log

- Block Explorer Check

## Acceptance Criteria

### UI Verification

### Functional Verification

### Interface Verification

### Verification of data on the chain

### Compatibility verification

### Verification of performance

