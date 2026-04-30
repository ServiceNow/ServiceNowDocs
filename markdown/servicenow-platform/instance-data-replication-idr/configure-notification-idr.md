---
title: Configure error notifications in Instance Data Replication
description: Notify one or more users when errors occur in Instance Data Replication \(IDR\).
locale: en-US
release: zurich
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Resolving errors, Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Configure error notifications in Instance Data Replication

Notify one or more users when errors occur in Instance Data Replication \(IDR\).

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the producer or consumer replication set for which you want to configure notifications.

    |Option|Description|
    |------|-----------|
    |**Producer instance**|Navigate to **All** &gt; **Instance Data Replication** &gt; **Producer Replication Sets** and select a replication set.|
    |**Consumer instance**|Navigate to **All** &gt; **Instance Data Replication** &gt; **Consumer Replication Sets** and select a replication set.|

2.  Select the **Notification Configuration** related link.

3.  In the **When to send** tab, configure when the notification is sent.

<table id="choicetable_t2s_vlq_qdc"><tbody><tr><td id="d597532e138">

**Record is inserted or updated**

</td><td>

1.  Select **Inserted**, **Updated**, or both **Inserted** and **Updated**.
2.  Configure the conditions under which this notification is sent using the condition builder. The default condition is **\[Status\] \[is\] \[Replication Error\]**


</td></tr><tr><td id="d597532e170">

**Event is fired**

</td><td>

1.  Select the event type that sends the notification.
2.  Configure the conditions under which this notification is sent using the condition builder. The default condition is **\[Status\] \[is\] \[Replication Error\]**


</td></tr><tr><td id="d597532e190">

**Triggered**

</td><td>

Select this option to trigger the notification from a Workflow Studio flow.

</td></tr></tbody>
</table>4.  In the **Who will receive** tab, select the users, groups, or user groups who will receive the notification.

5.  In the **What it will contain** tab, select an email template to populate the Subject and Message HTML.

    The default template is Unsubscribe and Preferences. You can override the template and customize the text as needed.

6.  Verify that the notification contents are correct by selecting **Preview Notification**.

7.  Select **Update**.


**Parent Topic:**[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

