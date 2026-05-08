---
title: Agent Client Collector health instance scan suite
description: The Agent Client Collector \(ACC\) health instance scan suite consists of checks that detect anomalies and other issues that might occur on your instance. These checks are designed to ensure the overall health and performance of the ACC, proactively identifying potential problems before they impact system operations.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector health instance scan suite

The Agent Client Collector \(ACC\) health instance scan suite consists of checks that detect anomalies and other issues that might occur on your instance. These checks are designed to ensure the overall health and performance of the ACC, proactively identifying potential problems before they impact system operations.

The ACC health instance scan suite consists of the following checks.

<table id="table_qzb_bj3_12c"><thead><tr><th>

Check name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ACC duplicate agent for host CI

</td><td>

Identifies configuration items \(CIs\) associated with multiple active agents, indicating potential issues with CI identification.Requires importing the `global.ACCInstanceScanUtil` for instances associated with the Xanadu release or earlier.

</td></tr><tr><td>

ACC Error Framework

</td><td>

Verifies whether the ACCErrorManager has been created, which enables associating errors to the relevant ACC scoped app. Detects whether an automation source application, automation error category, and automation error code exist for the Agent Client Collector Framework application.

</td></tr><tr><td>

ACC find modified script includes

</td><td>

Detects modified Agent Client Collector Framework script includes that might have been altered post-upgrade.Requires importing the `global.ACCInstanceScanUtil` for instances associated with the Xanadu release or earlier.

</td></tr><tr><td>

ACC skipped upgrades

</td><td>

Reports upgrades that were skipped since the last upgrade.Requires importing the `global.ACCInstanceScanUtil` for instances associated with the Xanadu release or earlier.

</td></tr><tr><td>

ACC verify plugin folder hierarchy

</td><td>

Validates the correct creation of ACC Plugin folders and flags duplicate folders that may cause synchronization issues.

</td></tr><tr><td>

ACC active policies count

</td><td>

Counts the number of active published policies, and if the number is above 300, recommends policy consolidation to improve performance.

</td></tr><tr><td>

ACC agent to MID Connection

</td><td>

Verifies the connection of 1000 agents per 1-GB Java Virtual Machine \(JVM\) to ensure the MID Server isn't overloaded. If overloaded, configure additional JVMs or redistribute agents to other MID Servers.

</td></tr><tr><td>

ACC verify sn\_agent CI counts match

</td><td>

Ensures the records in the sn\_agent\_ci\_extended\_info and sn\_agent\_cmdb\_ci\_agent tables match, confirming data consistency for agents.

</td></tr></tbody>
</table>For details on importing the `global.ACCInstanceScanUtil` script include, see the [Script Include ACCInstanceScanUtil \[KB1630132\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1630132) article in the Now Support Knowledge Base.

For details on instance scans, see Instance Scan.

For details on executing the Agent Client Collector health instance scan suite, see Execute a suite scan.

**Parent Topic:**[Deploying Agent Client Collector on both servers and endpoints](acc-shared-deployment.md)

