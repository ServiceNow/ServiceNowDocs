---
title: Create a matrix version
description: Create a version of a published price or product eligibility matrix when you need to update the matrix, for example to add or delete a context variable used in the price matrix.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring product pricing, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Create a matrix version

Create a version of a published price or product eligibility matrix when you need to update the matrix, for example to add or delete a context variable used in the price matrix.

## Before you begin

Role required: sn\_csm\_pricing\_pricelist\_administrator, sn\_csm\_pricing\_pricelist\_manager

## About this task

You can create a version of a published pricing matrix \(Standard Price Adjustment Matrix, Price List Defaulting Matrix, Cost Book Defaulting Matrix, or Configuration Component Price Adjustment Matrix\) and a product eligibility matrix. When you create a matrix version, the new version becomes the active version. After creating the version, you update the decision table for the matrix, then save and publish the matrix.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../image/Lists.png) view.

2.  Navigate to **Pricing** &gt; **Pricing Matrices**.

3.  In the Pricing Matrices list, select the matrix to be updated.

4.  In the Details tab for the matrix, select **Create new version**.

    The following changes occur:

    -   The new version of the matrix opens in another tab.
    -   In the former matrix, the **State** changes from Published to Retired and the System **System defined** value changes to false.
5.  Change the matrix as needed.

    For example, if you're updating context variables used in the Standard Price Adjustment Matrix, you can add or delete context variables in the **Context variables** section of the matrix.

6.  Select **Save**.

7.  Update the decision table for the matrix by selecting **Create rule**.

    Add the decision rows in the decision table for the matrix. You can use the decision table export feature to edit the decision table for the previous matrix version in Excel, update the Excel file, then import the updated Excel table to populate the decision table for the new version. For details, see [Manage decision tables in Excel.](https://www.servicenow.com/docs/access?context=manage-decision-tables-ms-excel&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)

8.  Select **Save** and then **Publish**.

    You can refresh the list of matrices to see the new matrix version.


