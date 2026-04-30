---
title: Control the default price list on transaction header or header line
description: Define the default price list displayed to your sales and order agents on the transaction header or header line by using the Price List Defaulting Matrix.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Pricing Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Control the default price list on transaction header or header line

Define the default price list displayed to your sales and order agents on the transaction header or header line by using the Price List Defaulting Matrix.

## Before you begin

Role required: sn\_csm\_pricing\_pricelist\_administrator, sn\_csm\_pricing\_pricelist\_manager

## About this task

For base systems, the default price list used is based on the transaction header. For example, if a sales agreement is populated on the transaction header, the sales agreement price list is used as the default. If a customer account is populated on a transaction header and a valid account-based price list exists, the header defaults to the account-based price list. If no account-based price list exists, the default currency-based price list is used.

You can change the default price list selection logic by using the Price List Defaulting Matrix.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![image.Lists] view.

2.  Navigate to **Pricing** &gt; **Pricing Matrices**.

3.  In the Pricing Matrices list, select Price List Defaulting Matrix.

4.  Select **Edit Rule**.

    The Decision Table for the Price List Defaulting Matrix opens in Workflow Studio and shows the inputs and the decision table for setting the conditions to display the default price list in the header.

5.  In the decision table, set the rule for displaying the default price list:

    1.  In the **Header Price List Type** column in the Results section, select the **Edit** icon to add the price lists that can be applied, for example an account-based price list or a currency-based price list.

    2.  In the Condition section, select **Add new decision row**.

    3.  In the row, select the column for the input to be applied, such as **Account** and select the condition to make it active.

    4.  In the Results section, select the **Header Price List Type** column and select the price list to be applied, for example an account-based price list or a currency-based price list.

6.  Select **Save**.

    Review the **Validation Status** and **Validation Message** columns to see if you're missing mandatory inputs or outputs or required information. If so, enter the appropriate information and select **Save**.

    The default price list is available to sales or order agents when working on the transaction header for opportunities, quotes, or orders or when working on the transaction line, for example a quote line or order line.


