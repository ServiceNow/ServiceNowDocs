---
title: Configure daily stats
description: Configure daily stats records that you want to display on the Manager Hub. Daily stats can be information related to employee PTO, employee location, and so on.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/configure-daily-stats.html
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Manager Hub, HR Service Delivery, Employee Service Management]
---

# Configure daily stats

Configure daily stats records that you want to display on the Manager Hub. Daily stats can be information related to employee PTO, employee location, and so on.

## Before you begin

Role required: sn\_mh.admin

## Procedure

1.  Navigate to **All** &gt; **Manager Hub** &gt; **Administration** &gt; **Team Daily Stats**.

2.  Click **New**.

3.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Name|Name of the daily stat configuration record.|
    |Display label|Display name of the daily stat record in the Manager Hub and Team members tabs in Your team menu.|
    |Active|Option to activate or deactivate the daily stat configuration record.|
    |Order|Order in which you want the daily stat record to appear in the Manager Hub and Team members tabs in Your team menu. The daily stat configuration record with the lowest order number appears first, and the daily stat configuration record with the highest order number appears last on the user interface.|

4.  Click **Submit**.


## What to do next

1.  In the **Filter sources** related list, click **New**.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Filter source|Filter configuration record that you want to associate the daily stat filter with.|
    |Active|Option to activate or deactivate a filter group record.|
    |All|Option to select all the filter values in the source at one time. For example, City is filter source. It contains cities such as Chicago, Hyderabad, Madison, and New York. If you want to select all the cities at time, select **All**. If you want to select only few cities, select **Options**.|
    |Options|Option to select only specific filters values in the source.|

3.  Click **Submit**.

**Parent Topic:**[Configure Manager Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/set-up-managerhub.md)

**Related topics**  


[RCA approvals for Manager Hub]()

[Activate a scheduled job]()

[Configure important dates]()

[Configure team requests]()

[Configure team data]()

[Configure team column data]()

[Configure team filters]()

[Set up View as Direct Reports]()

[Configure to do mappings]()

[Configure widgets]()

