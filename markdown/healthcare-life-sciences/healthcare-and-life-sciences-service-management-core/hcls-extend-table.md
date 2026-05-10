---
title: Extend the healthcare case table
description: Extend the Healthcare case \[sn\_hcls\_case\] table to create a case type for viewing patient information within healthcare-related cases.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Display patient information on a healthcare case, Set up your Healthcare Workspace, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Extend the healthcare case table

Extend the Healthcare case \[sn\_hcls\_case\] table to create a case type for viewing patient information within healthcare-related cases.

## Before you begin

Set the application scope to Healthcare and Life Sciences using the application picker. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).

Role required: sn\_hcls.admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  In the Tables list, click **New**.

3.  Fill in the details of the new table record.

4.  In the **Extends Table** field, click the lookup icon ![Lookup using list icon.](../image/lookup-using-list.png) and search for and select the sn\_hcls\_case table.

5.  Click **Submit**.

6.  In the table record, navigate to the controls tab and set the Auto-number field to **True**.

7.  Under the Application Access tab, set the following fields:

    -   Can read - True
    -   Can create - True
    -   Can update - True
    -   Can delete - True
    -   Allow Configuration - True
8.  Click **Save.**


