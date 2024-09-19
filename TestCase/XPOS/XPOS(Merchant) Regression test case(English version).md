# XPOS (Merchant)

## Testing OS

### Web (Desktop)

- Primary testing OS

### API

- Secondary testing OS

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

### Networks

- ERC20

- BEP20

- TRC20

## Test Scenarios

### Home Page

### Store Page

- Store List

	- Displays a list of all stores. Each store includes details such as Create On, Store number, Store name, Physical Address, Device Sum, Staff Sum, Fee Group, Status, and Actions.

- Search Module

	- Store number

	- Store name

	- Fee group

	- Status

	- Create time

- Add Store

	- Store name is a required string field.

	- Physical Address is a required string field.

	- Store phone number only accepts numbers.

	- Fees & tax management is a required dropdown menu, showing all fee settings.

	- Clicking the fee settings link redirects to the Fees & Tax Management page.

	- Clicking the Add button adds a new store.

- Edit Store

	- Store name is a required string field.

	- Physical Address is a required string field.

	- Store phone number only accepts numbers.

	- Fees & tax management is a required dropdown menu showing all set fees.

	- Status is a required dropdown menu for enabling or disabling the store.

	- Clicking the fee settings link redirects to the Fees & Tax Management page.

	- Clicking the Save button saves the store changes.

- Delete Store

	- Clicking Delete does not allow the store to be deleted if a Device is bound.

	- Clicking Delete does not allow the store to be deleted if Staff is bound.

	- Clicking Delete allows the store to be deleted if no Device or Staff is bound.

### QR Code Page

- QR Code List

	- Displays all QR codes. Each includes Code No., Store, Email, QR Code, Status, and Actions.

- Create QR Code

	- Select a Store to create a QR code. If no store has been created or the store already has a QR code, the QR code cannot be created.

	- Email is a required field and allows repeated email addresses.

- Edit QR Code

	- You can edit the email and status for any created QR code.

	- When the status is Active, the QR code can be used for payments. When Inactive, a 404 error is shown.

- QR Code Details

	- Payment QR code link.

	- Copy payment QR code link.

	- Download QR code image in A5 size.

	- Download QR code image in A4 size.

	- Download QR code image.

### Staff Page

- Staff List

	- Displays all staff. Each includes Create On, User No., User Name, Phone No., Accessible Store, Status, and Actions.

- Search Module

	- User No. TextBox

	- User Name TextBox

	- Phone No. TextBox

	- Status DropDownMenu with Activated, Inactive, and All Status options.

	- Start Date Time

	- End Date Time

- Add Staff

	- First name is a required string field.

	- Last name is a required string field.

	- Store is a required multi-select dropdown menu, showing all stores.

	- Staff phone number is required and includes a country dropdown. After selecting a country, the country code is auto-filled, and the phone number is validated.

	- Staff Login Password is a required string field, with a minimum of 8 characters including uppercase, lowercase, and numbers.

	- Staff Fund Password is a required string field with exactly 6 digits.

	- Clicking the Create button adds a new staff member.

- Edit Staff

	- First name is a required string field.

	- Last name is a required string field.

	- Store is a required multi-select dropdown menu, showing all stores.

	- Staff phone number is pre-filled from the Add step and cannot be modified.

	- Staff Login Password is a required string field, with a minimum of 8 characters including uppercase, lowercase, and numbers.

	- Staff Fund Password is a required string field with exactly 6 digits.

	- Clicking the Save button saves the staff changes.

- Delete Staff

	- Clicking the confirm button deletes the staff member.

	- Clicking the cancel button cancels the deletion.

- Limitations

	- Limitations List

		- Displays all limitations. Each includes Create On, Staff No., Staff Name, Phone No., Crypto Sales Maximum Per Transaction, Crypto Sales Maximum Per Day, Crypto Cashier Maximum Per Transaction, Crypto Cashier Maximum Per Day, and Actions.

	- Search Module

		- Search by User No. You can click "Reset" to clear the search filters.

	- Add Limitation

		- Staff is a required dropdown. Select any staff member who hasn't been assigned limitations. Staff No., Staff Name, and Phone No. are auto-filled.

		- Crypto Sales Maximum Per Transaction is a required TextBox, only allowing numbers greater than 0.

		- Crypto Sales Maximum Per Day is a required TextBox, only allowing numbers greater than 0 and greater than the Crypto Sales Maximum Per Transaction.

		- Crypto Cashier Maximum Per Transaction is a required TextBox, only allowing numbers greater than 0.

		- Crypto Cashier Maximum Per Day is a required TextBox, only allowing numbers greater than 0 and greater than the Crypto Cashier Maximum Per Transaction.

		- Clicking the Create button adds the limitation.

	- Edit Limitation

		- Staff details are auto-filled for Staff No., Staff Name, and Phone No.

		- Crypto Sales Maximum Per Transaction is a required TextBox, only allowing numbers greater than 0.

		- Crypto Sales Maximum Per Day is a required TextBox, only allowing numbers greater than 0 and greater than the Crypto Sales Maximum Per Transaction.

		- Crypto Cashier Maximum Per Transaction is a required TextBox, only allowing numbers greater than 0.

		- Crypto Cashier Maximum Per Day is a required TextBox, only allowing numbers greater than 0 and greater than the Crypto Cashier Maximum Per Transaction.

		- Clicking the Save button saves the changes.

		- Clicking the Modify button saves the changes.

### Devices Page

- Device List

	- Displays all devices. Each includes Device IMEI, Device activation time, Manufacturer, Model, Store name, Staff, Device status, and Actions.

- Search Module

	- Device IMEI TextBox

	- Device Status DropDownMenu with Activated, Normal, and Damaged options.

	- Store can filter all devices that have not been deleted.

	- Start Date Time

	- End Date Time

- Edit Device

	- You can select which store to assign the device to.

- Delete Device

	- Deleting a device will remove it from the list and the device can be activated by another merchant.

### Orders Page

- Overview

	- Search Module

		- Start Date and Time

		- End Date and Time

		- Currency TextBox

		- All Blockchain dropdown menu

	- Summary Data

		- Crypto Sales Overview, including the following detailed data: 
      1. Order Sum 
      2. Transaction Volume 
      3. Service Fee 
      4. Tax

		- Crypto Cashier Overview, including the following detailed data: 
      1. Order Sum 
      2. Transaction Volume 
      3. Service Fee 
      4. Tax

- Crypto Sales

	- Search Module

		- Order No. TextBox

		- Hash TextBox

		- All Store multi-select dropdown list

		- All Staff multi-select dropdown list

		- Start Date and Time

		- End Date and Time

		- Currency TextBox

		- All Blockchain dropdown menu

	- Crypto Sales List

		- Displays all crypto sales orders. Each order includes:
        Create On, Order NO., Store, Staff, Device, Blockchain, Actual cost of sales, Commission, Service Fee, Total sales, Deposit amount, Crypto/Settlement, Settlement/Fiat, Transaction Hash, Actions.

- Crypto Cashier

	- Search Module

		- Order No. TextBox

		- Hash TextBox

		- All Store multi-select dropdown list

		- All Staff multi-select dropdown list

		- Start Date and Time

		- End Date and Time

		- Currency TextBox

		- All Blockchain dropdown menu

		- Payment Method dropdown menu

	- Crypto Cashier List

		- Displays all crypto cashier orders. Each order includes:
        Create On, Order NO., Store, Staff, Device, Blockchain, Method, Received USDT, Commission, Expense amount, Service Fee, Tax, Tax Type, Receivable, Payment Amount, Crypto/Settlement, Settlement/Fiat, Transaction Hash, Actions.

- Cash Sales

	- Search Module

		- Order No. TextBox

		- All Store multi-select dropdown list

		- All Staff multi-select dropdown list

		- Start Date and Time

		- End Date and Time

	- Cash Sales List

		- Displays all cash sales orders. Each order includes: 
        Create On, Order NO., Store, Staff, Total Amount.

- Pay-via-Email

	- Search Module

		- Invoice No. TextBox

		- Customer TextBox

		- Email TextBox

		- Store No. TextBox

		- Staff No. TextBox

		- All Fiat dropdown menu

		- All Blockchain dropdown menu

		- Start Date and Time

		- End Date and Time

	- Pay-via-Email List

		- Displays all pay-via-email orders. Each order includes:
        Invoice Date, Due by, Payment Amount, Fiat Amount, Invoice Rate, Customer Email, Customer Name, Invoice No., Blockchain, Invoice Notes, Status, Product Details.

---

### Funds Page

- Overview

	- Total asset amount, with a single-select button to switch between amounts in set fiat or stablecoins.

	- Clicking the Sales Account Slide displays the account balance and shows the following report, including currencies USDT and DAI:
        Crypto, Total Value, Total Amount, Available Amount, In Order Amount, Actions.

	- Clicking the Cashier Account Slide displays the account balance and shows the following report, including currencies USDT and DAI:
        Crypto, Total Value, Total Amount, Available Amount, In Order Amount, Actions.

- History

	- Search Module

		- Accounts Dropdown Menu including Cashier Account, Sales Account, All Accounts.

		- Summary dropdown menu

		- Directions Dropdown Menu including Increase, Decrease, All Directions.

	- Asset Change List

		- Displays all fund change records. Each transaction includes:
        Time, Type, Summary, Volume, Crypto.

- Deposit

	- Deposit Account

		- Dropdown menu to select the deposit account. Currently, only the Sales Account is selectable.

	- Deposit Currency

		- Dropdown menu to select the deposit currency. Currently, only USDT is selectable.

	- Deposit Network

		- Dropdown menu to select the deposit network. Currently, only ERC, BEP, TRON are selectable.

	- Deposit Address

		- Automatically generates the deposit address and QR code based on the deposit currency and network.

	- Deposit Record

		- When depositing, the exact time, currency, and amount will be shown.

- Withdrawal

	- Withdrawal Account

		- Dropdown menu to select the withdrawal account. Currently, Sales Account or Cashier Account can be selected.

	- Withdrawal Currency

		- Dropdown menu to select the withdrawal currency. Currently, USDT or DAI are selectable.

	- Withdrawal Network

		- Dropdown menu to select the withdrawal network. Currently, only ERC, BEP, TRON are selectable.

	- Withdrawal Address

		- A required field. The address format is validated based on the selected network.

	- Withdrawal Amount

		- A required field, must enter a number greater than 0. Clicking Max automatically inputs the maximum withdrawal value for the account.

	- Withdrawal Record

		- When withdrawing, the exact time, currency, and amount will be shown.

- Transfer

	- Transfer Out Account

		- Dropdown menu to select the transfer-out account. Currently, only the Cashier Account is selectable.

	- Transfer In Account

		- Dropdown menu to select the transfer-in account. Currently, only the Sales Account is selectable.

	- Transfer Currency

		- Dropdown menu to select the transfer currency. Currently, USDT or DAI are selectable.

	- Transfer Amount

		- A required field, must enter a number greater than 0. Clicking Max automatically inputs the maximum transfer value for the account.

	- Transfer Record

		- When transferring, the exact time, currency, and amount will be shown.

---

### API Management Page

- API Key

	- Add API Key

		- Name is a required TextBox.

		- IP whitelist TextBox, not required but must be a valid IP format.

		- Cashier Permission, optional Toggle. If set to True, this API Key can use cashier functions.

		- Payment password is a required TextBox, with a Retrieve button that redirects to the payment password recovery page.

		- Email verification code is a required TextBox. Click Get Code to obtain the email verification code.

		- Click Add to create the API Key. After creation, the API Key and Key Secret will be displayed.

	- Edit API Key

		- Name is a required TextBox.

		- IP whitelist TextBox, not required but must be a valid IP format.

		- Cashier Permission, optional Toggle. If set to True, this API Key can use cashier functions.

		- Payment password is a required TextBox, with a Retrieve button that redirects to the payment password recovery page.

		- Email verification code is a required TextBox. Click Get Code to obtain the email verification code.

		- Click Save to edit the API Key.

	- Delete API Key

		- Name is a required TextBox.

		- IP whitelist TextBox, not required but must be a valid IP format.

		- Cashier Permission, optional Toggle. If set to True, this API Key can use cashier functions.

		- Payment password is a required TextBox, with a Retrieve button that redirects to the payment password recovery page.

		- Email verification code is a required TextBox. Click Get Code to obtain the email verification code.

		- Click Confirm to delete the API Key.

	- API Key List

		- Displays all pay-via-email order lists. Each order includes:
        Invoice Date, Due by, Payment Amount, Fiat Amount, Invoice Rate, Customer Email, Customer Name, Invoice No., Blockchain, Invoice Notes, Status, Product details.

### Settings Page

- **Time Zone Settings**

	- A dropdown menu is available for selecting different time zones based on country or region, with the ability to Save changes.

- **Fee Management**

	- **Fee Rate List**

		- Displays all fee rates. Each rate includes:
          Fee name, Fee And Tax Id, Cash collection service charge, Cash collection tax, Crypto collection service charge, Crypto collection tax, Tax methods, Tax amount, and Actions.

	- **Add Fee Rate**

		- Dropdown menu for selecting tax-inclusive or tax-exclusive options. The right-side Display Toggle is set to True to show taxes on the XPOS and receipts.

		- Fee name is a required TextBox.

		- Cash collection service charge is a required TextBox, with input restricted to numbers greater than 0.

		- Cash collection tax is a required TextBox, with input restricted to numbers greater than 0.

		- Crypto collection service charge is a required TextBox, with input restricted to numbers greater than 0.

		- Crypto collection tax is a required TextBox, with input restricted to numbers greater than 0.

		- Click the Create button to add a new fee rate.

	- **Edit Fee Rate**

		- Dropdown menu for selecting tax-inclusive or tax-exclusive options. The right-side Display Toggle is set to True to show taxes on the XPOS and receipts.

		- Fee name is a required TextBox.

		- Cash collection service charge is a required TextBox, with input restricted to numbers greater than 0.

		- Cash collection tax is a required TextBox, with input restricted to numbers greater than 0.

		- Crypto collection service charge is a required TextBox, with input restricted to numbers greater than 0.

		- Crypto collection tax is a required TextBox, with input restricted to numbers greater than 0.

		- Click the Save button to modify the fee rate.

	- **Delete Fee Rate**

		- Click Confirm to delete the fee rate.

		- Click Cancel to cancel the deletion.

- **Settlement Type**

	- Dropdown menu available for selecting different stablecoins, with the ability to Save changes.

- **Fiat Currency Unit**

	- Dropdown menu available for selecting different fiat currencies, with the ability to Save changes.

---

### Appearance Module

- **Language**

	- Change the display language of the system.

- **Theme Mode**

	- Switch between day or night mode for the page appearance.

- **Fullscreen**

	- Enable or disable fullscreen mode.

- **Search**

	- Use keywords to search for functions within the system.

- **Toolbar**

	- Expand or collapse the left-side toolbar.

---

## Acceptance Criteria

### UI Verification

### Functional Verification

### API Verification

### On-Chain Data Verification

### Performance Verification