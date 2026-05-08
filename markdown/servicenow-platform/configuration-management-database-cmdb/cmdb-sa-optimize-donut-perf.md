---
title: Configuring record count visibility in the CMDB success advisor dashboard to handle large datasets
description: Improve the performance of the CMDB success advisor dashboards for large datasets by hiding the record count on click-through from donut charts using a configurable system property.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuring record count visibility in the CMDB success advisor dashboard to handle large datasets

Improve the performance of the CMDB success advisor dashboards for large datasets by hiding the record count on click-through from donut charts using a configurable system property.

## Before you begin

Set the application scope to CMDB success advisor using the application picker. For more information, see Application picker.

Role required: admin

## About this task

Selecting a segment in a donut chart on a CMDB success advisor dashboard displays a list page with records that match the criteria of the selected segment. By default, this list shows a record count in the header and a total count in the pagination area. In environments with large datasets, retrieving these counts can increase load time. To improve page responsiveness, add the **hide\_list\_record\_count** system property and set its value to `true`. Enabling this property hides the record count in the list header and the total count in the pagination area, reducing the data load during navigation from donut charts without affecting the functionality of the charts or the list results.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  Select **New**.

3.  In the **Name** field, enter `hide_list_record_count`.

4.  From the Type list, select **true \| false**.

5.  In the **Choices** field, enter `true`.

6.  Select **Submit**.


