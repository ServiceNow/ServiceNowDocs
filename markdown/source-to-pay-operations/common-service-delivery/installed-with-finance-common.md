---
title: Components installed with Finance Common Architecture
description: Several types of components are installed with the installation of the Finance Common Architecture application, including tables and user roles.
locale: en-US
release: australia
product: Common Service Delivery
classification: common-service-delivery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Learn about FSC common applications, Common applications, Finance and Supply Chain applications, Finance and Supply Chain]
---

# Components installed with Finance Common Architecture

Several types of components are installed with the installation of the Finance Common Architecture application, including tables and user roles.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Finance admin\[sn\_fin.finance\_admin\]

</td><td>

Generate fiscal and accounting periods.

</td><td>

sn\_fin.finance\_user

</td></tr><tr><td>

Finance user\[sn\_fin.finance\_user\]

</td><td>

View and edit accounting and fiscal periods.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account Access\[sn\_fin\_gl\_access\]

</td><td>

Defines the access control for general ledger \(GL\) accounts, specifying who can view or modify particular GL records.

</td></tr><tr><td>

Account Access Rule\[sn\_fin\_gl\_access\_rule\]

</td><td>

Defines rules that govern access control to the general ledger, ensuring proper segregation of duties and user permissions.

</td></tr><tr><td>

Account Group Mapping\[sn\_fin\_gl\_group\_mapping\]

</td><td>

Maps general ledger accounts to specific groups for reporting purposes, ensuring proper categorization and alignment with business functions.

</td></tr><tr><td>

Accounting Periods\[sn\_fin\_accounting\_period\]

</td><td>

Defines accounting periods for financial reporting, such as fiscal year, quarters, and months.

</td></tr><tr><td>

Balance\[sn\_fin\_balance\]

</td><td>

Tracks balances for different financial entities, which could include balances for accounts, departments, or cost centers.

</td></tr><tr><td>

Base Invoice\[sn\_fin\_base\_invoice\]

</td><td>

Stores high-level details about invoices, such as invoice number, date, supplier, customer, and total amount.

</td></tr><tr><td>

Base Tax Line\[sn\_fin\_base\_tax\_line\]

</td><td>

Contains detailed tax line items associated with invoices, including tax rates, tax amounts, and tax classifications.

</td></tr><tr><td>

Currency Conversion Setting\[sn\_fin\_gl\_currency\_setting\]

</td><td>

Contains settings and preferences for handling multiple currencies in the general ledger, including conversion rates and currency codes.

</td></tr><tr><td>

Due Date Rule\[sn\_fin\_gl\_due\_rule\]

</td><td>

Defines rules for determining when accounts payable or receivable amounts are due, including due dates, grace periods, and interest rates.

</td></tr><tr><td>

ERP Source\[sn\_fin\_erp\_source\]

</td><td>

Maps and stores information regarding source systems from which financial data is imported or integrated into the financial system.

</td></tr><tr><td>

ERP source mapping\[sn\_fin\_erp\_source\_mapping\]

</td><td>

Maps external ERP system data to the internal financial schema, facilitating data integration and synchronization.

</td></tr><tr><td>

Excel Data Import\[sn\_fin\_excel\_data\_import\]

</td><td>

Supports the asynchronous excel data import for a journal entry.

</td></tr><tr><td>

Period\[sn\_fin\_period\]

</td><td>

Maps external ERP system data to the internal financial schema, facilitating data integration and synchronization.

</td></tr><tr><td>

Finance Exchange Rates\[sn\_fin\_fx\_rate\]

</td><td>

Maintains foreign exchange rates used for currency conversions in financial transactions, tracking historical and current rates.

</td></tr><tr><td>

Fixed Asset\[sn\_fin\_fixed\_asset\]

</td><td>

Stores information about fixed assets owned by the organization, including asset type, value, depreciation, and location.

</td></tr><tr><td>

Fixed Asset to Asset\[sn\_fin\_m2m\_fixed\_asset\]

</td><td>

Represents a many-to-many relationship between fixed assets and various attributes, such as locations, departments, or asset classifications.

</td></tr><tr><td>

GL Rule\[sn\_fin\_gl\_rule\]

</td><td>

Defines rules and policies for general ledger account management, including rules for automated journal entries and account mappings.

</td></tr><tr><td>

GL Support\[sn\_fin\_gl\_support\]

</td><td>

Provides supporting data for general ledger accounts, such as supplementary details or documents linked to specific transactions.

</td></tr><tr><td>

Import Error\[sn\_fin\_import\_error\]

</td><td>

Tracks errors encountered during the import process, typically for financial data, to aid in troubleshooting and data validation.

</td></tr><tr><td>

Industry\[sn\_fin\_industry\]

</td><td>

Holds industry classifications or categories relevant to the suppliers, customers, or financial entities in the system.

</td></tr><tr><td>

Ledger\[sn\_fin\_ledger\]

</td><td>

The main table for storing general ledger \(GL\) entries, summarizing financial transactions by account, period, and other dimensions.

</td></tr><tr><td>

Ledger Account\[sn\_fin\_gl\_account\]

</td><td>

Stores balances for subledgers, such as accounts payable or receivable, tracking amounts owed or due by customers and suppliers.

</td></tr><tr><td>

Ledger Account Group\[sn\_fin\_gl\_group\]

</td><td>

Organizes general ledger accounts into groups for reporting and analysis purposes, such as by department or business segment.

</td></tr><tr><td>

Ledger Balance\[sn\_fin\_gl\_balance\]

</td><td>

Holds the balance of general ledger accounts, tracking current balances, debits, credits, and running totals.

</td></tr><tr><td>

Legal Entity\[sn\_fin\_legal\_entity\]

</td><td>

Contains information about legal entities within the organization, such as corporations or limited liability companies, along with their legal statuses.

</td></tr><tr><td>

Office Location\[sn\_fin\_office\_location\]

</td><td>

Contains information about office locations, including address, contact details, and organizational unit associated with each location.

</td></tr><tr><td>

Organization\[sn\_fin\_organization\]

</td><td>

Contains details about the organizations within the financial system, including business units, departments, and organizational hierarchies.

</td></tr><tr><td>

Organization Tax Details\[sn\_fin\_org\_tax\_detail\]

</td><td>

Contains tax-related information for different organizations, including tax registration numbers, rates, and jurisdictions.

</td></tr><tr><td>

Purchasing Entity\[sn\_fin\_purchasing\_entity\]

</td><td>

Stores information about entities involved in purchasing transactions, such as divisions or business units within an organization.

</td></tr><tr><td>

Properties\[sn\_fin\_properties\]

</td><td>

Stores various configuration properties related to financial data management, such as thresholds, settings, or flags used throughout the system.

</td></tr><tr><td>

Profit Center\[sn\_fin\_profit\_center\]

</td><td>

Defines profit centers within the organization, enabling financial reporting and analysis by business units or operational segments.

</td></tr><tr><td>

Signer\[sn\_fin\_signer\]

</td><td>

Stores information about individuals or entities authorized to sign financial documents or approve transactions.

</td></tr><tr><td>

Supplier\[sn\_fin\_supplier\]

</td><td>

Contains details about suppliers, including name, address, contact information, and payment terms

</td></tr><tr><td>

Supplier Legal Entity Mapping\[sn\_fin\_supplier\_detail\]

</td><td>

Contains more detailed information about individual suppliers, including banking details, payment methods, and credit terms.

</td></tr><tr><td>

Supplier Payment Information\[sn\_fin\_supplier\_payment\]

</td><td>

Stores records of payments made to suppliers, including payment dates, amounts, and methods of payment.

</td></tr><tr><td>

Subledger Balance\[sn\_fin\_subledger\_balance\]

</td><td>

Maps general ledger accounts to specific groups for reporting purposes, ensuring proper categorization and alignment with business functions.

</td></tr><tr><td>

Tax Code\[sn\_fin\_tax\_code\]

</td><td>

Stores various tax codes used for transactions, including sales tax, VAT, and other region-specific tax codes.

</td></tr><tr><td>

Tax Type\[sn\_fin\_tax\_type\]

</td><td>

Contains different tax types used in financial transactions, such as VAT, sales tax, and withholding tax, along with their applicable rules.

</td></tr><tr><td>

Threshold Rule\[sn\_fin\_gl\_threshold\_rule\]

</td><td>

Defines rules for thresholds in the general ledger, such as limits for certain accounts, to ensure compliance with financial policies.

</td></tr><tr><td>

Unit of measure\[sn\_fin\_uom\]

</td><td>

Manages the unit of measurement \(UOM\) standards used across financial transactions, including different types like kilograms, liters, and hours.

</td></tr></tbody>
</table>