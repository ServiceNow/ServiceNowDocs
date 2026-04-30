---
title: Create the criteria for a service organization
description: Define the criteria in the service organization criteria \[service\_organization\_criteria\] table so that you can later associate your service organizations to a service or your customers to a service organization. You do this task in the Customer Service Management \(CSM\) application.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Create the criteria for a service organization

Define the criteria in the service organization criteria \[service\_organization\_criteria\] table so that you can later associate your service organizations to a service or your customers to a service organization. You do this task in the Customer Service Management \(CSM\) application.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Service Organizations** &gt; **Administration** &gt; **Service Organization Criteria**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_o4r_swk_byb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

String

</td><td>

Name of the criteria.

</td></tr><tr><td>

Table

</td><td>

Table Name

</td><td>

Table where you must define the criteria.

 To establish customer associations, you must select **Account**, **Consumer**, or **Household** from the drop-down list in the **Table** field. Similarly, for associating products and services, you must choose **Internal Business Location** from the drop-down list in the **Table** field.

 Selecting **Business Location** or **Service Organization** from the drop-down list in the **Table** field leads to an error because the system currently doesn’t support fulfillment capabilities for external business locations when resolving a case.

**Note:** Support can be extended to other tables by configuring them in the `SOCriteriaTableScript` script include.

</td></tr><tr><td>

Criteria

</td><td>

Conditions

</td><td>

Condition or query filter that matches a list of records in the table.

</td></tr></tbody>
</table>4.  Select **Submit**.


