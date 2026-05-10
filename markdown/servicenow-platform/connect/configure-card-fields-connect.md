---
title: Configure the fields on a record card in Connect
description: When a record is either linked to or created from a Connect Chat conversation, the details of the record display as a card in the chat window.
locale: en-US
release: australia
product: Connect
classification: connect
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connect administration, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the fields on a record card in Connect

When a record is either linked to or created from a Connect Chat conversation, the details of the record display as a card in the chat window.

## Before you begin

Role required: admin

## About this task

The card view only applies to the full Connect Chat page and the end-user view of Connect Support conversations.

## Procedure

1.  Select the menu icon \( ![Menu icon](../image/IconMenu.png)\) on any of the column names of the incident list view.

2.  Right-click on the column name and select **Configure** &gt; **List Layout**.![Screen shot of list layout example](../image/list-layout-screenshot.png)

3.  On the Configuring Incidents List screen, select **New** from the View name list.![Screen shot of Configuring Incidents List](../image/config-incidents-list-screenshot.png)

4.  In the Create New View dialog, enter `Connect` in the View name field. ![Create new view dialog](../image/create-new-view.png).

    For more information on creating a form view, see [Create and delete views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/create-delete-view.md) .

    You cannot remove the Author or the Updated fields from the card regardless of whether they are on the view or not. The card always shows the Short Description field in the top even if it is in a different order in the list.

5.  Choose the fields that you want to display on the Connect card and select Save.![Screen shot of Configuring Incidents List](../image/configure-card-screenshot3.png)

6.  Validate that the card displays the fields in a Connect Chat conversation.


