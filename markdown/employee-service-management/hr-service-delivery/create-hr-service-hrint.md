---
title: Create an integration service in Enterprise Service Management Integrations Framework
description: Create an integration service to connect with the third-party system.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Enterprise Service Management Integrations Framework, Enterprise Service Management Integrations Framework, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Create an integration service in Enterprise Service Management Integrations Framework

Create an integration service to connect with the third-party system.

## Before you begin

Role required: sn\_hr\_integr\_fw.admin

## Procedure

1.  Navigate to **All** &gt; **Integrations Framework** &gt; **Source**.

2.  In Integration Services, click **New**.

3.  On the form, fill in the fields:

<table id="table_yqg_y3h_qmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Option to indicate that the integration service is available for use.

</td></tr><tr><td>

Import set tables

</td><td>

List of intermediate tables which store records from the third-party system.**Note:** This field is enabled only when Scheduled pull service is selected in the **Service type** field.

</td></tr><tr><td>

Flow

</td><td>

Flow that interacts with the third-party system to pull the required data.

</td></tr><tr><td>

Name

</td><td>

Display name of integration service.

</td></tr><tr><td>

Source

</td><td>

Name of the third-party system with which you want to integrate your application.

</td></tr><tr><td>

Application

</td><td>

Application which contains the integration service record.

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

Configuration set to push a record if the previous push fails.**Note:** This field appears only when Ondemand Push service is selected in the **Service type** field.

</td></tr></tbody>
</table>
