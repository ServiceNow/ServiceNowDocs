---
title: Apply user criteria to a page, widget, or widget instance
description: Assign user criteria to pages, widgets, or widget instances to limit user access to content in a portal.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [User criteria for Service Portal, Managing portal access, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Apply user criteria to a page, widget, or widget instance

Assign user criteria to pages, widgets, or widget instances to limit user access to content in a portal.

## Before you begin

Activate the Service Portal User Criteria Support \(com.glide.service-portal.user-criteria\) plugin and set the **glide.service\_portal.user\_criteria\_enabled** system property to **true**.

Role required: admin or sp\_admin

## About this task

You can apply several user criteria records to a single portal item.

## Procedure

1.  In the Service Portal Configuration page \(**Service Portal** &gt; **Service Portal Configuration**\), open the Page Editor.

2.  Select a page from the list.

3.  Select a page, widget, or widget instance node from the page tree.

4.  Under related lists, click **Who Can View** or **Who Cannot View**.

5.  Click **New**.

6.  Select a criteria from the **Can View** or **Cannot View** list.

    Selecting criteria from the **Can View** or **Cannot View** list applies user criteria records created in [Create a user criteria record for Service Portal](create-user-criteria-record.md) to the selected page, widget, or widget instance.

7.  Click **Save**.


**Parent Topic:**[User criteria for Service Portal](../concept/user-criteria.md)

