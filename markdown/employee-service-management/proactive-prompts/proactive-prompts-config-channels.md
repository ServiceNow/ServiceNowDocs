---
title: Configure delivery channels in Proactive Prompts
description: Configure a channel to display the prompts to end users in their workflow.
locale: en-US
release: xanadu
product: Proactive Prompts
classification: proactive-prompts
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Proactive Prompts, Proactive Prompts, HR Service Delivery, Employee Service Management]
---

# Configure delivery channels in Proactive Prompts

Configure a channel to display the prompts to end users in their workflow.

## Before you begin

Role required: sn\_pp.admin

## Procedure

1.  Navigate to **All** &gt; **Proactive Prompts** &gt; **Signal Channel Configurations**.

2.  Select **New**.

3.  On the form, fill in the fields:

<table id="table_phm_fyz_4vb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the Signal channel configuration.

</td></tr><tr><td>

Application

</td><td>

The scope in which the application is created.

</td></tr><tr><td>

Portal

</td><td>

Option to select Employee Portal as the channel to display the prompts.

</td></tr><tr><td>

Portal action group

</td><td>

The action group applicable to the prompts displayed on the portal.Action groups include some frequently used actions for quick access to the end user. For more information, see [Action groups](../reference/proactive-prompts-actions.md#section_x25_dgg_vvb).

</td></tr><tr><td>

Virtual agent

</td><td>

Option to select Virtual Agent as the channel to display the prompts.

</td></tr><tr><td>

Virtual agent actions

</td><td>

The Virtual Agent actions \(both NLU and LLM type\) from the Signal action \[ \[sn\_pp\_signal\_action\] table that can be performed by the end user. For more information, see [Configure signal actions for Proactive Prompts](proactive-prompts-signal-actions.md).**Note:** A maximum of three NLU based Virtual Agent actions and three LLM based Virtual Agent actions can only be selected for each channel configuration record.

</td></tr></tbody>
</table>4.  Click **Submit**.


