---
title: Special handling notes
description: The Special Handling Notes application enables you to create notes that bring important information about individual records, such as a case or account record, to the user's attention.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-18"
reading_time_minutes: 6
breadcrumb: [Administer Customer Service Management, Customer Service Management]
---

# Special handling notes

The Special Handling Notes application enables you to create notes that bring important information about individual records, such as a case or account record, to the user's attention.

![Special Handling Notes pop-up window displaying multiple notes with header, description, and priority illustrated with colours.](../image/csm-special-handling-note.png "Special handling notes in CSM Configurable Workspace")

You can create special handling notes for specific records or for a set of records that meet one or more conditions. You can also configure this application to display any special handling notes from related records, such as the account or the product associated with a customer service case.

**Important:** Use special handling notes for special circumstances and not for the general case processing workflow. It is not recommended to have more than 10k special handling notes on an instance. In addition, avoid complex conditions and use dot walking sparingly when creating special handling notes. Having a large number of notes with complex conditions can affect the load time.

## Configuring special handling notes

Users with the sn\_shn.admin role can configure the desired entity tables, such as the Case table, to use special handling notes. Special handling notes can be configured to display in the following ways:

-   [In a pop-up window that appears when a user accesses a form](c_OnScreenAlerts.md#section_why_gwg_scc).
-   [In an embedded list or a related list on a record form](c_OnScreenAlerts.md#section_myw_fwg_scc).

For more information, see the following configuration topics:

-   [Configure special handling notes](../task/configure-special-handling-notes.md)
-   [Configure an entity table to use special handling notes](../task/t_ConfigEntityToUseSHNotes.md)
-   [Configure a form to show special handling notes](../task/t_ConfigFormToShowOnScreenAlerts.md)

## Creating, updating, and deleting special handling notes

Users with the sn\_shn.admin role can create, update, and delete special handling notes. Users with the sn\_shn.editor role can view and update notes and users with the sn\_shn.user role can view notes. For more information about creating special handling notes, see the following topics:

-   [Create a special handling note](../task/t_CreateAnOnScreenAlert.md)
-   [Components installed with Special Handling Notes](../reference/r_InstalledWithSpecHandNotes.md#)

Special handling notes display important information to the user. In addition to a message, a special handling note also has a status, an assigned priority, and an expiration date.

The status of a note can be one of the following:

<table id="table_apb_1tt_jyb"><thead><tr><th>

Status

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Active

</td><td>

The note is active. Active notes appear on the Special Handling Notes list or pop-up window.

 Active notes remain on the list until they are set to **Inactive** or **Expired**.

 Active notes remain on the pop-up window until dismissed or until they are set to **Inactive** or **Expired**.

</td></tr><tr><td>

Inactive

</td><td>

The note is no longer active. Users with the sn\_shn.admin or sn\_shn.editor role can set a note to **Inactive** if the information in the note is no longer useful. When a note is set to **Inactive**, it is removed from the Special Handling Notes list or pop-up window.

 Inactive notes can be viewed by navigating to **Special Handling Notes** &gt; **Special Handling Notes**.

</td></tr><tr><td>

Expired

</td><td>

The note has reached it's expiration date or it has been expired manually.If a note is expired, the form becomes read-only for all user roles other than the system administrator.

 A note is expired automatically by a scheduled job when it reaches it's expiration date. The scheduled job also sets any inactive notes to expired if the inactive notes have reached their expiration date.

</td></tr></tbody>
</table>A note can be assigned one of the following priorities. Each priority has an associated color, which is displayed as a colored bar in the pop-up window and as a colored circle in the **Priority** field in a list. The Core UI and the CSM Configurable Workspace interface use different colors to represent priority.

|Priority|Core UI|CSM Configurable Workspace|
|--------|-------|--------------------------|
|1 - Critical|Red|Red|
|2 - High|Orange|Orange|
|3 - Moderate|Green|Purple|
|4 - Low|Blue|Gray|

When creating a special handling note, you can make it effective right away or you can select a date when it becomes effective. You can also select an expiration date.

## Special handling notes pop-up window

Special handling notes can be displayed on a form in a pop-up window. Users with the sn\_shn.admin role can configure a form to display the Special Handling Notes pop-up window. This window appears when you access a record that has one or more active notes. The pop-up window displays the following information for each note:

-   Message
-   Priority

To dismiss a note, click **Dismiss**. Once you dismiss a note, it no longer appears in the pop-up window. To close the Special Handling Notes pop-up window, click **X**.

## Special handling notes list

Special handling notes can be displayed on a form in an embedded or related list. Users with the sn\_shn.admin role can configure a form to display the Special Handling Notes list. This list appears on a form when there are one or more active notes for a record. The Special Handling Notes list displays the following information for a note:

-   Message
-   Expiration date
-   Priority
-   Table

## Resurfacing special handling notes

Special handling notes are typically displayed in a pop-up window when a record is opened. Agents can view the special handling notes, dismiss individual notes, and close the window. If an agent closes the window, they can open it again and display the special handling notes without closing and reopening the record tab in CSM Configurable Workspace.

To open the special handling notes pop-up window after it has been closed, select **Special handling notes** from the More actions menu \(![agent workspace more UI actions icon](../image/agent-workspace-more-ui-actions-icon.jpg)\) on the action bar. If no special handling notes are available, the system displays an informational message: “No special handling notes are available.”

The **Special handling notes** action that agents can use to reopen the special handling notes window is currently available on the following record pages in CSM Configurable Workspace:

-   Front-line case page
-   CSM default record page

## Expiring special handling notes

The **Deactivate Special Handling Notes** scheduled job, which runs daily at midnight, checks the dates in the **Effective on** and **Expires on** fields for each note.

-   If a special handling note has reached its **Effective on** date, the scheduled job sets the status of the note to **Active**.
-   If a special handling note has reached its **Expires on** date, the scheduled job sets the status of the note to **Expired**.

## Domain separation for Special Handling Notes

The Special Handling Notes application supports domain separation as a process-separated table.

When inserting or updating a special handling note, the picker domain scope takes precedence by design with the Overrides \[sys\_overrides\] field on process-separated tables. For more information, see [Process administration](https://www.servicenow.com/docs/access?context=c_DelegatedAdministration&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

**Parent Topic:**[Customer Service Management](c_CustomerServiceManagement.md)

**Related topics**  


[Configure special handling notes](../task/configure-special-handling-notes.md)

[Manage special handling notes](../task/manage-special-handling-notes.md)

