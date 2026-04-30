---
title: Add a Journey Accelerator action plan link to the My active items widget
description: Add a menu item for Journey Accelerator action plans to the My active items widget in the Employee Center.
locale: en-US
release: yokohama
product: Journey Accelerator
classification: journey-accelerator
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure action plan access in the Employee Center, Install and configure Journey Accelerator, Journey Accelerator, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Add a Journey Accelerator action plan link to the My active items widget

Add a menu item for Journey Accelerator action plans to the My active items widget in the Employee Center.

## Before you begin

The latest Employee Center app installed on your instance. See, [Install Employee Center](../../employee-center/task/activate-ec.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Activity Configuration**.

    The Activity Configurations table appears.

2.  Select **New** to create an activity configuration.

    The Activity Configuration form appears.

3.  Use the application picker to set the application scope to **Employee Center**.

    See [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information about using the application scope picker.

    The **Application** field is set to **Employee Center**.

4.  In the **Activity Name** field, type `Action plan items`.

5.  In the **Activity portal page** field, select **ja\_plans**.

6.  Accept the default values for the following fields:

    1.  **Activity navigation** field is set to **Internal**.

    2.  **Order** field is set to **100**.

    3.  **Primary** check box is cleared.

    4.  **Advanced** check box is cleared.

    5.  **Active** check box is selected.

7.  Select **Submit**.


## What to do next

Complete the configuration process for the activity configuration you created by specifying configuration details. See [Create activity configuration details for the Journey Accelerator action plan items activity](create-ja-activity-config.md).

