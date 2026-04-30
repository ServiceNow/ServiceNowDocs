---
title: Hide email addresses in a watch list
description: You can remove the email address text entry element from a watch list by modifying the dictionary.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure email notifications for watch lists, Add users to a watch list, Add and customize a field in a table, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Hide email addresses in a watch list

You can remove the email address text entry element from a watch list by modifying the dictionary.

## Before you begin

Role required: admin

## Procedure

1.  Open a task record that displays the **Watch list** field.

2.  Right-click the label and select **Configure Dictionary**.

3.  In the **Attributes** related list, click **New**.

4.  Enter or select the **no\_email** attribute and enter `true` in the **Value** field.

5.  Click **Submit**.


## Result

The email entry field is hidden. Users can select users from the reference field to add to the watchlist.

**Parent Topic:**[Configure email notifications for watch lists](t_ConfigNotifications4WatchLists.md)

**Related topics**  


[Altering tables and fields using dictionary attributes](../../reference-pages/concept/c_DictionaryAttributes.md)

