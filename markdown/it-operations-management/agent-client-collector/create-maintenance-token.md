---
title: Create a maintenance token
description: Create a maintenance token to use when uninstalling an agent from a Windows device. Administrators require maintenance tokens to ensure that unauthorized employees can't perform an uninstall.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/create-maintenance-token.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 1
breadcrumb: [ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Create a maintenance token

Create a maintenance token to use when uninstalling an agent from a Windows device. Administrators require maintenance tokens to ensure that unauthorized employees can't perform an uninstall.

## Before you begin

Role required: sn\_agent.token\_admin

## About this task

Maintenance tokens are short-lived by design. The default expiration is after 30 minutes. To modify the expiration time:

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.
2.  Select **New**.
3.  Configure the following values for the token's expiration time:

    |Field|Value|
    |-----|-----|
    |Name|**sn\_agent.maintenance\_token.expiry\_minutes**|
    |Type|integer|
    |Value|&lt;the amount of time, in minutes, before the token expires&gt;|

4.  Select **Submit**.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Maintenance Token**.

2.  Select **New**.

3.  Configure the following values for the token:

<table id="table_ejw_tgq_jkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Alias

</td><td>

Enter a descriptive name for the maintenance token.

</td></tr><tr><td>

Purpose

</td><td>

Select **uninstall**.

</td></tr><tr><td>

Scope

</td><td>

Select the token's scope:-   **global**: Token applies to all agents.
-   **targeted**: Token applies only to selected agents. When selecting this option, the **Agents** field appears.


</td></tr><tr><td>

Agents

</td><td>

Select the **Unlock agents** \(\[Omitted image "unlock-icon-acc.png"\] Alt text: Unlock agents icon\) icon and select the agents for the token to apply to.This field appears only when selecting **targeted** as the token scope.

</td></tr></tbody>
</table>4.  Select the **Activate** check box to activate the token.

5.  Select **Submit**.


## What to do next

Uninstall the agent using the maintenance token, as described in [Uninstall an agent using a maintenance token](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/uninstall-agent-maintenance-token.md).

**Note:** Ensure that you use the maintenance token before it expires.

**Parent Topic:**[Deploying Agent Client Collector on servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-server-deployment.md)

