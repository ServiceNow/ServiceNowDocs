---
title: Create a product capability record
description: Create a product capability record and associate with one or more capability usage records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/customer-success-management/account-lifecycle-create-prod-cap.html
release: australia
product: Customer Success Management
classification: customer-success-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Product capabilities, Customer success, Configure, Customer Success Management]
---

# Create a product capability record

Create a product capability record and associate with one or more capability usage records.

## About this task

A product capability is the higher-level ability of a product to solve a problem or deliver value. You can monitor the adoption and usage of specific product capabilities and gain insights into how effectively those capabilities are being used.

## Before you begin

-   Role required: sn\_acct\_lc.customer\_success\_application\_admin
-   Product and capability usage records must already be present. See [Product and capability usage records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-prod-usage-data-model.md).

## Procedure

1.  Navigate to **All** &gt; **Capabilities &amp; Usage** &gt; **Capabilities** and select **New**.

2.  In the form, fill in these fields:

<table id="table_egk_ysm_yfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for this capability.

</td></tr><tr><td>

Description

</td><td>

Enter a description for this capability.

</td></tr><tr><td>

Type

</td><td>

The options are:-   Feature
-   Capability
-   Technical Service
Select **Capability** from the list.

</td></tr><tr><td>

Category

</td><td>

Select the category or area to which the capability belongs.

</td></tr></tbody>
</table>3.  Navigate to the **Product Capability Maps** related list.

4.  Select **New** to associate it this capability with a product model.

5.  In the form, fill in these fields.

<table id="table_hpm_pvm_yfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

State

</td><td>

The state of the map.-   Draft
-   Published
-   Archived
-   Canceled


</td></tr><tr><td>

Product model

</td><td>

Select the product with which the capability is to be associated.

</td></tr><tr><td>

Product capability

</td><td>

The capability for which the product is being associated.

</td></tr><tr><td>

Active

</td><td>

This flag is set to **True** when the product capability map is published.

</td></tr><tr><td>

Release date

</td><td>

The release date for this capability.

</td></tr><tr><td>

Availability date

</td><td>

The availability date for this capability.

</td></tr></tbody>
</table>6.  In the **State** field, set the status to **Publish**.

7.  Select **Submit**.

    You can view the product and capability usage scores in the Engagement home page. See [View product usage and capability data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-prod-cap-usage.md)


-   **[Product and capability usage records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-prod-usage-data-model.md)**  
The product and capability usage records are automatically created and updated when changes occur in sold product configurations, capability mappings, or in the data context engine.

**Parent Topic:**[Configure product capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-setup-prod-cap.md)

