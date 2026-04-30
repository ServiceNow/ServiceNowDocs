---
title: Close an asset remediation task
description: View the open asset remediation from the Inventory view and close the task after updating the Model category and Model fields value for the asset.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-01-20"
reading_time_minutes: 1
keywords: [Open asset remediation tasks, close an asset remediation task, asset remediation tasks]
breadcrumb: [Audit hardware asset inventory, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Close an asset remediation task

View the open asset remediation from the **Inventory** view and close the task after updating the **Model category** and **Model** fields value for the asset.

## Before you begin

Role required: admin

## About this task

**Important:** This feature is available with Hardware Asset Management version 15.0.0 onwards.

A new asset record is created when all of the following are true:

-   The audit record's **Scan method** is set to **Multi scan**.
-   During asset scanning, a new asset is detected that doesn’t exist in the ServiceNow® instance,

For this new asset record, the application can’t automatically determine the **Model category** and **Model** field values. These fields are initially set to **Unknown Model Category** and **Unknown Model**. An asset remediation task is then generated to notify you that an asset record has been created with an unknown model category and an unknown product model. In the Hardware Asset Workspace, you can access the open remediation task, update the asset record as required, and then close the remediation task.

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Inventory view**.

2.  Select the **Overview** tab.

3.  In the Important Actions section, in the Open asset remediation tasks tile, select **View records**.

    The Open asset remediation tasks list is displayed.

4.  Select the task Number link.

    The Asset remediation form is displayed.

5.  In the **Asset** field, select the Open Record icon.

    The asset form is displayed. The default value for the **Model category** and **Model** field is displayed in read-only mode.

6.  Select the **Update** button.

7.  On the form, fill in the details.

    |Field|Description|
    |-----|-----------|
    |Asset type|Type of the asset.|
    |Model category|Model category that the asset can be associated with.|
    |Model|Model that the asset can be associated with.|

8.  Select **Update**.

    The updated Model category and Model value are displayed in the respective fields.

9.  Open the **Details** tab.

    The Asset remediation task form is displayed.

10. Select the **Close Task** button.

    The closed asset remediation task isn’t listed on the Open asset remediation tasks list.


**Parent Topic:**[Audit hardware asset inventory](../concept/ham-inventory-audit.md)

**Related topics**  


[Complete multi scan inventory audit using the ServiceNow Agent app](complete-multi-scan-inventory-audit-using-mobile-app.md)

