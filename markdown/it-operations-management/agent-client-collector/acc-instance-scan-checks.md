---
title: Agent Client Collector health instance scan checks
description: The Agent Client Collector \(ACC\) health instance scan suite includes checks that detect anomalies and issues on your instance. Use this reference to identify what each check does and when it applies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/acc-instance-scan-checks.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 2
keywords: [ACC health instance scan, agent client collector scan checks, ACC instance scan suite]
breadcrumb: [ACC health instance scan suite, ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector health instance scan checks

The Agent Client Collector \(ACC\) health instance scan suite includes checks that detect anomalies and issues on your instance. Use this reference to identify what each check does and when it applies.

<table id="table_acc_scan_checks"><thead><tr><th>

Check name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ACC duplicate agent for host CI

</td><td>

Identifies configuration items \(CIs\) associated with multiple active agents, indicating potential issues with CI identification.

</td></tr><tr><td>

ACC Error Framework

</td><td>

Verifies whether the ACCErrorManager has been created, which enables associating errors to the relevant ACC scoped app.Detects whether an automation source application, automation error category, and automation error code exist for the Agent Client Collector Framework application.

</td></tr><tr><td>

ACC find modified script includes

</td><td>

Detects modified Agent Client Collector Framework script includes that might have been altered post-upgrade.

</td></tr><tr><td>

ACC skipped upgrades

</td><td>

Reports upgrades that were skipped since the last upgrade.**Note:** Skipped upgrades don't generate an error message.

</td></tr><tr><td>

ACC verify plugin folder hierarchy

</td><td>

Validates the correct creation of ACC Plugin folders and flags duplicate folders that may cause synchronization issues.

</td></tr><tr><td>

ACC active policies count

</td><td>

Counts the number of active published policies. If the number exceeds 300, consolidate the policy to improve performance.

</td></tr><tr><td>

ACC agent to MID Connection

</td><td>

Verifies the connection of 1000 agents per 1-GB Java Virtual Machine \(JVM\) to confirm the MID Server isn't overloaded. If overloaded, configure additional JVMs or redistribute agents to other MID Servers.

</td></tr><tr><td>

ACC verify sn\_agent CI counts match

</td><td>

Confirms that the records in the sn\_agent\_ci\_extended\_info and sn\_agent\_cmdb\_ci\_agent tables match, verifying data consistency for agents.

</td></tr><tr><td>

ACC ICS Diagnostics Tool

</td><td>

Analyzes the ServiceNow instance and its setup with ITOM Cloud Services.

</td></tr><tr><td>

ACC automation\_error\_msg cleaner

</td><td>

Verifies that the Agent Issues table cleaner exists and is enabled, ensuring ACC-specific error records are regularly cleaned up and the table remains manageable.

</td></tr><tr><td>

ACC Verify global.ACCInstanceScanUtil exists

</td><td>

Detects that the `global.ACCInstanceScanUtil` file is installed for instances starting with the Xanadu release or later. Without this file, several ACC Health Instance Scan checks don't run.

</td></tr></tbody>
</table>## Additional information

For details on importing the `global.ACCInstanceScanUtil` script include, see the [Script Include ACCInstanceScanUtil \[KB1630132\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1630132) article in the HI Knowledge Base.

For details on running the ACC health instance scan, see [Run the Agent Client Collector \(ACC\) health instance scan as a scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-instance-scan-run.md).

**Parent Topic:**[Agent Client Collector health instance scan suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-instance-scan-suite.md)

