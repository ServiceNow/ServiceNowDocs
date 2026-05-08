---
title: Activity formatter
description: The activity formatter provides an easy way to track items not saved with a field in the record, for example, journal fields like comments and work notes.You can create an activity formatter for any audited table.Add an activity formatter to any form to track journal fields on the form.Enable the Live Feed-Activity toggle, which allows users to switch between the activity feed and the document feed for a record.You can customize which fields appear in the activity formatter. You can add or remove fields from the list of activities that users can select when they open the activity filter.The system property glide.ui.activity.email\_roles enables you to control which roles can see emails in the activity formatter.Use the glide.max\_activity\_size property to increase the amount of content that can be visible in the Activity Formatter.The glide.ui16.emailStreamResponseActions system property determines whether a user can reply to email using the email reply button in the activity stream in Core UI.Use the glide.ui.activity\_stream.style.comments and glide.ui.activity\_stream.style.work\_notes properties to change the color-coding in the Activity Formatter.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Formatters, Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Activity formatter

The activity formatter provides an easy way to track items not saved with a field in the record, for example, journal fields like comments and work notes.

The activity formatter is enabled by default on the Task \[task\] table and other tables that extend the Task table, such as the Incident \[incident\] table. It is also enabled on the Approvals \[sysapproval\_approver\] table.

You can filter the content that appears on the activity formatter and participate in the record feeds on the record. You can create an activity formatter for any form and configure properties that control what fields appear in the formatter. The number next to activities indicates the number of entries in the record feed. The number updates when users use the filter.

Activity type and a time stamp display in the top of each entry.

In Core UI, the activity formatter shows updates in real time so you can see the latest information without refreshing the form. User presence enables you to see when other users are entering comments.

![image.activity-formatter]

**Parent Topic:**[Using formatters](c_Formatters.md)

## Create an activity formatter

You can create an activity formatter for any audited table.

### Before you begin

Role required: ui\_macro\_admin

### Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Formatters**.

2.  Click **New**.

3.  Enter a name for the formatter, such as `Activities (task)`.

4.  Select a **Table**.

5.  Enter `activity.xml` in the **Formatter** field.

6.  Leave the **Type** as **Formatter**.

7.  Click **Submit**.


### Result

**Note:** You can create more than one activity formatter for a table, however, the system does not allow you to add more than one activity formatter to a form.

### What to do next

Add the new activity formatter to forms as needed.

## Add the activity formatter to a form

Add an activity formatter to any form to track journal fields on the form.

### Before you begin

Role required: personalize\_form

### Procedure

1.  Verify that the table associated with the form is audited.

2.  Configure the form layout to add **Activities \(filtered\)**.

    **Note:** In Core UI, you cannot place another field in between a journal field and the activities formatter. The Activity Stream is built to keep journal fields stacked on top of the activity formatter.

    Field styles are not applied to comments and work notes fields used with the activity formatter. Styles for these fields can be set using the `glide.ui.activity_stream.style.comments` and `glide.ui.activity_stream.style.work_notes` system properties located on the sys\_properties table.


## Enable the Live Feed-Activity toggle

Enable the Live Feed-Activity toggle, which allows users to switch between the activity feed and the document feed for a record.

### Before you begin

The Live Feed-Activity toggle is only supported in the Core UI. To enable it, the system property **glide.ui.polaris.experience** must be set to "false."

Role required: admin.

### About this task

Use live feed to interact with other users on a record by posting messages and adding attachments to the feed. Use the activity formatter to see an overall summary of activity for the record.

![Live Feed/Activity toggle](../image/ActivityFormatterToggle.png "Live Feed/Activity toggle")

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Find the **glide.ui.show\_live\_feed\_activity** property and set it to "true."


### Result

Form activity formatters include a Live Feed-Activity toggle.

## Customize activities

You can customize which fields appear in the activity formatter. You can add or remove fields from the list of activities that users can select when they open the activity filter.

### Before you begin

Role required: personalize\_form and personalize\_list

### About this task

![Customize the fields that appear in the activity filter](../image/customize-formatter-activities.png "Customize the fields that appear in the activity filter")

### Procedure

1.  Select the activity filter icon \(![Toggle activity filter icon](../image/Show_hide_activity_filters_UI15.png)\).

2.  At the bottom of the list, select **Configure available fields**.

3.  In the slushbucket, select the desired fields in the **Available** column and move them to the **Selected** column.

    The activities appear in alphabetical order, regardless of the order in the **Selected** column.

    **Note:** In Core UI, **Configure available fields** is responsible for the order of the Additional Comments and Work Notes fields.

4.  Select **Save** to add them to the activity formatter and the filter.


### What to do next

Administrators can also modify the system property **Incident activity formatter fields**\(**glide.ui.incident\_activity.fields**\). Access this property through **System Properties** &gt; **UI Properties**. The system automatically synchronizes the values in the system property and the selections you made.

## Configure roles for viewing emails in the activity formatter

The system property **glide.ui.activity.email\_roles** enables you to control which roles can see emails in the activity formatter.

### Before you begin

Role required: admin

### About this task

In the activity formatter, users see activity only for fields they have permission to read. For example, self-service users might see the activity formatter on the self-service view of the Incident form, but they do not see work notes, unless security rules have been customized to allow this.

If the **Emails-autogenerated** or **Emails-correspondence** field is included in the activities list, all users see all emails. No determination is made whether an end user, for example, should see an email containing work notes. Configure this property to restrict this capability to specified roles.

**Note:** Email does not appear as an activity until it is sent. If email properties are not configured for outbound delivery, the message can be found by navigating to **System Mailboxes** &gt; **Outbox**.

### Procedure

1.  Navigate to **System Properties** &gt; **UI Properties**.

2.  Locate the property labeled **List of roles \(comma separated\) that can view emails in the Activity Formatter when "Emails-autogenerated" or "Emails-correspondence" are included.**

3.  Add roles to the property, separated by commas.

    These are the only roles that can see email in the activity formatter. All other roles are prevented from seeing email. If no roles are listed, all users can see email. The itil role is on the list by default.

4.  Click **Save**.


## Configure the max activity size property

Use the glide.max\_activity\_size property to increase the amount of content that can be visible in the Activity Formatter.

### Before you begin

Role required: admin

### About this task

The default size for an activity is 100 \* 1024, which causes large amounts of content to be hidden in the Activity Formatter. You can change the default value by adding the glide.max\_activity\_size property.

### Procedure

1.  Type `sys_properties.list` in the Application Navigator.

2.  Select **New** and enter the following values.

<table id="table_td5_tnz_p1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

glide.max\_activity\_size

</td></tr><tr><td>

Type

</td><td>

integer

</td></tr><tr><td>

Value

</td><td>

102400Use this field to increase the number of content allowed in the Activity Formatter. This value should be in bytes, for example 100 \* 1024, or 102400.

</td></tr></tbody>
</table>
## Enable the email reply button for the activity formatter in Core UI

The **glide.ui16.emailStreamResponseActions** system property determines whether a user can reply to email using the email reply button in the activity stream in Core UI.

### Before you begin

Role required: admin

### Procedure

1.  In the navigation filter, type `sys_properties.list`.

2.  Add the following system property.

    For more information on adding a system property, see [Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#).

    |Field|Description|
    |-----|-----------|
    |**Name**|**glide.ui16.emailStreamResponseActions**|
    |**Description**|Add the email reply button to the activity stream.|
    |**Type**|true \| false|
    |**Value**|Set the value to **true**. The default value if this property is not configured is false.|

3.  Select **Submit**.


## Configure activity formatter colors

Use the glide.ui.activity\_stream.style.comments and glide.ui.activity\_stream.style.work\_notes properties to change the color-coding in the Activity Formatter.

### Before you begin

Role required: admin

### Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  Add a system property for the **Additional comments** field.

    1.  Select **New**.

    2.  Enter the following values.

        |Field|Description|
        |-----|-----------|
        |Name|`glide.ui.activity_stream.style.comments`|
        |Type|string|

    3.  Select **Submit**.

3.  Change the color of the **Additional comments** field.

    1.  In the System Properties list, select the glide.ui.activity\_stream.style.comments record.

    2.  Enter the color that you want to use.

        For example, enter `LightGreen`. The default value is transparent.

    3.  Select **Update**.

4.  Add a system property for the **Work notes** field.

    1.  Select **New**.

    2.  Enter the following values.

        |Field|Description|
        |-----|-----------|
        |Name|`glide.ui.activity_stream.style.work_notes`|
        |Type|string|

5.  Change the color of the **Work notes** field.

    1.  In the System Properties list, select the glide.ui.activity\_stream.style.work\_notes record.

    2.  Enter the color that you want to use.

        For example, enter `Blue`. The default value is gold.

    3.  Select **Update**.


