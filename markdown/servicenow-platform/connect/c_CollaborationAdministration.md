---
title: Connect Chat administration
description: Administrators can configure various performance settings and features of Connect Chat.The email notification interval determines how long the system waits before sending a Connect Chat email notification to an inactive user.Record conversations are enabled for all tables that extend Task \[task\] by default. You can configure record conversations for additional tables that extend Task.Users can follow records in Connect for any table that extends Task \[task\] by default. You can disable this functionality for all tables.Users can follow records in Connect for any table that extends Task \[task\] by default. You can disable this functionality for a specific table.You can disable Connect Chat to prevent users from being able to chat within the platform.
locale: en-US
release: australia
product: Connect
classification: connect
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Connect Chat, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Connect Chat administration

Administrators can configure various performance settings and features of Connect Chat.

**Note:** There are also settings that apply to both Connect Chat and Connect Support. For more information, see [Connect administration](c_ConnectAdministration.md).

## Configure the email notification interval

The email notification interval determines how long the system waits before sending a Connect Chat email notification to an inactive user.

### Before you begin

Role required: admin

### About this task

The default interval is 3 minutes. You can change this value.

### Procedure

1.  Navigate to **All** &gt; **Connect** &gt; **Administration** &gt; **Properties**.

2.  Locate the property called **Number of minutes to wait before collecting unread messages and sending an email to offline users.** \(**collaboration.email\_interval**\) and set the value to a different number of minutes.

3.  Click **Save**.


### Result

When an offline user is sent a Connect message, the collaboration.new\_offline\_message event fires. The system waits the amount of time provided in the collaboration.email\_interval property, then triggers the collaboration.notify\_offline\_user and collaboration.notify\_offline\_user.group events \(depending on if the conversation was peer to peer or a group conversation\).The sysevent\_email\_action record listens for collaboration.notify\_offline\_user\(.group\) then builds an email notification containing all the messages from the last collaboration.email\_interval minutes that the user has received in that conversation.

## Enable record conversations for a table

Record conversations are enabled for all tables that extend Task \[task\] by default. You can configure record conversations for additional tables that extend Task.

### Before you begin

Role required: admin

### About this task

To create record conversations, users must have access to the **Follow** button in the form header. To show the button and thus enable record conversations for a table, the following conditions must be true.

-   The **live\_feed** dictionary attribute must be set to **true** for the table. By default, **live\_feed=true** for all tables that extend Task \[task\].
-   The **glide.live\_feed.task\_header\_button** property must be set to **both** or **collaboration**. By default, **glide.live\_feed.task\_header\_button** is set to **collaboration**.

### Procedure

1.  Navigate to the list view of a table for which you want to enable record conversations.

2.  Perform the appropriate action for the list version.

<table id="choicetable_g3c_qhc_mv"><thead><tr><th align="left" id="d533382e267">

Version

</th><th align="left" id="d533382e270">

Action

</th></tr></thead><tbody><tr><td id="d533382e276">

**List v3**

</td><td>

1.  Click the list title menu and select **Configure**.
2.  In the Configure window, click **Dictionary**.


</td></tr><tr><td id="d533382e300">

**List v2**

</td><td>

Right-click any column header and select **Configure** &gt; **Dictionary**.

</td></tr></tbody>
</table>    The list of dictionary entries for the table appears.

3.  Open the dictionary entry that has **Type** set to **Collection**.

    The Dictionary Entry form appears.

4.  In the **Attributes** related list, click **New**.

    The Dictionary Attribute form appears.

5.  In the **Attribute** field, enter `Live feed`.

6.  In the **Value** field, enter `true`.

7.  Click **Submit**.

8.  Navigate to **Collaborate** &gt; **Administration** &gt; **Properties**.

9.  Locate the property called **Determine whether or not a button is shown in task forms to view the Collaboration document conversation or Live Feed Record Feed related to the task** \(**glide.live\_feed.task\_header\_button**\).

10. Ensure the property is set to **both** or **collaboration**.

    The **glide.live\_feed.task\_header\_button** property also controls whether the show Live Feed icon \(![Show Live Feed icon](../../live-feed/image/ShowLiveFeedIcon.png)\) appears. If the property is set to **collaboration**, the show Live Feed icon does not appear on form headers.


**Related topics**  


[Dictionary attributes](https://www.servicenow.com/docs/access?context=c_DictionaryAttributes&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

## Prevent users from following records in Connect for all tables

Users can follow records in Connect for any table that extends Task \[task\] by default. You can disable this functionality for all tables.

### Before you begin

Role required: admin

### About this task

To disable record conversations for all tables, prevent the **Follow** button from appearing in all form headers by editing the **glide.live\_feed.task\_header\_button** property.

### Procedure

1.  Navigate to **sys\_properties.list**.

2.  Locate the **glide.live\_feed.task\_header\_button** property.

3.  Set the **Value** to **live\_feed**.


## Prevent users from following records in Connect for a specific table

Users can follow records in Connect for any table that extends Task \[task\] by default. You can disable this functionality for a specific table.

### Before you begin

Role required: admin

### About this task

To disable record conversations for a specific table, prevent the **Follow** button from appearing in form headers for the table. To do so, set the **live\_feed** dictionary attribute to **false** for the table.

### Procedure

1.  Navigate to the list view of a table for which you want to disable record conversations.

2.  Perform the appropriate action for the list version.

    |Version|Action|
    |-------|------|
    |**List v2**|Right-click any column header and select **Configure** &gt; **Dictionary**.|
    |**List v3**|Open the list title menu and select **Configure**, and then select **Dictionary**.|

    The list of dictionary entries for the table appears.

3.  Open the dictionary entry that has **Type** set to **Collection**.

    The Dictionary Entry form appears.

4.  In the **Attributes** related list, locate the **Live feed** dictionary attribute.

5.  Set the **Value** to **false**.

    Setting the dictionary attribute to **false** also removes the show Live Feed icon \(![Show Live Feed icon](../../live-feed/image/ShowLiveFeedIcon.png)\) for the table.


**Related topics**  


[Dictionary attributes](https://www.servicenow.com/docs/access?context=c_DictionaryAttributes&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

## Disable Connect Chat

You can disable Connect Chat to prevent users from being able to chat within the platform.

### Before you begin

Role required: admin

### About this task

Disabling Connect Chat hides the Connect Chat sidebar icon. Users who try to access Connect Chat from the navigation pane receive a message that says Connect has been disabled.

### Procedure

1.  In the navigation filter, type `sys_properties.list` and press Enter.

2.  Search for the **glide.connect.chat.disabled** property.

3.  Set the property value to **true**.


