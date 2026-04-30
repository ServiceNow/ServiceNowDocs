---
title: Create an ACL
description: Create an access control rule \(ACL\) to prevent the Needs review field from being modified after it has been set.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Tutorial: add a new change management state, Reference section for Change Management, Change Management, IT Service Management]
---

# Create an ACL

Create an access control rule \(ACL\) to prevent the **Needs review** field from being modified after it has been set.

## Before you begin

Role required: admin with elevated security

## About this task

The newly created UI Policy makes the **Needs review** field mandatory when a change request reaches the **Complete** state.

The subsequent configuration of the state model ensures that a value is required in the **Needs review** field before the change request can be saved in the **Complete** state. To prevent the **Needs review** value from being changed after it has been set, create a new access control level record \(ACL\) to make the field read-only.

## Procedure

1.  Open the **Change Request** form.

2.  Open the form context menu and select **Configure** &gt; **Security Rules**.

3.  Elevate your security role in the user menu that opens when you click your name in the header.

    Only administrators with elevated security roles can add ACLs.

4.  Click **New**.

5.  Enter the following values.

    |Field|Value|
    |-----|-----|
    |Type|Record|
    |Operation|Write|
    |Name \(first part\)|Change Request|
    |Name \(second part\)|Needs review|
    |Condition|\[State\] \[is\] \[Implement\]|

    ![New change request ACL](../image/NewStateTutNewACL1.png)

6.  Click **Submit**.


**Parent Topic:**[Tutorial: add a new change management state](t_AddNewStateTutorial.md)

**Previous topic:**[Add a UI policy](t_AddUIPolicy.md)

**Next topic:**[Update the state handler script include](t_UpdateStateHandlerScriptInclude.md)

