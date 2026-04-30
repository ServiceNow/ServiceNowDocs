---
title: Set default values for a cloud catalog form fields
description: You can set default values for all users or you can populate fields with default values based on conditions. This example shows you how to set a default schedule profile and business service.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Cloud catalog form configuration examples, Form configuration with blueprints, Cloud Provisioning Blueprints, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Set default values for a cloud catalog form fields

You can set default values for all users or you can populate fields with default values based on conditions. This example shows you how to set a default schedule profile and business service.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

Before you can follow this example, you should be familiar with creating blueprints and blueprint rules. See these resources:

-   [Cloud Provisioning Blueprints](../concept/blueprints.md)
-   [Build a Cloud Provisioning blueprint](create-blueprint-cmp.md)
-   [Configure a blueprint rule](configure-a-blueprint-rule.md#)

## About this task

The goal of this example is to display a default value for both the schedule profile and the business service field. Each field derives its values differently:

-   The schedule profile derives its values from a pool filter that returns a text value. Therefore, you must set the default value by applying the correct, matching text for one of the schedule profile options that appear to the user in a list.
-   The business service derives its values from a reference to the Service \[cmdb\_ci\_service\] table. Therefore, you must set the value by specifying the Sys ID of the record that you want to display.

The example in this topic sets the values in different ways:

-   The schedule profile default value is set directly on the Schedule Profile property and applies to all users without any conditions. You might want to do this to limit the use of virtual resources to specific schedule, such as during business hours only, for all users.
-   The business service default value is set using an action on a blueprint rule. You might want to use a rule to set a default value when you want the value to be the default only when certain conditions are met. For example, if the user belongs to a user group that deals with only one business service, set the value for the user so they do not have to sort through a long list of all the business services in your organization.

## Procedure

1.  Create a blueprint with a virtual server.

    For this example, a blueprint with a virtual server on an AWS datacenter is used.

    ![Virtual server on AWS](../image/blueprint-virtual-server-aws.png)

2.  On the blueprint form, click the **Catalog** tab, and then click the tile that represents the **Provision** operation.

    ![Catalog item](../image/request-operation-catalog-item.png)

3.  Click the **General Info** variable set in the Variable Sets related list.

4.  Click the **ScheduleProfile** variable.

    Notice that the **Pool** field on the **Type Specifications** tab specifies the pool from which the values for the schedule profile are derived: ScheduleProfilePool.

    The **ScheduleProfilePool** pool specifies the **All** filter, which returns the values in the Name field from the Schedule Profile \[sn\_cmp\_schedule\_profile\] table. These values are static text values, which means that you can specify the exact text value for the name of the schedule profile that you want to make the default. ![The ScheduleProfile pool](../image/schedule-profile-pool.png)

5.  On the **Default Value** tab of the ScheduleProfile property form, enter the text that matches the value in the Name field from the Schedule Profile \[sn\_cmp\_schedule\_profile\] table.

    In this example, that value is `8-5 weekdays`.

    ![8-5 Weekdays](../image/schedule-profile-default-value.png)

6.  Click **Update**.

7.  Click the **BusinessService** variable.

    Notice that the **Reference** field on the **Type Specifications** tab specifies the Service \[cmdb\_ci\_service\] table, from which the values for the business service are derived.

    ![The Business Service property](../image/business-service-property.png)

    By default, to refer to a specific record in a table, you must know the Sys ID of the record.

8.  To obtain the Sys ID of a business service:

    1.  In the main interface for the instance \(not the Cloud Admin Portal interface\), enter `cmdb_ci_service.list` in the application filter.

    2.  Find the business service that you want to make the default.

    3.  Right-click the record, and then select **Copy sys\_id**.

        This example uses **Workday Enterprise Services**.

        ![Copy the Sys ID](../image/copy-workday-sys-id.png)

9.  On the **BusinessService** variable form, create a rule, action, and condition with these values:

    1.  In the **Rule** related list, click **New**.

    2.  Provide a name and a description.

    3.  Right-click the form header and select **Save**.

    4.  In the **Action** related list for the rule, click **New**.

    5.  Provide a name, and then configure these fields as specified:

<table id="table_q1n_2xd_t2b"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Action Type

</td><td>

**SetValue**

 This option tells the system to change the field to the value you specify. Selecting this option is the same as entering a default value on the property form.

</td></tr><tr><td>

Target Field

</td><td>

**BusinessService**

</td></tr><tr><td>

Value

</td><td>

The Sys ID of the business service that you copied.

</td></tr></tbody>
</table>        In this example, the business service is set to Workday Enterprise Services by default, which is represented in the system with the Sys ID that you already copied.

        ![Business Service Rule with default value](../image/bp-set-business-service-action.png)

    6.  Click **Submit**.


## Result

![Default values for schedule profile and business service](../image/cloud-management-v2-admin.png)

## What to do next

You can create a condition or multiple conditions that must be met before the system sets the default value for the business service. For example, you might want to change the default value of business service to Workday Enterprise Services only when the group that the user belongs to is the Workday Admins group.

**Parent Topic:**[Cloud catalog form configuration examples](../concept/example-blueprint-rules.md)

