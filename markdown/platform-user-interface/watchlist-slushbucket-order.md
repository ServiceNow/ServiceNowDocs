---
title: Configure order buttons on the watch list slushbucket
description: When you add multiple users to a glide\_list, such as a watch list, the slushbucket does not display the order buttons for the list of selected members. You can set a dictionary attribute to display the order buttons.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure email notifications, Add users to a watch list, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Configure order buttons on the watch list slushbucket

When you add multiple users to a glide\_list, such as a watch list, the slushbucket does not display the order buttons for the list of selected members. You can set a dictionary attribute to display the order buttons.

## Before you begin

Role required: admin

## About this task

The slushbucket opens when the user clicks the add/remove multiple users icon.

![Add/remove multiple users opens the slushbucket.](../image/add-multiple-users-icon.png)

By default, the order buttons on the right are not displayed. Follow the procedure to display the order buttons.

![Display the order buttons](../image/glidelist-slushbucket-order-buttons.png)

## Procedure

1.  Open a task record that displays the **Watch list** field.

2.  Right-click the label and select **Configure Dictionary**.

3.  Under **Related Links**, click **Advanced view**.

4.  In the **Attributes** field, enter `maintain_order=true` separated by a comma if necessary.

5.  Click **Update**.


**Parent Topic:**[Configure email notifications for watch lists](t_ConfigNotifications4WatchLists.md)

**Related topics**  


[Altering tables and fields using dictionary attributes](https://www.servicenow.com/docs/access?context=c_DictionaryAttributes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

