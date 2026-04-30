---
title: Create activity configuration details for the Journey Accelerator action plan items activity
description: Complete the configuration process for the Journey Accelerator activity that you created by specifying activity configuration details. The activity configuration details enable administrators to control the actions of links associated with applications and features.
locale: en-US
release: yokohama
product: Journey Accelerator
classification: journey-accelerator
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Add a Journey Accelerator action plan link to the My active items widget, Configure action plan access in the Employee Center, Install and configure Journey Accelerator, Journey Accelerator, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Create activity configuration details for the Journey Accelerator action plan items activity

Complete the configuration process for the Journey Accelerator activity that you created by specifying activity configuration details. The activity configuration details enable administrators to control the actions of links associated with applications and features.

## Before you begin

Ensure that the application scope is set to Employee Center. Use the application picker to change the application scope if it isn’t currently set to Employee Center. See [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information about using the application scope picker.

Role required: admin

## About this task

An activity configuration is associated with an application that you specify using the application picker. The fields that appear in an Activity Configuration or Activity Configuration Detail form depend on the application scope that you set using the application picker. See the following topics for more information about the forms associated with the Activity Configurations table:

-   [Activity Configuration form](../../employee-center/reference/ec-activity-configuration-form.md)
-   [Activity Configuration Detail form](../../employee-center/reference/activity-configuration-detail-form.md)

This task starts with the application scope set to the Employee Center application, and ends with creating conditional filters that are applied to the Journey Accelerator application.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Activity Configuration**.

    The Activity Configuration table appears.

2.  Select the activity configuration that you created for the Journey Accelerator action plan items.

    **Tip:** If you used the task described in the [Add a Journey Accelerator action plan link to the My active items widget](add-ja-action-plan-myitems-list.md) topic to create the activity configuration, select the Activity Configuration record with the **Activity Name** field set to **Action plan items**.

    The Activity Configuration form appears.

3.  Set the application scope to **Employee Center** using the application picker if the application scope is set to a different value.

    **Tip:** The application scope must be set to **Employee Center** to create the activity configuration details associated with the activity that you're configuring.

4.  From the **Related Links** section, select **New** on the **Activity Configuration Details** tab.

    The Activity Configuration Detail form appears.

5.  Change the application scope to **Journey Accelerator** using the application picker.

6.  In the **Table** field, select **Journey Accelerator Plan \[sn\_ja\_plan\]** from the drop-down list.

7.  Use the **Conditions** field to add filter conditions and or clauses that determine the employee's visibility into the action plans listed in the Journey Accelerator Plan table.

    These conditions control access to the links associated with the Journey Accelerator activity that you configured for the different employees across your organization.

    **Tip:** The following filter conditions and or clauses are examples that you can use or further modify to your specifications:

    |Conditions|Boolean Operator|
    |----------|----------------|
    |**Active**|**is**|**true**|**AND** **OR**|
    |**Manager**|**is \(dynamic\)**|**Me**|**AND** **OR**|
    |**Mentors**|**is \(dynamic\)**|**Me**|**AND** **OR**|

    |Conditions|Boolean Operator|
    |----------|----------------|
    |**Active**|**is**|**true**|**AND** **OR**|
    |**Employee**|**is \(dynamic\)**|**Me**|**AND** **OR**|
    |**State**|**is not**|**Draft**|**AND** **OR**|

8.  Select **Submit**.


