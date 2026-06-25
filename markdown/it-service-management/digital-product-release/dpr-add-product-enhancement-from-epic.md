---
title: Add a product enhancement from a work item
description: Add a product enhancement from a work item to a product or service manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-product-release/dpr-add-product-enhancement-from-epic.html
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Define release scope, Use, Digital Product Release, IT Service Management]
---

# Add a product enhancementfrom a work item

Add a product enhancement from a work item to a product or service manually.

## Before you begin

Role required: sn\_dpr\_model.product\_manager

## About this task

Product enhancements can also be generated automatically from the main epics imported into the ServiceNow instance through the DevOps data model if the following settings have been completed:

-   The system property **sn\_dpr\_workspace.enhancement\_work\_item\_types** lists the DevOps work item types that can be mapped. By default only epics can be mapped; add other types such as feature or story as needed. For more information, see [Digital Product Release properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/digital-product-release-properties.md).
-   The integration with the external planning tool is done.
-   The validates version option of the release is set to true.
-   A project from the Planning tool is linked with the product or service. For more information, see [View and manage data from external tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-manage-product-ext-tool.md).
-   The system property **sn\_dpr\_workspace.auto\_create\_product\_enhancement\_for\_primary\_epic** is set to **true**. For more information, see [Digital Product Release properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/digital-product-release-properties.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the products and services icon \(\[Omitted image "dpr-icon-products.png"\] Alt text: Products and services icon.\).

3.  Select a product or service from the list to open.

4.  Select the **Product enhancements** tab.

5.  Select the more actions icon next to the **Add enhancement** button and then select **Add enhancement from work item**.

    \[Omitted image "dpr-icon-enhance-epic-btn.png"\] Alt text: Add enhancement from work item button.

    The Add enhancements from work items dialog box appears. It lists every work item from the linked project whose type matches the **sn\_dpr\_workspace.enhancement\_work\_item\_types** system property and that does not already have a product enhancement.

6.  Select the work items from the list, and then select **Add enhancements**.

    The product enhancements are created for the selected work items and listed in the Product enhancements list.


**Related topics**  


[Add an enhancement to a product or service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-create-product-enhancement.md)

[Add a product feature to a product or service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-create-product-feature.md)

