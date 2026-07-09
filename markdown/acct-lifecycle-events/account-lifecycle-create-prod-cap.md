---
title: Create a product capability record
description: Create a product capability record and associate it with one or more capability usage records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-create-prod-cap.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Product capabilities, Customer success, Configure, Customer Success Management]
---

# Create a product capability record

Create a product capability record and associate it with one or more capability usage records.

## About this task

A product capability is the higher-level ability of a product to solve a problem or deliver value. Monitor the adoption and usage of specific product capabilities to understand how effectively those capabilities are being used.

## Before you begin

-   Role required: sn\_acct\_lc.customer\_success\_application\_admin
-   Product and capability usage records must already be present. See [Product and capability usage records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-prod-usage-data-model.md).

## Procedure

1.  Navigate to **All** &gt; **Capabilities &amp; Usage** &gt; **Capabilities** and select **New**.

2.  On the form, complete these fields.

<table id="table_egk_ysm_yfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for this capability.

</td></tr><tr><td>

Description

</td><td>

Description of this capability.

</td></tr><tr><td>

Type

</td><td>

Type of capability. Options:-   Feature
-   Capability
-   Technical Service
Select **Capability** from the list.

</td></tr><tr><td>

Category

</td><td>

Category or area to which the capability belongs.

</td></tr></tbody>
</table>3.  Navigate to the Product Capability Maps related list.

4.  Select **New** to associate this capability with a product model.

5.  On the form, complete these fields.

<table id="table_hpm_pvm_yfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

State

</td><td>

State of the map.-   Draft
-   Published
-   Archived
-   Canceled


</td></tr><tr><td>

Product model

</td><td>

Product to associate with this capability.

</td></tr><tr><td>

Product capability

</td><td>

The capability for which the product is being associated.

</td></tr><tr><td>

Active

</td><td>

Automatically set to **True** when the product capability map is published.

</td></tr><tr><td>

Release date

</td><td>

The release date for this capability.

</td></tr><tr><td>

Availability date

</td><td>

The availability date for this capability.

</td></tr></tbody>
</table>6.  In the **State** field, set the state to **Published**.

7.  Select **Submit**.

    You can view the product and capability usage scores in the Engagement home page. See [View product usage and capability data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-prod-cap-usage.md)


-   **[Product and capability usage records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-prod-usage-data-model.md)**  
The product and capability usage records are automatically created and updated when changes occur in sold product configurations, capability mappings, or in the data context engine.

**Parent Topic:**[Configure product capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-setup-prod-cap.md)

