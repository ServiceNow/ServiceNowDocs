---
title: Add a product enhancement from an epic
description: Add a product enhancement from an epic to a product or service manually.
locale: en-US
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Define release scope, Use, Digital Product Release, IT Service Management]
---

# Add a product enhancement from an epic

Add a product enhancement from an epic to a product or service manually.

## Before you begin

Role required: sn\_dpr\_model.product\_manager

## About this task

Product enhancements can also be generated automatically from the main epics imported into the ServiceNow instance through the DevOps data model if the following settings have been completed:

-   The integration with the external planning tool is done.
-   The validates version option of the release is set to true.
-   A project from the Planning tool is linked with the product or service. For more information, see [View and manage data from external tools](dpr-manage-product-ext-tool.md).
-   The system property **sn\_dpr\_workspace.auto\_create\_product\_enhancement\_for\_primary\_epic** is set to **true**. For more information, see [Digital Product Release properties](../reference/digital-product-release-properties.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the products and services icon \(![Products and services icon.](../image/dpr-icon-products.png)\).

3.  Select a product or service from the list to open.

4.  Select the **Product enhancements** tab.

5.  Select the more actions icon next to the **Add enhancement** button and then select **Add enhancement from epic**.

    ![Add enhancement from epic button.](../image/dpr-icon-enhance-epic-btn.png)

    The Add enhancements from epics dialog box appears. It has a list of all top-level epics from the linked project that don’t have a product enhancement.

6.  On the Add enhancements from epics dialog box, select the epics from the list, and then select **Add enhancements**.

    The product enhancements are created for the selected epics and listed in the Product enhancements list.


**Related topics**  


[Add an enhancement to a product or service](dpr-create-product-enhancement.md)

[Add a product feature to a product or service](dpr-create-product-feature.md)

