---
title: Administering tags
description: If you have an administrator role, you can configure and manage all tags, even tags created by other users. You can also configure notifications, auto-assignment, and Zing indexing for tags.You can create a tag directly from the Tags list.From the Tags module, you can edit all tags.Configure the system to automatically assign a tag to records that match conditions defined in the tag record.You can enable the system to send a notification when a record with a certain tag is updated.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Tags, Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Administering tags

If you have an administrator role, you can configure and manage all tags, even tags created by other users. You can also configure notifications, auto-assignment, and Zing indexing for tags.

You must have the tags\_admin role for these administrative tasks.

**Parent Topic:**[Tags](c_Tags.md)

## Create a tag from the Tags list

You can create a tag directly from the Tags list.

### Before you begin

Role required: tags\_admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tags** or **Self-Service** &gt; **My Tags**.

2.  Click **New**.

3.  Enter a name for the tag in the **Name** field.

4.  Modify tag settings.

<table id="table_wcw_1vd_31b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Owner

</td><td>

Specifies the owner of the tag. Users are allowed to change the ownership of the tag to someone else.

</td></tr><tr><td>

Type

</td><td>

Specifies the type of tag.-   **Standard:** is controlled by users who have access to the tag. These users can add or remove records from the tag.
-   **Most Active:** displays the most frequently accessed modules and is automatically maintained by the system. There is no maximum duration a module can remain as most active.
-   **Most Recent:** displays the most recently accessed modules and is automatically maintained by the system.
-   **Most Active Record:** displays the most frequently viewed records and is automatically maintained by the system. There is no maximum duration a record can remain as most active.
-   **Most Recent Record:** displays the most recently viewed records and is automatically maintained by the system.
 Only tags of the **Standard** or **Most Recent Record** types appear on the Tagged Documents page.

</td></tr><tr><td>

Viewable by

</td><td>

Specifies the sharing level. By default tags are visible only to the user \(**Me**\), but you can share tags with **Groups and Users**. Users with the tags\_admin role are the only users who can create global tags shared with **Everyone**.

</td></tr><tr><td>

Active

</td><td>

Specifies whether the tag is enabled or disabled.

</td></tr></tbody>
</table>
## Edit tags from the Tags module

From the Tags module, you can edit all tags.

### Before you begin

Role required: tags\_admin

### About this task

**Note:** Tag names are case-insensitive and must not include punctuation.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tags**.

2.  Open a tag.

3.  Make the necessary changes.

4.  Click **Update**.


## Configure tags to assign automatically

Configure the system to automatically assign a tag to records that match conditions defined in the tag record.

### Before you begin

Role required: tags\_admin, however for users with the tags\_admin role to be able to create conditions for labels, you need to create the following ACLs. Creating ACLs requires the security\_admin elevated role. Include tags\_admin as a required role for each ACL. For more information on creating an ACL, see [Create an ACL rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/t_CreateAnACLRule.md).

|Name|Operation|
|----|---------|
|label\_table|read|
|label\_table|write|
|label\_table|create|
|label\_auto|read|
|label\_auto|write|
|label\_auto|create|
|\(Optional\) label\_table|delete|
|\(Optional\) label\_auto|delete|

### About this task

Use automatically assigned tags to group high urgency incidents, overdue incidents, canceled changes, or any other set of records. The system automatically assigns the tag to records that match the criteria and removes the tag from records that no longer match the criteria.

**Note:** Tags can't be automatically assigned to a record when its condition includes a dot-walked field.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tags**.

2.  Open the tag that you want to assign automatically.

3.  Configure the form to add the **Conditions for Labels** embedded list.

4.  Create a row in the **Conditions for Labels** list.

5.  Click the reference icon in the **Table** column.

    The Label Table list opens in a pop-up window.

6.  Click **New**.

7.  Enter a **Name**, select a **Table**, and add conditions for the automatic assignment of the tag.

8.  Click **Submit**.

9.  Click the check mark icon to save the new row.

10. Click **Update**.


## Configure notifications for tagged records

You can enable the system to send a notification when a record with a certain tag is updated.

### Before you begin

Role required: tags\_admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tags**.

2.  Open a tag.

3.  In the **Label Entries** related list, open the record for which you want notifications.

4.  Select the **Notify onchange** check box to be notified any time the record is modified.

5.  Use the **Notify when** condition builder to specify the conditions that must be true to trigger the notification.

6.  Select a business rule in the **Notify script** field.

7.  Save the record.


