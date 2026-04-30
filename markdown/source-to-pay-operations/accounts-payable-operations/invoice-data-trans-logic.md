---
title: Invoice data transformation logic
description: Accounts Payable Operations integration with Document Intelligence converts the invoice and invoice line field values from the invoice document to a format supported by the system that processes the invoice.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [How Accounts Payable Operations integration with Document Intelligence works, Install Accounts Payable Operations integration with Document Intelligence, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice data transformation logic

Accounts Payable Operations integration with Document Intelligence converts the invoice and invoice line field values from the invoice document to a format supported by the system that processes the invoice.

## Type deriving logic

The application includes the following logic for deriving the type field on the invoice.

-   Considers the purchase order value in the invoice stage record
-   If the purchase order value isn’t empty, then the invoice type is set to PO type.
-   If the purchase order value is empty, then the invoice type is set to Non- PO type.

## Date conversion logic

The application includes the following logic for converting date formats mentioned in the invoice document:

-   Considers YYY-MM-DD as the ISO format and the system format for date conversion.
-   Considers dates only in MM-DD-YYYY format for conversion.
-   Doesn’t consider dates in DD-MM-YYYY format if DD is less than 12.

|Date format in the incoming invoice|Converted date format|
|-----------------------------------|---------------------|
|2nd Sep, 2022|2022-09-02|
|3rd September, 2022|2022-09-02|
|02-Sep-2022|2022-09-02|
|02-Sept-2022|2022-09-02|
|Sept-02-2022|2022-09-02|
|Sep-02-2022|2022-09-02|
|09-02-2022|2022-09-02|
|02-09-2022|2022-02-09|
|09/02/2022|2022-09-02|
|02/09/2022|2022-02-09|

## Currency conversion logic

The application supports different locale such as US, European and Indian number systems. For example, "X,XXX.XXX", "X.XXX,XX", "XX,XX.XXX" where X is a single-digit positive number.

|Scenario|Currency format in the incoming invoice|Converted currency format|
|--------|---------------------------------------|-------------------------|
|Amount followed by a space and the currency code|76 EUR|76 EUR|
|Amount followed by a space and the currency symbol|76 €|76 EUR|
|Currency code followed by multiple spaces and the amount|EUR 76|76 EUR|
|Currency symbol followed by multiple spaces and the amount|€ 76|76 EUR|
|Amount without a currency code or symbol|76|76 \(followed by the purchase order currency or the session currency\)|
|Amount separated by comma, dot or any other grouping or decimal separator followed by a space and the currency code|7.123.456,99 EUR|7123456.99 EUR|
|Amount followed by the currency code without any space|76EUR|76 EUR|
|Amount followed by the currency symbol without any space|76€|76 EUR|
|Currency code followed by the amount without any space|EUR76|76 EUR|
|Currency symbol followed by the amount without any space|€76|76 EUR|

The application first looks for the active unique currency code in the Currency \[fx\_currency\] table when an incoming invoice amount has a currency symbol or code. If multiple currency matches are found or the incoming invoice amount has no currency code or symbol, then the application runs the defaulting currency logic depending on the invoice type as follows.

-   PO invoice - Searches for purchase order and related currency, and sets the invoice currency to purchase order currency. In case of missing purchase order or related currency, the invoice currency is set to system currency.
-   Non- PO invoice - Searches for legal entity and local currency, and sets the invoice currency to the legal entity's local currency. In the case of missing legal entity and local currency, the invoice currency is set to system currency.

## Unit Price conversion logic

The application supports different locale such as US, European and Indian number format locale. For example, "X,XXX.XXX", "X.XXX,XX", "XX,XX.XXX" where X is a single-digit positive number.

If the incoming invoice unit price consists of currency symbol or code present in Currency \[fx\_currency\] table, then the unit price is converted. For example, $ XX,XXX,XXX.XX or USD XX,XX,XXX.X, where X is a single-digit positive number.

|Unit price mentioned in the incoming invoice|Converted unit price|
|--------------------------------------------|--------------------|
|1,000,25.10|100025.10|
|1,00,025.10|100025.10|
|$1,000,25.10|100025.10|
|1,000,25.10 $|100025.10|
|USD1,00,025.10|100025.10|
|1,00,025.10 USD|100025.10|

## Decimal conversion logic

The application supports different locale such as US, European and Indian decimal format locale. For example, "X,XXX.XXX", "X.XXX,XX", "XX,XX.XXX" where X is a single-digit positive number.

Currency groupings on invoice and invoice lines are determined based on the user system locale settings. European currencies consider comma as a decimal separator and dot as a thousand separators. In some cases, various characters can also be used as grouping separator. The incoming invoice and invoice lines present in \[sn\_ap\_ic\_invoice\_stage\] and \[sn\_ap\_ic\_invoice\_line\_stage\] tables are converted based on the positioning of decimal and thousand separators.

**Note:** During conversion, for numbers such as 100,251 and 100.251, the system checks for other decimal separators mentioned in the invoice, and converts it to the appropriate decimal format. If the invoice contains fields with single decimal separator, then conversion does not apply for the invoice, and the value is set to empty as shown in the table below.

For more information on currency conversion, see [Currency administration](https://www.servicenow.com/docs/access?context=currency&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

|Decimal format mentioned in the incoming invoice|Converted decimal format|
|------------------------------------------------|------------------------|
|1,000,25.10|100025.10|
|1,00,025.10|100025.10|
|100,251|100,251|
|10.102,510|10102.51|
|10.10.102,510|1010102.51|
|100,251| |
|100.251| |

## Logic to fetch reference field values

<table id="table_rxz_svm_1xb"><thead><tr><th>

Reference Field

</th><th>

Logic to fetch the field value

</th></tr></thead><tbody><tr><td>

Legal Entity

</td><td>

The system fetches the value by checking the following values in the order listed:1.  Bill to company
2.  Street, City, State, Country, Zip
3.  City, State, Country, Zip
4.  State, Country, Zip
5.  Country, Zip
6.  Country
7.  Zip

</td></tr><tr><td>

Purchase Order

</td><td>

The system does the following:-   The system considers the purchase order value mentioned in the invoice stage
-   If the purchase order value is prefixed with special characters, alphabets or zeroes, then the application ignores the prefixes and matches the remaining purchase order value with the ERP number from the purchase order table
-   If a unique purchase order is found then the application populates the purchase order in the invoice

</td></tr><tr><td>

Supplier

</td><td>

The system does one of the following:-   The system considers the value mentioned in the invoice and does a complete match with supplier in Supplier table.
-   If the invoice contains a purchase order associated with the supplier, the application matches with the supplier name mentioned in the invoice with the supplier name of purchase order and populates the supplier.
-   If the invoice document contains supplier name with more than two words, the application performs partial name match against the supplier details in the supplier table along with street address or city. Example. If the invoice document contains supplier name as XX Corp, and the supplier name in the supplier table is XX Ltd, the application matches XX in supplier table along with the address and populates the invoice document with the corresponding supplier.

If a unique supplier record is found in any of the above, then the application populates the supplier in the invoice.

</td></tr><tr><td>

Country

</td><td>

The system does one of the following:-   Considers the value mentioned in the invoice
-   If this value isn’t mentioned in the invoice, it populates the International Organization for Standardization \(ISO\) short country name or the ISO long country name

</td></tr><tr><td>

Subtotal, Tax amount, Other charges

</td><td>

The system does the following:-   If the invoice contains XX.XXX,XXX the application groups the numeric to four digits after decimal separator.
-   If the invoice contains three numeric digits after the separator, the application sets the invoice fields to empty.
-   If the invoice contains a combination of decimal and thousand separators in a form, the application defaults to the numeric value to the decimal separator.

</td></tr></tbody>
</table>**Parent Topic:**[How Accounts Payable Operations integration with Document Intelligence works](apm-docintel-how-it-works.md)

