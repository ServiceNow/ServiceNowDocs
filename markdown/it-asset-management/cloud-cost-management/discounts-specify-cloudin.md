---
title: Specify rate discounts to enable accurate pricing for Rightsizing recommendations
description: Specify the provider's discount rate for each service account to enable Rightsizing calculations. To generate accurate recommendations, the system analyzes 14 days of usage data, applies price sheet rates, and appropriate discounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/discounts-specify-cloudin.html
release: brazil
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure Rightsizing operations, Resize resources with Rightsizing, Use, Cloud Cost Management, IT Asset Management, Asset Management]
---

# Specify rate discounts to enable accurate pricing for Rightsizing recommendations

Specify the provider's discount rate for each service account to enable Rightsizing calculations. To generate accurate recommendations, the system analyzes 14 days of usage data, applies price sheet rates, and appropriate discounts.

## Before you begin

Role required: Insights admin \(sn\_clin\_core.insights\_admin\)

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **AWS price discounts**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_uwf_2wm_1jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service account

</td><td>

The service account that the specified discount applies to.

</td></tr><tr><td>

Discount \(%\)

</td><td>

The percentage discount for the selected service account.

</td></tr></tbody>
</table>4.  Select **Save**.


## What to do next

View the provider's discount rate for each service account by navigating to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **AWS price discounts**.

**Parent Topic:**[Configure Rightsizing operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/cloud-cost-management/rs-settings-config-cloudin.md)

**Related topics**  


[Schedule and manage the Cloud Cost Management jobs that download AWS price sheets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/cloud-cost-management/aws-pricesht-sched-dwnld-cloudin.md)

