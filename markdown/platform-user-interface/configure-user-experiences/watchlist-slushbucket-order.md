---
title: Configure order buttons on the watch list slushbucket
description: When you add multiple users to a glide\_list, such as a watch list, the slushbucket does not display the order buttons for the list of selected members. You can set a dictionary attribute to display the order buttons.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-user-experiences/watchlist-slushbucket-order.html
release: australia
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure email notifications for watch lists, Add users to a watch list, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Configure order buttons on the watch list slushbucket

When you add multiple users to a glide\_list, such as a watch list, the slushbucket does not display the order buttons for the list of selected members. You can set a dictionary attribute to display the order buttons.

## Before you begin

Role required: admin

## About this task

The slushbucket opens when the user clicks the add/remove multiple users icon.

\[Omitted image "add-multiple-users-icon.png"\] Alt text: Add/remove multiple users icon opens the slushbucket

By default, the order buttons on the right are not displayed. Follow the procedure to display the order buttons.

\[Omitted image "glidelist-slushbucket-order-buttons.png"\] Alt text: Display the order buttons

## Procedure

1.  Open a task record that displays the **Watch list** field.

2.  Right-click the label and select **Configure Dictionary**.

3.  Under **Related Links**, click **Advanced view**.

4.  In the **Attributes** field, enter `maintain_order=true` separated by a comma if necessary.

5.  Click **Update**.


**Parent Topic:**[Configure email notifications for watch lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/t_ConfigNotifications4WatchLists.md)

**Related topics**  


[Altering tables and fields using dictionary attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DictionaryAttributes.md)

