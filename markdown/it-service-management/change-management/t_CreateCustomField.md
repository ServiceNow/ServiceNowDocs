---
title: Create a custom field
description: Create a custom choice field to indicate whether a change request must go through the Review state.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Tutorial: add a new change management state, Reference section for Change Management, Change Management, IT Service Management]
---

# Create a custom field

Create a custom choice field to indicate whether a change request must go through the **Review** state.

## Before you begin

Role required: admin

## Procedure

1.  Open the **Change Request** form.

2.  Complete the following steps to create a new field on the Change Request form.

    1.  Open the form context menu and select **Configure** &gt; **Form Layout**.

    2.  Enter the following values in the **Create new field** section.

        |Field|Value|
        |-----|-----|
        |Name|Needs Review|
        |Type|Choice|

    3.  Click **Add** to add the new field to the slushbucket.

        The new field appears at the bottom of the **Selected** slushbucket.

    1.  Use the up and down arrows next to the slushbucket to move the new field next to the **Assigned to** field.

        ![Needs Review field placement](../image/NewStateTutCustFld2.png)

    2.  Click **Save**.

        The Change Request form reopens with the **Needs review** field below the **Assigned to** field.

3.  Complete the following steps to configure the choices for the **Needs review** field.

    1.  Right-click the **Needs review** field label and select **Configure choices**.

    2.  In the **Enter new item** field, add **Yes** and **No** choices and click **Add**.

        The choices appear in the **Selected** list.

    3.  Click **Save**.

    The Change Request form reopens. The **Needs review** choice list contains the**Yes** and **No** choices.

4.  If the value in the **Needs review** field is **Yes**, **No**, or blank, configure the default by completing the following steps.

    1.  Right-click the **Needs review** field label and select **Configure Dictionary**.

    2.  In the **Choice List Specification** section, select **Dropdown with – None –**as the default **Choice**.

    3.  Click **Update**.

    The Change Request form reopens. The **Needs review** field displays **–- None --**.


**Parent Topic:**[Tutorial: add a new change management state](t_AddNewStateTutorial.md)

**Previous topic:**[Create a new choice](t_CreateNewChoice.md)

**Next topic:**[Add a UI policy](t_AddUIPolicy.md)

