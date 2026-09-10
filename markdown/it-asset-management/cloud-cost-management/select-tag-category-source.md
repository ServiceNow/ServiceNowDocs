---
title: Select a tag category source
description: Select a tag category source to control how the Cloud Cost Management application maps cloud resource tags to business entities for cost attribution and reporting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/select-tag-category-source.html
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-08-13"
reading_time_minutes: 2
breadcrumb: [Create and update a tag category, Use, Cloud Cost Management, IT Asset Management, Asset Management]
---

# Select a tag category source

Select a tag category source to control how the Cloud Cost Management application maps cloud resource tags to business entities for cost attribution and reporting.

## Before you begin

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\]

## About this task

The tag category source determines how spend tags are derived during billing downloads. Selecting the tag category source also determines how costs are grouped in analytics, forecasting, and recommendations.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Cost usage tags** &gt; **Tag category source**.

2.  In the **Tag source category** field, select the tag category source that matches your environment.

<table><thead><tr><th align="left" id="d190390e84">

Tag category source

</th><th align="left" id="d190390e87">

Description

</th></tr></thead><tbody><tr><td id="d190390e93">

**Cloud provider tags**

</td><td>

Uses native cloud provider resource tags that are defined and managed in the Cloud Cost Management application.

</td></tr><tr><td id="d190390e105">

**CMDB-driven cloud mapping**

</td><td>

Maps billing data to CMDB CI entities for cost attribution. You must take the following actions after you select **CMDB-driven cloud mapping**. -   **Select an entity**: Maps billing line items to an entity. Options include:
    -   **Application service**: Maps billing line items to application services using a tag name present on cloud resources.
    -   **Business application**: Maps billing line items to business applications. The table is auto-selected.
    -   **Custom table**: Select when your organization uses a child table of **Application service** with a custom column for tag values. You select the table and column manually.
-   **Select table**: The CMDB CI table that contains the entity values. These values are auto-selected for **Application service** and **Business application**. For **Custom table**, select the child table of **Application service** that your organization uses.
-   **Select column**: The column in the selected table whose values correspond to the tag values on billing line items.
-   **Select tags**: The tag name to look for in each billing line item. When this tag name is found, the Cloud Cost Management application looks up the matching entity in the selected table and column and associates it with the spend record.


</td></tr><tr><td id="d190390e174">

**ServiceNow-managed dimensions**

</td><td>

Uses ServiceNow-managed dimension tags for cost attribution. You must verify that CI-to-application service relationships are populated in your CMDB before you select this option.

</td></tr></tbody>
</table>    \[Omitted image "tag-category-source-cmdb.png"\] Alt text: Tag category source selection page in Cloud Cost Management Workspace

3.  Select **Save**.

    The Cloud Cost Management application saves the tag category source and triggers a billing data repopulation. All billing data is reprocessed to reflect the updated taxonomy.


**Parent Topic:**[Create and update a tag category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/tag-category-crud-cloudin.md)

**Related topics**  


[Cost usage tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/tags-overview.md)

[Create and update a tag category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/tag-category-crud-cloudin.md)

