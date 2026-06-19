---
title: Agent Client Collector upgrade overview
description: The Agent Client Collector Framework manages agent upgrades directly from the instance, with no manual action required on individual agent hosts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/acc-agent-upgrade-overview.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-05-28"
reading_time_minutes: 2
keywords: [ACC agent upgrade, auto-upgrade, agent upgrade overview]
breadcrumb: [ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector upgrade overview

The Agent Client Collector Framework manages agent upgrades directly from the instance, with no manual action required on individual agent hosts.

You can upgrade Agent Client Collector agents one at a time through the UI, or upgrade all eligible agents at once using the auto-upgrade feature. After an upgrade starts, each agent downloads the new version, installs it, restarts, and reports the result back to the instance.

## Upgrade methods

Two upgrade methods are available:

-   **Single agent upgrade**

    Upgrade one agent at a time from the agent record in the UI. Use this method to validate the upgrade process before a broader rollout. You can also select multiple agents from the list view to upgrade up to 50 agents at a time.

-   **Mass upgrade**

    Upgrade all eligible agents automatically using the built-in scheduled job or a background script. The scheduled job applies rate limiting to control the rollout pace. The background script also uses rate limiting, and triggers an immediate upgrade without waiting for the next scheduled run.


## Upgrade stages

Both single and mass upgrade attempts, progress through the following stages. Each stage creates a record in the Agent Upgrade Histories table.

-   **InstanceVerification**

    The instance confirms the agent is eligible for upgrade. Checks include operating system support, agent version, agent status, and MID Server connectivity.

-   **AgentVerification**

    The agent confirms it can perform the upgrade. Checks include permissions, available disk space, and dependencies.

-   **Upgrade**

    The agent downloads the package, installs it, and restarts with the new version.


For details on the required properties for agent overview, see [Agent Client Collector upgrade properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-agent-upgrade-properties.md).

## Agent eligibility

An agent is eligible for auto-upgrade when it meets all of the following conditions:

-   Status is **Up**.
-   Version is 2.7.0 or higher and lower than the target upgrade version.
-   Agent is not flagged as a duplicate.
-   Has a valid MID Server or Pod reference.
-   Has not exceeded the retry limit for failed upgrades.
-   Runs on a supported operating system.

## Package download sources

During upgrade, each agent downloads the new package from one of the following sources, depending on its connection type:

-   Agents connected via Cloud Services \(ICS\) download from the ServiceNow CDN at `https://cdn-install.sncapps.service-now.com`.
-   Agents connected via MID Server download from the MID Server directly over the local network.
-   If the MID Server is unavailable, agents fall back to the Install Server at `https://install.service-now.com`. To enable agent fallback, ensure that the install server is specified on the ServiceNow instance.

If your agents use a custom download server, configure the **agent-upgrade-url-path** key in the agent's `acc.yml` file. This setting takes priority over the default sources.

## Rollout strategy

Use a phased approach to reduce risk when upgrading a large agent fleet:

1.  Upgrade one agent from the UI to confirm the process works end-to-end.
2.  Upgrade 5–10 agents from the list view, selecting agents across different operating systems.
3.  Perform a full rollout by enabling the scheduled job or running the background script.

