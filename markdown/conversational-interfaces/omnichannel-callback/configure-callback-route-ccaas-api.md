---
title: Configure callback routing
description: Configure callback requests to route them to the external CCaaS providers using Callback Actions API.
locale: en-US
release: zurich
product: Omnichannel Callback
classification: omnichannel-callback
topic_type: task
last_updated: "2026-01-13"
reading_time_minutes: 1
breadcrumb: [Configuring Omnichannel Callback, Omnichannel Callback, Manage people and work, Conversational Interfaces]
---

# Configure callback routing

Configure callback requests to route them to the external CCaaS providers using Callback Actions API.

## About this task

To send callback requests to the external CCaaS providers, you have to define routing rules in the **Callback routing configuration** table. While defining it, you can control when to apply routing, which group it is going to affect, and what subflow to use to process the outbound request.

## Before you begin

Ensure that you have copied the External Callback Operations template in Subflows. To learn more, see [Copy subflow template for callback routing](configure-callback-route-copy-subflow-template.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **sys\_cs\_callback\_routing\_config.LIST**.

2.  On the Callback routing configuration table, select **New** and fill in the details.

<table id="table_c55_g33_yhc"><thead><tr><th>

Fields

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Source Table

</td><td>

Table from which the callback request originates. For example:-   Portal
-   Engagement center module
-   Embeddable core module


</td></tr><tr><td>

Source ID

</td><td>

Specific record in the source table, the routing configuration applies to.

</td></tr><tr><td>

Apply to groups

</td><td>

Groups for which the routing configuration is applied.

</td></tr><tr><td>

Order

</td><td>

Determines the sequence in which the routing rules are evaluated.

</td></tr><tr><td>

Third Party Subflow ID

</td><td>

The external callback operations template that you've copied in Subflows to integrate with third-party CCaaS providers.

</td></tr></tbody>
</table>3.  Select **Submit**.


