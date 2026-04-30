---
title: Specify rate discounts to enable accurate pricing for Rightsizing recommendations
description: To generate an accurate Rightsizing recommendation, the system analyzes usage data for the last 14 days, obtains prices from the price sheet data tables, and then applies appropriate discounts. To enable the calculations, specify the provider's discount rate for each service account.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Rightsizing operations, Resize resources with Rightsizing, Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Specify rate discounts to enable accurate pricing for Rightsizing recommendations

To generate an accurate Rightsizing recommendation, the system analyzes usage data for the last 14 days, obtains prices from the price sheet data tables, and then applies appropriate discounts. To enable the calculations, specify the provider's discount rate for each service account.

## Before you begin

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\]

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

**Parent Topic:**[Configure Rightsizing operations](rs-settings-config-cloudin.md)

**Related topics**  


[Schedule and manage the Cloud Cost Management jobs that download AWS price sheets](aws-pricesht-sched-dwnld-cloudin.md)

