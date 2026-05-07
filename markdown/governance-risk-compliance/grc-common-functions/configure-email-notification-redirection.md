---
title: Configure GRC notification redirection
description: Create notification routing rules that automatically direct users to workspace view or classic view based on their access permissions.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [GRC notification redirection, Common GRC features, Governance, Risk, and Compliance]
---

# Configure GRC notification redirection

Create notification routing rules that automatically direct users to workspace view or classic view based on their access permissions.

## Before you begin

Role required: sn\_grc\_workspace.admin

## About this task

Notification routing rules determine which workspace a user is directed to when they select a notification link. You create routing rules by adding records to the notification redirection metadata table. Each rule maps a table to a target workspace with an order value that determines evaluation priority. If a user has access to only one workspace for a table, the system automatically directs them to that workspace. Routing rules are used only when a user has access to multiple workspaces for the same table. In this case, the system directs them to the workspace with the lowest order value they can access.

## Procedure

1.  Navigate to **All** &gt; **GRC Notification Redirection** &gt; **Notification Routing Rules**.

2.  **New**.

3.  On the form, fill in the fields.

<table id="choicetable_yhj_ymw_h3c"><thead><tr><th align="left" id="d199135e98">

Field

</th><th align="left" id="d199135e101">

Description

</th></tr></thead><tbody><tr><td id="d199135e107">

**Table**

</td><td>

The table for which notification links are redirected to workspace view.

</td></tr><tr><td id="d199135e116">

**Target Workspace**

</td><td>

The workspace to which users are redirected when they select notification links.

</td></tr><tr><td id="d199135e125">

**Order**

</td><td>

The evaluation priority for the routing rule. Lower values are evaluated first when multiple rules exist for the same table.

</td></tr><tr><td id="d199135e134">

**Active**

</td><td>

Indicates whether the routing rule is active.

 Only active rules apply to notification redirection.

</td></tr><tr><td id="d199135e150">

**Table filter**

</td><td>

Optional conditions that determine when the routing rule applies.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  If you want to configure multiple workspaces for the same table, repeat this procedure for each workspace using different order values.

    Users are directed to the first workspace that they can access based on the order value.


## Result

The notification routing rule is active. Users with access to the configured workspace are directed to the workspace when they select notification links for records from the specified table. Users without workspace access are directed to the classic view.

**Parent Topic:**[GRC notification redirection](../concept/email-notification-redirection.md)

