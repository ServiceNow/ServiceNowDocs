---
title: Create a special handling note
description: Create a special handling note for a record, such as a customer service case.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage special handling notes, Agent management, Use, Customer Service Management]
---

# Create a special handling note

Create a special handling note for a record, such as a customer service case.

## Before you begin

Role required: sn\_shn.admin or sn\_customerservice\_manager

## About this task

Use special handling notes to highlight important information about individual records, such as a case or account record.

You can create special handling notes from the Special Handling Notes module in the application navigator or from a record that has been configured to use special handling notes.

**Important:** While this feature provides the flexibility to create complex conditions, it is recommended that you keep the configuration simple and use dot walking sparingly. Creating complex conditions for special handling notes can affect the load time.

## Procedure

1.  Perform one of the following actions.

    -   **CSM Configurable Workspace**: Navigate to the desired form, select the More actions menu in the record header and then select **Special Handling Notes**.
    -   **Core UI**: Navigate to the desired form and select the **Create Special Handling Notes** related link. You can find these links in the Related Links section at the bottom of the form.
    -   Navigate to **All** &gt; **Special Handling Notes** &gt; **Special Handling Notes** and select **New** in the Special Handling Notes list form header.
2.  Fill in the fields, as necessary.

<table id="table_czw_glr_sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short Description

</td><td>

A brief description of the note which is displayed in the Special Handling Notes list.

</td></tr><tr><td>

Message

</td><td>

The detailed content of the note.

</td></tr><tr><td>

Display as pop-up alert

</td><td>

Displays this note in the Special Handling Notes pop-up window.

</td></tr><tr><td>

Type

</td><td>

The type of special handling note:-   **Standard**: Create a note for a specific record, which you select in the **Related record** field.
-   **Conditional**: Create a note for multiple records which meet certain conditions. Select a **Table name** and then create **Conditions**.


</td></tr><tr><td>

Priority

</td><td>

The priority of the note:-   1-Critical
-   2-High
-   3-Moderate
-   4-Low


</td></tr><tr><td>

Status

</td><td>

The status of the special handling note:-   **1-Active**: The note is active and appears in the Notes list or pop-up window.
-   **2-Inactive**: The note is inactive and does not appear in the Notes list or pop-up window.

Inactive notes are removed from the Notes list but can be seen by navigating to **Special Handling Notes** &gt; **Special Handling Notes**.

-   **3-Expired**: The note has reached its expiration date.


</td></tr><tr><td>

Effective immediately

</td><td>

Check box to make the special notes effective immediately. The status is set to **1 -Active**.Deselect this check box to display the **Effective on** field.

</td></tr><tr><td>

Effective on

</td><td>

The date on which the special notes become effective.Enter a date for the special notes to become effective and click **Update**. The status is set to **2 - Inactive** until the date is reached.

</td></tr><tr><td>

Expires on

</td><td>

The date on which the note expires. Select a date from the calendar and click **Save**.The **Deactivate Special Handling notes** scheduled job runs daily at midnight and checks all active alerts. If the notes have reached their expiration date, it sets the status to **Expired**.

 The **Deactivate Special Handling notes** scheduled job also checks the **Effective on** field. If the status is active or inactive and the expiry date has been reached, it sets the status to **Expired**. If the status is inactive and the effective on date has been reached, it sets the status to **Active**.

</td></tr><tr><td>

Related record

</td><td>

The record for which this note is created. This field appears when you select **Standard** in the **Type** field.If you access this form from the **Create Special Handling Notes** related link, the record number is automatically filled in.

 To select a record, select a **Table name** and a **Document** from the pop-up window. The tables available for selection have been configured to use special handling notes.

</td></tr><tr><td>

Table name

</td><td>

The table that stores the entity for which the note is being created. This field appears when you select **Conditional** in the **Type** field.The default is the first table which has been configured to use special handling notes.

 After you select a table, a link is displayed with the number of matching records. This link is updated after you select one or more conditions. Click the link to display these records in a list.

</td></tr><tr><td>

Conditions

</td><td>

This field appears when you select **Conditional** in the **Type** field.Use the buttons in this field to build one or more conditions on the selected table. A condition is made up of a selected field, an operator, and a value. Add conditions using the **AND** and **OR** buttons. Delete conditions by clicking the **Delete** button to the right of a condition.

</td></tr></tbody>
</table>3.  Click **Submit**.


**Related topics**  


[Special handling notes](../concept/c_OnScreenAlerts.md)

