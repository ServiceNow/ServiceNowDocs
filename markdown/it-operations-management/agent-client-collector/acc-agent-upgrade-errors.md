---
title: Agent Client Collector upgrade error codes
description: Error codes generated during Agent Client Collector upgrades, with descriptions and resolution steps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/acc-agent-upgrade-errors.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-05-28"
reading_time_minutes: 2
keywords: [ACC upgrade errors, ACC-5005, ACC-5006, ACC-5017]
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector upgrade error codes

Error codes generated during Agent Client Collector upgrades, with descriptions and resolution steps.

Upgrade errors appear in **All** &gt; **Agent Client Collector** &gt; **ACC Errors**. Filter by error codes starting with `ACC-50` to see upgrade-specific issues. Additional detail is available in the **Message** column of the Agent Upgrade Histories table. For supported platforms, see [Supported platforms for Agent Client Collector auto-upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-agent-upgrade-platforms.md).

<table id="table_upgrade_errors"><thead><tr><th>

Error code

</th><th>

Description

</th><th>

Resolution

</th></tr></thead><tbody><tr><td>

ACC-5005

</td><td>

Agent operating system is not supported for auto-upgrade.

</td><td>

The agent can't be auto-upgraded. Manually install the new version on the agent host. For supported platforms, see [Supported platforms for Agent Client Collector auto-upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-agent-upgrade-platforms.md).

</td></tr><tr><td>

ACC-5006

</td><td>

Agent version is earlier than the minimum required for auto-upgrade \(2.7.0\).

</td><td>

Manually upgrade the agent to version 2.7.0 or higher, then retry.

</td></tr><tr><td>

ACC-5007

</td><td>

Agent is not in **Up** status.

</td><td>

Wait for the agent to reconnect. If the agent remains down, investigate connectivity issues on the agent host.

</td></tr><tr><td>

ACC-5013

</td><td>

Agent-side validation failed \(AgentVerification stage\).

</td><td>

Check the `acc.log` file on the agent host. Common causes include insufficient permissions, low disk space, and missing dependencies.

</td></tr><tr><td>

ACC-5015

</td><td>

MID Server is not in **Up** status.

</td><td>

Restore the MID Server that this agent connects through, then retry the upgrade.

</td></tr><tr><td>

ACC-5016

</td><td>

Upgrade timed out. The agent did not complete the upgrade within the allowed time.

</td><td>

Connect to the agent host and check whether the agent service is running. Review the upgrade log: -   Linux and macOS: `{AGENT_LOG_DIR}/servicenow/agent-client-collector/upgrade.log`
-   Windows: `%TEMP%\ACC_Logs\ACC_Upgrade.log`

If the service is running but the status did not update, restart the agent service.

</td></tr><tr><td>

ACC-5017

</td><td>

Agent has exceeded the maximum retry limit for failed upgrades.

</td><td>

1.  Investigate the root cause in the agent logs.
2.  After resolving the issue, open the agent record and navigate to the related Agent Extended Info record.
3.  Set `failed_upgrade_attempts` to `0` and save.
4.  Navigate to ACC Errors and resolve the ACC-5017 error for this agent.
5.  The agent is picked up in the next scheduled upgrade run.

</td></tr><tr><td>

ACC-5018

</td><td>

Target upgrade version is invalid.

</td><td>

Check the **sn\_agent.agent\_upgrade\_version** property. The value must be a valid version number, for example `5.0.1`.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Framework reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/agent-client-collector-reference.md)

