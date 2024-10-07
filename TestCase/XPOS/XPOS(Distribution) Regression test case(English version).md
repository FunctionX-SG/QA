# XPOS (Distribution)

## Test OS

### Web (Desktop)

- Primary test OS

### API

- Secondary test OS

## Test Data

### Cryptocurrencies

- USDT
- DAI

### Fiat Currencies

- USD
- TWD

### Transaction Cryptocurrencies

- BTC
- ETH

### Cashier Cryptocurrencies

- USDT
- DAI

### Cashier Fiat Currencies

- USD
- TWD

### Blockchains

- ERC20
- BEP20
- TRC20

## Test Scenarios

### Dashboard Page

- Distributor Overview Table Data

  - Displays total number of distributors.
  - The "Type" shows Sum and Total Assets.
  - "Directly Added" shows the total number of directly added distributors and their total assets.
  - "Distributor Added" shows the total number of distributors added by other distributors and their total assets.

- Merchant Overview Table Data

  - Displays total number of merchants.
  - The "Type" shows Sum and Total Assets.
  - "Directly Added" shows the total number of directly added merchants and their total assets.
  - "Sub Distributor Added" shows the total number of merchants added by sub-distributors and their total assets.
  - "Distributor Added" shows the total number of merchants added by distributors and their total assets.

### Distributor Page

- Distributor List

  - Search Module

    - Creator TextBox
    - User NO. TextBox
    - User Name TextBox
    - Owner TextBox
    - Email TextBox
    - "All Roles" DropDownMenu includes Distributor, Sub Distributor, and All Roles status options.
    - "Status" DropDownMenu includes Activated, Inactive, and All Status options.
    - Start Date and Time
    - End Date and Time

  - Distributor List

    - Displays a list of all distributors. Each distributor includes information such as Create On, Creator, User NO., User Name, Owner, Distributor Level, Country, Phone No., Email, Status, and Actions.

  - Add Distributor

    - Distributor Name is a required field.
    - Country/region is a required search dropdown including all countries.
    - Time zone is a dropdown including all time zones.
    - Email is a required field.
    - Confirm Email Address is a required field.
    - First Name is a required field.
    - Middle Name is optional.
    - Last Name is a required field.
    - Phone No. is a required field.
    - Confirm Phone Number is a required field.
    - Address is a required field.
    - Remarks input box.
    - Submit button to add the distributor.
    - Reset button to clear all inputs.

  - Distributor Details

    - Assets Details Table

      - "Type" shows the currency type.
      - Main Account shows the detailed balance of the corresponding currency in the main account.
      - Commission Account shows the detailed balance of the corresponding currency in the commission account.
      - Sub-Total shows the total converted to USD.

    - Distribution Share Data

      - Shows the Master Distributor share percentage.
      - Shows the Sub Distributor share percentage.
      - Shows the Distributor share percentage.

- Balance

  - Search Module

    - Creator TextBox
    - User NO. TextBox
    - User Name TextBox
    - Start Date and Time
    - End Date and Time

  - Balance List

    - Displays all balances. Each balance includes Creator, User NO., User Name, Subtotal (USD), Main Account (USD), Commission Account (USD).

- Distribution

  - My Portion TextBox
  - Sub Distributor Portion TextBox
  - Distributor Portion TextBox
  - Save Button

    - After pressing, it saves the distribution settings and checks if the sum of the three fields equals 100%.

  - Reset to Default Button

    - After pressing, it reverts to default settings: Master Distributor: 20%, Sub Distributor: 30%, Distributor: 50%.

### Merchant Page

- Merchant List

  - Search Module

    - Creator TextBox
    - Brand NO. TextBox
    - Brand Name TextBox
    - Phone No. TextBox
    - Email TextBox
    - Start Date and Time
    - End Date and Time

  - Merchant List

    - Displays all merchants. Each merchant includes Create On, Creator, Brand NO., Brand Name, API Key, Sub-merchant, Owner, Country, Phone No., Email, Status, and Actions.

  - Merchant Details

    - Assets Details Table

      - "Type" shows the currency type.
      - Sales Account shows the corresponding currency's balance in the sales account.
      - Cashier Account shows the corresponding currency's balance in the cashier account.
      - Sub-Total shows the total converted to USD.

    - Merchant Settings Data

      - Shows Withdraw Permission, whether it is enabled or not.
      - Shows Commission Rates, for both Cashier and Sales.
      - Shows Group Label settings.

    - Limitation Table Data

      - "Name" shows the limitation name for the merchant.
      - Crypto Sales Maximum Per Txn shows the maximum amount for a single sales transaction in USDT.
      - Crypto Sales Maximum Per Day shows the maximum amount for sales per day in USDT.
      - Crypto Cashier Maximum Per Txn shows the maximum amount for a single cashier transaction in USDT.
      - Crypto Cashier Maximum Per Day shows the maximum amount for cashier transactions per day in USDT.

  - Add Merchant

    - Type of Business is a required search dropdown including all business categories.
    - Brand Name is a required field.
    - Country/region is a required search dropdown including all countries.
    - Time zone is a dropdown including all time zones.
    - Settlement Crypto is a required search dropdown including all applicable cryptocurrencies.
    - First Name is a required field.
    - Middle Name is optional.
    - Last Name is a required field.
    - Phone No. is a required field.
    - Confirm Phone Number is a required field.
    - Email is a required field.
    - Confirm Email Address is a required field.
    - Submit Button to add the merchant.
    - Reset Button to clear all inputs.
- Finance

  - Query Module

    - Creator TextBox
    - Brand Name TextBox
    - Brand NO. TextBox
    - Email TextBox
    - All Permission DropDownMenu (includes options: On, Off, All Permission)
    - Start Date and Time
    - End Date and Time

  - Finance List

    - Displays all Finance records. Each Finance entry includes Creator, Brand NO., Brand Name, Subtotal (USD), Sales Account (USD), Cashier Account (USD), Withdraw Permission, and Actions information.

  - Asset Details

    - **Assets Details Table Data**
      - Crypto: Displays the type of cryptocurrency.
      - Total Value (USD): Displays the total value of the cryptocurrency converted to USD.
      - Total Amount: Displays the sum of Sales Account and Cashier Account amounts.
      - Sales Account: Displays the asset details corresponding to the Sales Account.
      - Cashier Account: Displays the asset details corresponding to the Cashier Account.
      - Sub-Total: Displays the total amount converted to USD.

    - **History Table Data**
      - Time: Displays the transaction time.
      - Account: Displays the transaction account.
      - Type: Displays the transaction type.
      - Amount: Displays the transaction amount and cryptocurrency type.
      - Export: Allows exporting of merchant financial reports.

    - **Transfer**
      - This activity will help the merchant transfer all assets from the Cashier Account to the Sales Account immediately and notify the merchant.

  - Withdraw Permission

    - **User Info Table Data**
      - Create On: The date and time when the merchant was added.
      - Creator: The person who added the merchant.
      - Brand Name: The display name when the brand was created.
      - Brand No: The unique value when the brand was created.
      - Country: The country where the merchant is located.
      - Industry: The industry to which the merchant belongs.
      - Phone No.: The merchant's phone number.
      - Email: The merchant's email.

    - **Modify History Table Data**
      - Displays the actions taken to adjust permissions and the date and time of adjustments.

    - **Withdraw Permission Toggle**
      - When set to True, the merchant can perform withdrawals.

    - **Save Button**
      - Saves the current settings for the merchant's withdrawal permission changes.

  - Deposit

    - **User Info Table Data**
      - Create On: The date and time when the merchant was added.
      - Creator: The person who added the merchant.
      - Brand Name: The display name when the brand was created.
      - Brand No: The unique value when the brand was created.
      - Country: The country where the merchant is located.
      - Industry: The industry to which the merchant belongs.
      - Phone No.: The merchant's phone number.
      - Email: The merchant's email.

    - **Deposit History Table Data**
      - Time: Displays the deposit time.
      - Amount: Displays the deposit amount and cryptocurrency type.

    - **Deposit**
      - Which Asset: A required dropdown menu to select the cryptocurrency to be deposited.
      - Amount: Input the deposit amount, which can include decimals. Click "Max" to auto-fill the maximum depositable amount.
      - Remarks: Input box for remarks.
      - Click the "Submit" button to perform the deposit for this merchant.

  - Withdrawal

    - **User Info Table Data**
      - Create On: The date and time when the merchant was added.
      - Creator: The person who added the merchant.
      - Brand Name: The display name when the brand was created.
      - Brand No: The unique value when the brand was created.
      - Country: The country where the merchant is located.
      - Industry: The industry to which the merchant belongs.
      - Phone No.: The merchant's phone number.
      - Email: The merchant's email.

    - **Withdraw History Table Data**
      - Time: Displays the withdrawal time.
      - Amount: Displays the withdrawal amount and cryptocurrency type.

    - **Withdrawal**
      - Account Type Radio Button: Choose to withdraw from the merchant's Cashier Account or Sales Account.
      - Which Asset: A required dropdown menu to select the cryptocurrency to be withdrawn.
      - Amount: Input the withdrawal amount, which can include decimals. Click "Max" to auto-fill the maximum withdrawable amount.
      - Remarks: Input box for remarks.
      - Click the "Submit" button to perform the withdrawal for this merchant.

- Commission Rate

  - Query Module

    - Name TextBox
    - Start Date and Time
    - End Date and Time

  - Commission List

    - Displays all Commission records. Each Commission entry includes Create On, Name, Cashier Commission Rate, Sales Commission Rate, Merchant Sum, Remarks, and Actions information.

  - Add Commission Group

    - Fee Name: Required field.
    - Remarks: Required field.
    - Cashier Commission Rate TextBox: Only accepts positive floating-point numbers or positive integers.
    - Sales Commission Rate TextBox: Only accepts positive floating-point numbers or positive integers.
    - Save Button: Click to add a new Commission Group.

  - Modify Commission

    - Fee Name: Required field.
    - Remarks: Required field.
    - Cashier Commission Rate TextBox: Only accepts positive floating-point numbers or positive integers.
    - Sales Commission Rate TextBox: Only accepts positive floating-point numbers or positive integers.
    - Save Button: Click to modify the Commission Group.
    - Merchant List: Displays all Merchant records. Each Merchant entry includes Create On, Creator, Brand NO., Brand Name, API Key, Sub-merchant, Owner, Country, Phone No., Email, Status, and Actions information.
    - Move Out/Move In Buttons: Allows adding or removing the selected Merchant to/from the Commission Group.

  - Delete Commission

    - Deletes a specific Commission. Upon successful deletion, the commission settings for Merchants and Distributors in that group are removed.

- Limitation

  - Query Module

    - Name TextBox
    - Start Date and Time
    - End Date and Time

  - Limitation List

    - Displays all Limitation records. Each Limitation entry includes Create On, Name, Crypto Sales Maximum Per Txn, Crypto Cashier Maximum Per Txn, Crypto Sales Maximum Per Day, Crypto Cashier Maximum Per Day, Merchant Sum, Remarks, and Actions information.

  - Add Limitation

    - Name: Required field.
    - Remarks: Required field.
    - Crypto Sales Maximum Per Txn TextBox: Only accepts positive floating-point numbers or positive integers and cannot exceed Crypto Sales Maximum Per Day.
    - Crypto Sales Maximum Per Day TextBox: Only accepts positive floating-point numbers or positive integers.
    - Crypto Cashier Maximum Per Txn TextBox: Only accepts positive floating-point numbers or positive integers and cannot exceed Crypto Cashier Maximum Per Day.
    - Crypto Cashier Maximum Per Day TextBox: Only accepts positive floating-point numbers or positive integers.
    - Save Button: Click to add a new Limitation setting.

  - Modify Limitation

    - Name: Required field.
    - Remarks: Required field.
    - Crypto Sales Maximum Per Txn TextBox: Only accepts positive floating-point numbers or positive integers and cannot exceed Crypto Sales Maximum Per Day.
    - Crypto Sales Maximum Per Day TextBox: Only accepts positive floating-point numbers or positive integers.
    - Crypto Cashier Maximum Per Txn TextBox: Only accepts positive floating-point numbers or positive integers and cannot exceed Crypto Cashier Maximum Per Day.
    - Crypto Cashier Maximum Per Day TextBox: Only accepts positive floating-point numbers or positive integers.
    - Merchant List: Displays all Merchant records. Each Merchant entry includes Create On, Creator, Brand NO., Brand Name, API Key, Sub-merchant, Owner, Country, Phone No., Email, Status, and Actions information.
    - Move Out/Move In Buttons: Allows adding or removing the selected Merchant to/from the Limitation Group.
    - Save Button: Click to modify the Limitation setting.

  - Delete Limitation

    - Deletes a specific Limitation. Upon successful deletion, the limitation settings for Merchants and Distributors in that group are removed.

### Orders Page

- Overview

  - Query Module

    - Start Date and Time
    - End Date and Time

  - Report Data

    - **Crypto Sales Overview** includes the following details:
      1. Order Sum
      2. Volume (USDT)
      3. Commission Generated

    - **Crypto Cashier Overview** includes the following details:
      1. Order Sum
      2. Volume (USDT)
      3. Commission Generated

- Crypto Sales

  - Query Module

    - Order No. TextBox
    - Hash TextBox
    - Creator TextBox
    - Store NO. TextBox
    - Brand NO. TextBox
    - Crypto Type TextBox
    - All Settlements DropDownMenu
    - Sub-merchant TextBox
    - Start Date and Time
    - End Date and Time

  - Crypto Sales List

    - Displays all Crypto Sales orders. Each order includes Create On, Order No., Creator, Brand NO., Merchant Name, Sub-merchant, Store NO., Method, Actual Cost of Sales, Commission, Service Fee, Total Sales, Deposit Amount, Crypto/Settlement, Settlement/Fiat, and Txn Hash information.

- Crypto Cashier

  - Query Module

    - Order No. TextBox
    - Hash TextBox
    - Creator TextBox
    - Store NO. TextBox
    - Brand NO. TextBox
    - Crypto Type TextBox
    - All Settlements DropDownMenu
    - Sub-merchant TextBox
    - Start Date and Time
    - End Date and Time

  - Crypto Cashier List

    - Displays all Crypto Cashier orders. Each order includes Create On, Order No., Creator, Brand NO., Merchant Name, Sub-merchant, Store NO., Method, Actual Cost of Sales, Commission, Service Fee, Total Sales, Deposit Amount, Crypto/Settlement, Settlement/Fiat, and Txn Hash information.

- pay-via-email

  - Query Module

    - Merchant TextBox
    - Invoice No. TextBox
    - Customer TextBox
    - Email TextBox
    - Store No. TextBox
    - Staff No. TextBox
    - All Fiat DropDownMenu
    - All Blockchain DropDownMenu
    - Start Date and Time
    - End Date and Time

  - pay-via-email List

    - Displays all pay-via-email orders. Each order includes Invoice Date, Due by, Payment Amount, Fiat Amount, Invoice Rate, Customer Email, Customer Name, Invoice No., Blockchain, Invoice Notes, Status, and Product Details information.

- Merchant Deposit

  - Query Module

    - Order No. TextBox
    - Start Date and Time
    - End Date and Time

  - Merchant Deposit List

    - Displays all merchant deposit records. Each record includes Create On, Order No., Brand NO., Amount, Crypto, Type, and Status information.

- Merchant Withdraw

  - Query Module

    - Order No. TextBox
    - Brand NO. TextBox
    - All Type DropDownMenu (includes options: Manually, Agent, Online, All Type)
    - All Accounts DropDownMenu (includes options: Crypto Cashier account, Crypto Sales account, All Accounts)
    - Start Date and Time
    - End Date and Time

  - Merchant Withdraw List

    - Displays all merchant withdrawal records. Each record includes Create On, Order No., Brand NO., Amount, Crypto, Type, Account, and Status information.

### Funds Page

- Overview

    - Total asset amount, with a toggle button to switch between fiat currency or stablecoin converted values.

    - Click on the Main Account Slide to display the account balance along with the following report, which includes cryptocurrencies USDT and DAI:
      Crypto, Total Value, Total Amount, Available Amount, In Order Amount, Actions.

    - Click on the Commission Account Slide to display the account balance along with the following report, which includes cryptocurrencies USDT and DAI:
      Crypto, Total Value, Total Amount, Available Amount, In Order Amount, Actions. The commission account can enable the AutoTransfer toggle to automatically transfer the account’s assets to the main account.

    - Main Account History

        - Search Module:
            - All Cryptos DropDownMenu with USDT and DAI options.
            - All Summary DropDownMenu.
            - Directions DropDownMenu with Increase, Decrease, and All Directions options.
        
        - Asset Change List:
            - Displays all asset change records, including Time, Account, Balance, Summary, and Related Order information.

- Deposit

    - Deposit Account:
        - DropDownMenu to select the deposit account, currently only the Main Account is available.

    - Deposit Cryptocurrency:
        - DropDownMenu to select the deposit cryptocurrency, currently USDT or DAI.

    - Deposit Network:
        - DropDownMenu to select the deposit network, currently ERC, BEP, and TRON.

    - Deposit Address:
        - Automatically generates the deposit address and QR code based on the selected deposit cryptocurrency and network.

    - Deposit Record:
        - Displays the exact time, cryptocurrency, and amount when a deposit is made.

- Withdraw

    - Withdraw Account:
        - DropDownMenu to select the withdrawal account, currently the Main Account or Commission Account.

    - Withdraw Cryptocurrency:
        - DropDownMenu to select the withdrawal cryptocurrency, currently USDT or DAI.

    - Withdraw Network:
        - DropDownMenu to select the withdrawal network, currently ERC, BEP, and TRON.

    - Withdraw Address:
        - A required field; the input must comply with the address format based on the selected withdrawal network.

    - Withdraw Amount:
        - A required field; a value greater than 0 must be entered. Clicking "Max" will automatically fill in the maximum withdrawal amount for the selected account.

    - Withdraw Record:
        - Displays the exact time, cryptocurrency, and amount when a withdrawal is made.

- Transfer

    - From Account:
        - DropDownMenu to select the from account, currently the Main Account or Commission Account.

    - To Account:
        - DropDownMenu to select the to account, currently the Main Account or Commission Account.

    - Transfer Cryptocurrency:
        - DropDownMenu to select the transfer cryptocurrency, currently USDT or DAI.

    - Transfer Amount:
        - A required field; a value greater than 0 must be entered. Clicking "Max" will automatically fill in the maximum transferable amount for the selected account.

    - Transfer Record:
        - Displays the exact time, cryptocurrency, and amount when a transfer is made.

### Settings Page

- Timezone Settings

    - You can select a timezone for different countries/regions from the dropdown menu and save changes accordingly.

- Fiat Currency Unit

    - You can select a different fiat currency from the dropdown menu and save changes accordingly.

- Withdraw 2FA Settings

    - When withdrawing, prompts for Google and email 2FA authentication. SMS verification can also be enabled. Click "Save" to save the settings.

### Appearance Module

- Language

    - Change the system's display language.

- Theme Mode

    - Switch the page between day mode and night mode.

- Full Screen

    - Toggle between full screen and normal screen mode.

- Search

    - Use keywords to search for functions within the system.

- Sidebar

    - Toggle the left sidebar expansion.

- Account Module

    - Account Information:
        - You can edit Brand Name, Email, Phone Number, Login Password, Fund Password, and Google Authenticator information.

    - Logout Function

- Appearance Theme Module

    - Customize appearance settings, such as fonts, colors, background, etc., according to personal preference.

## Acceptance Criteria

### UI Verification

### Functionality Verification

### Interface Verification

### Blockchain Data Verification

### Performance Verification
