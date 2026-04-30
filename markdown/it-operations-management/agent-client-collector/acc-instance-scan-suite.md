---
title: Agent Client Collector health instance scan suite
description: The Agent Client Collector \(ACC\) health instance scan suite consists of checks that detect anomalies and other issues that might occur on your instance.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector health instance scan suite

The Agent Client Collector \(ACC\) health instance scan suite consists of checks that detect anomalies and other issues that might occur on your instance.

The Agent Client Collector \(ACC\) health instance scan suite consists of the checks in the following table.

<table id="table_els_lpf_cbc"><thead><tr><th>

Check name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ACC duplicate agent for host CI

</td><td>

Checks and reports configuration items \(CIs\) that are associated with multiple active agents, which could indicate imprecise CI identification.When working on an instance associated with the xanadu release or earlier, you must import the `global.ACCInstanceScanUtil` to enable running this check.

</td></tr><tr><td>

ACC find modified script includes

</td><td>

Reports Agent Client Collector Framework script includes that might have been modified. Because these files might have been modified after the last upgrade, the Agent Client Collector \(ACC\) health instance scan suite detects changes that weren’t detected by the regular check.When working on an instance associated with the xanadu release or earlier, you must import the `global.ACCInstanceScanUtil` to enable running this check.

</td></tr><tr><td>

ACC skipped upgrades

</td><td>

Reports skipped updates since the last upgrade.When working on an instance associated with the xanadu release or earlier, you must import the `global.ACCInstanceScanUtil` to enable running this check.

</td></tr><tr><td>

ACC verify plugin folder hierarchy

</td><td>

Validates that the ACC Plugin folders were created correctly and flags duplicate folders that might cause assets to synchronize incorrectly.

</td></tr><tr><td>

ACC active policies count

</td><td>

Counts the number of active published policies. If the number is above 300, the check warns about adverse performance and suggests consolidating policies, where possible.

</td></tr><tr><td>

ACC agent to MID Connection

</td><td>

Connects 1000 agents for every 1-GB Java Virtual Machine \(JVM\). This check verifies whether a MID Server is overloaded. If so, either add an additional JVM or disperse the agents to other MID Servers.

</td></tr><tr><td>

ACC verify sn\_agent CI counts match

</td><td>

Verifies that the number of records in the sn\_agent\_ci\_extended\_info table match the number of records in the sn\_agent\_cmdb\_ci\_agent table. Both tables contain the data for a single agent.

</td></tr></tbody>
</table>For details on importing the `global.ACCInstanceScanUtil` script include, see the [Script Include ACCInstanceScanUtil \[KB1630132\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1630132) article in the Now Support Knowledge Base.

For details on instance scans, see [Instance Scan](https://www.servicenow.com/docs/access?context=hs-landing-page&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

For details on executing the Agent Client Collector health instance scan suite, see [Execute a suite scan](https://www.servicenow.com/docs/access?context=hc-execute-suite-scan&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

