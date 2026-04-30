---
title: Create and manage sold products for a business location
description: Staff members with the location agent role can manage sold products for their business locations.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Model Foundation business locations, Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Create and manage sold products for a business location

Staff members with the location agent role can manage sold products for their business locations.

## Before you begin

Role required: sn\_customerservice\_manager, sn\_customerservice.svc\_location\_agent, or admin

## About this task

Staff members with the sn\_customerservice\_manager role can create sold products by choosing the appropriate product model. In contrast, staff members with the sn\_customerservice.svc\_location\_agent role can only view the list of sold products installed at any service organization.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Service Organizations** &gt; **Internal/External Business Locations**.

2.  Select either an internal or an external business location.

3.  In the Sold Products related lists, click **New**.

4.  On the form, fill in the fields.

<table id="table_hc5_l4g_c5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the sold product.

</td></tr><tr><td>

Product

</td><td>

Product model sold to the customer.

</td></tr><tr><td>

Parent Sold Product

</td><td>

If the sold product contains child components, reference to another sold product.

</td></tr><tr><td>

Service Organization

</td><td>

Internal or external entity that is involved in providing service to the customer.**Note:** The sold products are closely tied to the service organization. As an example, if you select a service organization, all the parent sold products come from the same service organization.

</td></tr></tbody>
</table>5.  Click **Submit**.

    A sold product record is created for the selected business location.


**Related topics**  


[Create a sold product](create-sold-item.md)

