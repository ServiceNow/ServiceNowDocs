---
title: Configure inbound decisions in ServiceNow instance
description: Specify events in your Slack spoke application for which actions must be performed in ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up Slack spoke, Slack Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Configure inbound decisions in ServiceNow instance

Specify events in your Slack spoke application for which actions must be performed in ServiceNow instance.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Slack** &gt; **Inbound Decisions**.

2.  Click **New**.

3.  On the Decision form, fill these values.

<table id="table_khv_ww4_3mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Name to identify the inbound decision.

</td></tr><tr><td>

Answer

</td><td>

Subflow that must be triggered when the specified conditions are met.

</td></tr><tr><td>

Default Answer

</td><td>

Option to specify if this is the default answer. The default answer is applicable when the conditions are not met.1.  Click the lookup icon \(![Lookup icon](../image/SearchIcon.png)\).
2.  Select the required subflow from the Document list.

**Note:** Ensure that the **Table name** is `Flow [sys_hub_flow]`.

</td></tr><tr><td>

Condition

</td><td>

Conditions to be met in your Slack application for which actions must be performed in ServiceNow instance. For updating relevant record in your ServiceNow instance, specify the **Action ID** value you had provided while [configuring outbound configurations](conf-outbound-slack.md) in the condition.

**Note:** **Action ID** of the outbound configuration must be used in the relevant inbound decision to complete the flow. For example, **Action ID** of the Approval Message outbound configuration is provided in the Approval Decision inbound decision. This ensures that upon the request approval or rejection, update is made to the relevant record in your ServiceNow instance.

</td></tr></tbody>
</table>4.  Click **Submit**.

    When events meet conditions specified in the policy, the associated subflow is triggered.

    **Note:** These inbound decisions are saved in the Decision tables. Users are cautioned against directly updating or modifying data in these tables.

    If you want to display modals in Slack, see [Configure Slack modals in ServiceNow instance](conf-slack-modals.md).


