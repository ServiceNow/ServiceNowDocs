---
title: Update the Employee Center theme
description: Install the Employee Center app from the ServiceNow Store to update the EC UI theme.
locale: en-US
release: zurich
product: Journey Accelerator
classification: journey-accelerator
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure action plan access in the Employee Center, Configure, Journey Accelerator, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Update the Employee Center theme

Install the Employee Center app from the ServiceNow Store to update the EC UI theme.

## Before you begin

Install the Employee Center app from the ServiceNow Store before you can update the labels for the menu items or My active items links. For more information, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

For more information on Employee Center themes, see [Customize Employee Center portal theme](../../employee-center/task/customize-theme.md).

Role required: admin

## About this task

Update the Employee Center service portal setting to use the latest Employee Center user interface.

**Note:** The Employee Center in your instance might already use the updated field settings.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**, and click **Employee Center**.

2.  Open the record for **Employee Center Menu**.

    Set these fields and values:

    |Field|Value|
    |:----|:----|
    |Homepage|`ec_dashboard`|
    |Theme|`EC Theme`|
    |Main menu|Employee Center Menu|

3.  Click **Update**.


## What to do next

You can update Employee Center menu items and links in My Active Items.

-   [Add a Journey Accelerator action plan to My active items](add-ja-action-plan-myitems-list.md)
-   [Add a Journey Accelerator action plan to the menu in the Employee Center](add-ja-action-plan-menu-ec-header.md)

