---
title: Configure the fields on a record card in Connect
description: When a record is either linked to or created from a Connect Chat conversation, the details of the record display as a card in the chat window.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/connect/configure-card-fields-connect.html
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

1.  Select the menu icon \( \[Omitted image "IconMenu.png"\] Alt text: Menu icon\) on any of the column names of the incident list view.

2.  Right-click on the column name and select **Configure** &gt; **List Layout**.\[Omitted image "list-layout-screenshot.png"\] Alt text: Screen shot of list layout example

3.  On the Configuring Incidents List screen, select **New** from the View name list.\[Omitted image "config-incidents-list-screenshot.png"\] Alt text: Screen shot of Configuring Incidents List

4.  In the Create New View dialog, enter `Connect` in the View name field. \[Omitted image "create-new-view.png"\] Alt text: Create new view dialog.

    For more information on creating a form view, see Create and delete views .

    You cannot remove the Author or the Updated fields from the card regardless of whether they are on the view or not. The card always shows the Short Description field in the top even if it is in a different order in the list.

5.  Choose the fields that you want to display on the Connect card and select Save.\[Omitted image "configure-card-screenshot3.png"\] Alt text: Screen shot of Configuring Incidents List

6.  Validate that the card displays the fields in a Connect Chat conversation.


