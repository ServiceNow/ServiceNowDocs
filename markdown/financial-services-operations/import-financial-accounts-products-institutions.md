---
title: Import your financial data using import sets
description: Import your financial accounts, financial products, financial institutions, and financial transactions into ServiceNow Financial Services Operations Core tables. You need this foundation data to make the Financial Services Operations applications work.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Financial Services Operations \(FSO\)]
---

# Import your financial data using import sets

Import your financial accounts, financial products, financial institutions, and financial transactions into ServiceNow Financial Services Operations Core tables. You need this foundation data to make the Financial Services Operations applications work.

## Before you begin

Ensure that the application scope is set to the Financial Services Operations Core. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).

Role required: sn\_bom.admin

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Load Data**.

2.  Select **Create table** and enter a label for the new table in the **Label** field.

3.  In the **Source of the import** field, select a source so that you can upload data from an external data source into an import set.

4.  Click **Submit**.

    The imported data is now available in the new Import Set table.

    For more information, see [Import sets key concepts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/c_ImportSetsKeyConcepts.md).

5.  [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_CreateATransformMap.md) to define the field mapping between columns of the import set and columns of the target table.

    For information on target tables, see the table topics in [Financial Services Operations Core](../reference/financial-services-operations-core-data-model.md).

6.  Transform the data from the import set table to the target table.

    For more information, see [Run an import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_RunImport.md).

7.  Verify that the data records are imported into the target tables by navigating to the target tables.

    -   For financial accounts, navigate to **Financial Services Operations** &gt; **Financial Accounts** and click the account to which you imported the financial accounts. For example, to view imported records for checking accounts, click **Checking Accounts**.
    -   For financial transactions, navigate to **Financial Services Operations** &gt; **Financial Accounts** and perform the following steps:
        1.  Click the account for which you imported the financial transactions, for example, **Checking Account**.
        2.  Open an account from the list and click the Transactions related list.
    -   For financial products, navigate to **Financial Services Operations** &gt; **Financial Products** and click the product to which you imported the financial products. For example, to view imported records for deposit model, click **Deposit Model**.
    -   For financial institutions, navigate to **Financial Services Operations** &gt; **Financial Institutions**.

