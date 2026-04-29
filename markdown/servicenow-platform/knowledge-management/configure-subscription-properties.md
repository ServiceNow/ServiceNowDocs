---
title: Configure knowledge subscriptions
description: Configure knowledge subscriptions by activating the Knowledge Management Advanced plugin and setting the subscription properties.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure knowledge subscriptions

Configure knowledge subscriptions by activating the Knowledge Management Advanced plugin and setting the subscription properties.

## Before you begin

Ensure that the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) is activated.

**Note:** The Knowledge Management Advanced plugin activates the Subscriptions and Activity Feed Framework plugin \(com.snc.activity\_subscriptions\).

Role required: knowledge\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Properties**.

2.  In the **KM Subscription Properties** section, configure the following properties.

<table id="table_ljp_3hb_qzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable subscribe feature for KM\[glide.knowman.enable\_km\_subscription\]

</td><td>

Enables or disables the Knowledge Management knowledge subscriptions feature.

</td></tr><tr><td>

List of roles \(comma-separated\) who can have subscription feature\[glide.knowman.enable\_km\_subscription.roles\]

</td><td>

A comma-separated list of the roles that can use the knowledge subscriptions feature and subscribe to knowledge bases and articles.

</td></tr><tr><td>

List of workflow states \(comma-separated\) that can have subscription feature\[glide.knowman.enable\_km\_subscription.workflow\_state\]

</td><td>

A comma-separated list of the article states for which the knowledge subscription feature is available. The default states include **Draft**, **Review**, and **Published**.

</td></tr></tbody>
</table>3.  Select **Save**.


**Parent Topic:**[Configuring Knowledge Management](../concept/configuring-knowledge-management.md)

