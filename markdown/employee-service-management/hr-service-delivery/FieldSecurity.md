---
title: Add field security in HR
description: You can secure a field on a form so that specific HR users cannot view it.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use HR Profile, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Add field security in HR

You can secure a field on a form so that specific HR users cannot view it.

## Before you begin

Role required: sn\_hr\_core.admin, security\_admin

## About this task

Use **Access Control** \(ACL\) on a field to secure it.

**Note:** This example shows how to secure the **Ethnicity** field on an **HR Profile** form so users with the HR Manager \[hr\_manager\] role or below cannot view it.

## Procedure

1.  Navigate to **All** &gt; **HR Profile**.

2.  Elevate your role to add **security\_admin**.

    Select your login name and select **Elevate Roles**.![Select Elevate Roles from login name.](../image/ElevateRoles.png)

3.  Check **security\_admin**.

4.  Select **OK**.

5.  Select an HR profile record to edit.

    It can be any record.

6.  Right-click the **Ethnicity** field and select **Configure Security**.

    ![Reveal the Configure Security field from the HR profile form.](../image/HRProfile.png)

7.  The **Security Mechanic** menu appears.

    Change the **Operation to secure** field to **read**. ![Operation Secure field on Security Mechanic menu.](../image/SecurityMechanic.png)

8.  Move a role that you want to view the field to the **Selected** column.

    For example, move **sn\_hr\_core.admin**. By selecting **read** and adding **sn\_hr\_core.admin**, any role below this role, cannot read the field. For example, **sn\_hr\_core.manager** is below this role and cannot view this field after completing the steps.

9.  Click **OK**.

    Because HRSM is a scoped application, you have to ensure that you are in the scoped version within the form.

    -   Click the Settings ![Gear icon](../../../common/image/Banner_GearIcon.png) icon.
    -   Select **Developer** under **System Settings**.
    -   Change **Application** to **Human Resources: Core**.![Change to scoped version of HR through System Settings.](../image/ChangeScope.png)
    -   Close the window.

**Parent Topic:**[Use HR Profile](../concept/c_HRProfileRecords.md)

**Related topics**  


[Access control list rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

