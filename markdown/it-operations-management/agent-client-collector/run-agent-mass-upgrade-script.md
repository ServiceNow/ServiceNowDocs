---
title: Run a mass Agent Client Collector upgrade using a background script
description: Trigger an immediate upgrade of all eligible Agent Client Collector agents without waiting for the next scheduled job run.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/run-agent-mass-upgrade-script.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-05-28"
reading_time_minutes: 1
keywords: [ACC mass upgrade, background script upgrade, AgentUpgradeUtil]
breadcrumb: [Agent Client Collector upgrade overview, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Run a mass Agent Client Collector upgrade using a background script

Trigger an immediate upgrade of all eligible Agent Client Collector agents without waiting for the next scheduled job run.

## Before you begin

Configure the required upgrade properties before running the script. For details, see [Agent Client Collector upgrade properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-agent-upgrade-properties.md).

Role required: agent\_client\_collector\_admin

## About this task

The background script upgrades agents connected via MID Server and agents connected via Cloud Services \(ICS\) in a single run. Both function calls in the script are required — omitting either skips the corresponding agent group.

The system queries all agents that are **Up**, not duplicated, have a valid MID Server or Pod connection, and have not exceeded the retry limit. Agents with no prior failures are upgraded before agents with prior failures.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scripts - Background**.

2.  Change the application scope to `sn_agent` \(Agent Client Collector\).

3.  Paste the following script into the editor.

    ```
    var duration = 60; // Duration in minutes for rate limiting calculations
    
    var a = new AgentUpgradeUtil();
    a.upgradeAgentsLimitedByMid(duration);  // Upgrades agents connected via MID Servers
    a.upgradeAgentsMidless(duration);       // Upgrades agents connected via Cloud Services
    ```

    Set `duration` to the number of minutes used for rate limiting calculations. The default value of `60` applies the per-hour limits configured in the upgrade properties.

4.  Select **Run script**.

    The system begins upgrading eligible agents immediately, adhering to the rate limits set in the upgrade properties.


**Parent Topic:**[Agent Client Collector upgrade overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-agent-upgrade-overview.md)

