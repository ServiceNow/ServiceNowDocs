---
title: Import financial transactions
description: Import a Microsoft Excel spreadsheet of financial transaction data to start managing software spending.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Software Spend Detection, Software Asset Management, IT Asset Management]
---

# Import financial transactions

Import a Microsoft Excel spreadsheet of financial transaction data to start managing software spending.

## Before you begin

Role required: sam\_spend\_import or sam\_admin

**Note:** Users with the sam\_user role can manually create transaction records by selecting **New** at the top of the All Imported Transactions page.

## About this task

Your imported data can include all financial transaction data for your company. Software Spend Detection automatically determines whether each transaction is a software purchase. Before importing data, ensure that the fields **Vendor name**, **Transaction Description**, and **GL account** don't contain any identifiable information such as company or employee names. Make any necessary changes to the data before you import. All imported financial transaction data fields are read-only once loaded in your instance.

The import may take several hours when importing large numbers of transactions.

**Note:** Software Spend Detection currently supports transaction data in English only. If you would like to help train ServiceNow artificial intelligence using data in other languages, contact the ServiceNow IT Asset Management product team.

## Procedure

1.  Navigate to **All** &gt; **Software Spend Detection** &gt; **Administration** &gt; **Import Transactions**.

2.  Select **Download Template File \(.xlsx\)**.

3.  Copy your financial data into the template file.

    The required fields are **Transaction date**, **Vendor name** or **Description**, and **Type**. Fill in as many fields as possible for the most robust results.

    |Field|Description|
    |-----|-----------|
    |Transaction date|Required. Transaction date.|
    |Vendor name|Company associated with the transaction. Don't include any identifiable information such as your company or employee names. Provide at least one of vendor name or description.|
    |Description|Description of the purchase. Don't include any identifiable information such as your company or employee names. Provide at least one of vendor name or description.|
    |GL account|General ledger account or expense category. Don't include any identifiable information such as your company or employee names. Optional.|
    |Amount|Transaction amount. Optional.|
    |Type|Required. Select Accounts Payable or Expense. Accounts Payable transactions are from an accounting or procurement system. Expense transactions are from an employee expense system or credit card feed.|
    |Location|Location. Optional.|
    |Cost center|Cost center. Optional.|
    |Department|Department. Optional.|
    |Source|Name of the system that the transaction came from. Optional.|
    |Type detail|Description for the Type field. For Accounts Payable, examples are vendor bill or invoice payment. For Expense, examples are credit card purchase or employee reimbursement. Optional.|
    |External ID|ID of the transaction in the source system. Optional.|
    |Employee ID|Employee ID. Optional.|
    |Employee name|Employee name. Optional.|
    |Employee email|Employee email. Optional.|

4.  Upload the completed file.

5.  Navigate to **Software Spend Detection** &gt; **Administration** &gt; **Transaction Import Results** to view information about the import and resolve any import errors.

    When the import is complete, Software Spend Detection begins matching your transactions to software publishers and products. Software Spend Detection also assigns a **0 - 1** value to the **Is software probability**, **Product confidence**, and **Publisher confidence** fields for every transaction. For example, a value of **.85** for **Publisher confidence** means that Software Spend Detection is 85% sure that it matched the correct publisher to the transaction. When the matching process is complete, you can view the data in the Overview, Overlapping Software, and Software Spend Transactions modules under Software Spend Detection.


## What to do next

Navigate to **Software Spend Detection** &gt; **Unnormalized Transactions** to view any transactions that Software Spend Detection wasn't able to match with a software publisher and product. You can manually update these transactions to add a publisher and product. [Opt in to Content Service](opt-in-content-service.md) to improve matching for future imports.

If necessary, you can mass delete all transactions from an import. Navigate to **Software Spend Detection** &gt; **Administration** &gt; **Transaction Import Results**, select the import record, and then select **Delete**.

**Parent Topic:**[Software Spend Detection](../concept/software-spend-detection.md)

