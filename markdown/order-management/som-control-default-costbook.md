---
title: Control the default cost book on transaction header or header line
description: Set the default cost book displayed to your sales agents on the transaction header or header line for a Sales Customer Relationship Management application by using the Cost Book Defaulting Matrix.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Control the default cost book on transaction header or header line

Set the default cost book displayed to your sales agents on the transaction header or header line for a Sales Customer Relationship Management application by using the Cost Book Defaulting Matrix.

## Before you begin

Role required: sn\_csm\_pricing.pricelist\_administrator, sn\_csm\_pricing.pricelist\_manager

## About this task

The transaction header is a record that contains general information about an entity, such as a cost book. A transaction line record contains specific information about a specific item, such as a cost book line for a certain product.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Pricing** &gt; **Pricing Matrices**.

3.  In the Pricing Matrices list, select **Cost Book Defaulting Matrix**.

4.  Select **Edit Rule**.

    The Decision Table for the Cost Book Defaulting Matrix opens in Workflow Studio and shows the inputs and the decision table for setting the conditions to display the default cost book in the header.

5.  In the decision table, set the rule for displaying the default cost book:

    1.  In the **Header Cost Book Type** column in the Results section, select the **Edit** icon to add the cost book that can be applied.

    2.  In the Condition section, select **Add new decision row**.

    3.  In the row, select the column for the input to be applied, such as **Currency** and set the condition to make it active.

    4.  In the Results section, select the **Header Price List Type** column and select the cost book to be applied, for example a specific currency-based cost book.

6.  Select **Save**.

    Review the **Validation Status** and **Validation Message** columns to see if you're missing mandatory inputs or outputs or required information. If so, enter the appropriate information and select **Save**.

    The default cost book is displayed in the transaction header or header line for the application.


