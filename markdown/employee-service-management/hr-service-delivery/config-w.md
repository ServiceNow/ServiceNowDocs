---
title: Configure Workday to-dos
description: Store one-time configuration parameters to pull tasks from Workday into the ServiceNow application.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring HR Service Delivery Integration with Workday, HR Service Delivery Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure Workday to-dos

Store one-time configuration parameters to pull tasks from Workday into the ServiceNow application.

## Before you begin

Role required: sn\_hr\_workday.admin

## Procedure

1.  Navigate to **All** &gt; **Workday Pull To-dos** &gt; **Configuration Pull To-dos**.

    For information on the Pull to-dos report creation, see this [KB article](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=749a27891bed81501e579979b04bcb41).

2.  On the form, fill in the fields:

<table id="table_a21_xq5_lnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workday to dos RAAS report name

</td><td>

Name of the report that is pulled from Workday.**Note:** Make sure you provide the exact name of the report for proper synchronization.

</td></tr><tr><td>

Workday to dos report owner username

</td><td>

Owner of the report.**Note:** Make sure you provide the exact name of the owner for proper synchronization.

</td></tr><tr><td>

Initial load start date time

</td><td>

Date and time from which you want to pull todos from Workday into ServiceNow.

</td></tr><tr><td>

Load Interval

</td><td>

Interval in which you want to pull data, for example, in terms of days or months or hours.Example: For initial load, if you want to pull data from the last six months, then you can set the load interval as 15 days. Data is pulled from the last six months \(in a set of 15 days\) till the starting time captured in the **Job Started at** field in Job tracker. In case the data is large, an outbound call timeout error is displayed in ServiceNow. You must then decrease the load interval.

 If a schedule flow is run for every 12 hours, then data is always pulled till current time.

</td></tr></tbody>
</table>
