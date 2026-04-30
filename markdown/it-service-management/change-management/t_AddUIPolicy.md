---
title: Add a UI policy
description: Add a UI policy to display the Needs review field for Normal change requests when it reaches the Complete state.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Tutorial: add a new change management state, Reference section for Change Management, Change Management, IT Service Management]
---

# Add a UI policy

Add a UI policy to display the **Needs review** field for **Normal** change requests when it reaches the **Complete** state.

## Before you begin

Role required: admin

## Procedure

1.  Open the **Change Request** form.

2.  Open the form context menu and select **Configure** &gt; **UI Policies**.

3.  Click **New**.

4.  Enter the following values on the **UI Policy** form.

<table id="table_ecg_y2m_b1b"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Change Request

</td></tr><tr><td>

Short description

</td><td>

Show “Needs review” field

</td></tr><tr><td>

Conditions

</td><td>

\[Type\] \[is\] \[Normal\]\[State\] \[is one of\] \[Review, Complete, Closed\]

</td></tr></tbody>
</table>5.  Open the form context menu and select **Save** to create the UI Policy record and stay on the form.

    The **UI Policy Actions** related list appears.

6.  Click **New** in the **UI Policy Actions** related list.

7.  Enter the following values.

    |Field|Value|
    |-----|-----|
    |Field name|Needs review|
    |Mandatory|True|
    |Visible|True|

8.  Click **Submit** to create the UI Policy action and return to the **UI Policy** form.

    ![New UI policy record](../image/NewStateTutUIPolicy1.png)


**Parent Topic:**[Tutorial: add a new change management state](t_AddNewStateTutorial.md)

**Previous topic:**[Create a custom field](t_CreateCustomField.md)

**Next topic:**[Create an ACL](t_CreateNewACL.md)

