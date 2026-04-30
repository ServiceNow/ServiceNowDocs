---
title: Create a source for a learning system
description: Create a source record for the third-party learning system that you want to integrate with your ServiceNow instance.
locale: en-US
release: xanadu
product: Learning Core
classification: learning-core
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Administration tasks in Learning Core, Configuring Learning Core, Learning Core, HR Service Delivery, Employee Service Management]
---

# Create a source for a learning system

Create a source record for the third-party learning system that you want to integrate with your ServiceNow instance.

## Before you begin

-   Role required: learning\_admin
-   Learning Core integrates with Cornerstone OnDemand, Pluralsight, Udemy, Sumtotal , and Saba learning systems by default. Activate only the learning system that you to plan use. For more information, see [Integrating Learning Core with third-party learning management systems](setup-learning-third-party-1.md).

## Procedure

1.  Navigate to **Integrations Framework** &gt; **Source**.

2.  Click **New**.

3.  In the **Name** field, enter the name of the integration source, for example, Pluralsight.

4.  Right-click the form header and click **Save**.

5.  In the Integration Services related list, click **New**.

6.  On the form, fill in the fields:

<table id="table_kfz_z3j_ppb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the integration service, for example, Pluralsight.

</td></tr><tr><td>

Import set tables

</td><td>

List of intermediate tables which store records from the third-party system.**Note:** This field is enabled only when a scheduled pull service is selected in the **Service type** field.

</td></tr><tr><td>

Flow

</td><td>

Flow that interacts with the third-party system to pull the required data.

</td></tr><tr><td>

Active

</td><td>

Option to indicate that the integration service is available for use.

</td></tr><tr><td>

Application

</td><td>

Application which contains the integration service record.

</td></tr><tr><td>

Source

</td><td>

Name of the third-party system with which you want to integrate your application.

</td></tr><tr><td>

Order

</td><td>

Order in which you want to run transformation scripts.

</td></tr><tr><td>

Service type

</td><td>

Option to indicate the type of service **Scheduled pull** or **Ondemand Push**.

</td></tr><tr><td>

Retry policy

</td><td>

Configuration set to push a record when the previous push fails.**Note:** This field appears only when Ondemand Push service is selected in the **Service type** field.

</td></tr></tbody>
</table>7.  Click **Update**.


**Parent Topic:**[Administration tasks in Learning Core](ln-administration.md)

