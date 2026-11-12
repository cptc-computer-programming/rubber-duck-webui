# Chapter 4 Exercises 1–8

Using the AP database, complete the following exercises.

**Unless otherwise stated, use explicit JOIN syntax.**

### 1.
Write a SELECT statement that returns all columns from the Vendors table inner-joined with the Invoices table.

### 2.
Write a SELECT statement that returns four columns:

| Column | Description |
|---|---|
| VendorName | From the Vendors table |
| InvoiceNumber | From the Invoices table |
| InvoiceDate | From the Invoices table |
| Balance | InvoiceTotal minus the sum of PaymentTotal and CreditTotal |

The result set should have one row for each invoice with a non-zero balance. Sort by VendorName in ascending order.

### 3.
Write a SELECT statement that returns three columns:

| Column | Description |
|---|---|
| VendorName | From the Vendors table |
| DefaultAccountNo | From the Vendors table |
| AccountDescription | From the GLAccounts table |

The result set should have one row for each vendor, with the account number and account description for that vendor's default account number.

Sort by AccountDescription, then by VendorName.

### 4.
Generate the same result set described in exercise 2, but use implicit JOIN syntax.

### 5.
Write a SELECT statement that returns five columns from three tables, all using column aliases:

| Alias | Column |
|---|---|
| Vendor | VendorName |
| Date | InvoiceDate |
| Number | InvoiceNumber |
| # | InvoiceSequence |
| LineItem | InvoiceLineItemAmount |

Assign the following correlation names to the tables:

| Correlation Name | Table |
|---|---|
| v | Vendors |
| i | Invoices |
| li | InvoiceLineItems |

Sort the final result set by Vendor, Date, Number, and #.

### 6.
Write a SELECT statement that returns three columns:

| Column | Description |
|---|---|
| VendorID | From the Vendors table |
| VendorName | From the Vendors table |
| Name | A concatenation of VendorContactFName and VendorContactLName, with a space in between |

The result set should have one row for each vendor whose contact has the same first name as another vendor's contact.

Sort by Name.

*Hint: Use a self-join.*

### 7.
Write a SELECT statement that returns two columns from the GLAccounts table:

- AccountNo
- AccountDescription

The result set should have one row for each account number that has never been used.

Sort by AccountNo.

*Hint: Use an outer join to the InvoiceLineItems table.*

### 8.
Use the UNION operator to generate a result set consisting of two columns from the Vendors table:

- VendorName
- VendorState

If the vendor is in California, the VendorState value should be `"CA"`. Otherwise, the VendorState value should be `"Outside CA"`.

Sort by VendorName.
