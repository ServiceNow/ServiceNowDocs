---
title: Agent Client Collector upgrade overview
description: The Agent Client Collector Framework manages agent upgrades directly from the instance, with no manual action required on individual agent hosts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/acc-agent-upgrade-overview.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-05-28"
reading_time_minutes: 5
keywords: [ACC agent upgrade, auto-upgrade, agent upgrade overview]
breadcrumb: [ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector upgrade overview

The Agent Client Collector Framework manages agent upgrades directly from the instance, with no manual action required on individual agent hosts.

You can upgrade Agent Client Collector agents one at a time through the UI, or upgrade all eligible agents at once using the auto-upgrade feature. After an upgrade starts, each agent downloads the new version, installs it, restarts, and reports the result back to the instance.

## Before you upgrade

Configure the Agent Client Collector web server. For details, see [Configure the websocket server on the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-configure-web-server.md).

Ensure that the MID Server, MID Web Server, and the MID Server websocket server are running.

Roles required: agent\_client\_collector\_admin

-   In a Windows environment: Local SYSTEM account
-   In a Linux environment: sudo rpm/dpkg
-   In a macOS environment: sudo pkg

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


For details on the required properties for agent overview, see [Agent Client Collector upgrade properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-agent-upgrade-properties.md).

High-volume upgrade does not support Agent Client Collector to MID Server communication via mTLS.

When performing high-volume upgrade, all agents that aren't using the most up-to-date version are upgraded. No upgrade is performed on agents already using the upgraded version.

No upgrade is performed on agents that are outside the application scope. For more information, see [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationScope.md).

An agent is excluded from high-volume upgrade when you reach the failed upgrade limit for an agent. The failed upgrade limit is specified in the **sn\_agent.auto\_upgrade.retry\_limit** system property. The default value for this property is 3.

-   This property applies to both high-volume and selective upgrades that have failed.
-   When an agent reaches the failed upgrade limit, an Agent Client Collector administrator can still run selective upgrade on the agent.
-   You can manually reset the failed upgrade limit by selecting the **Reset failed upgrade attempts** option on the agent page \(select **All** &gt; **Agent Client Collector** &gt; **Agents** and select an agent\).
-   After a successful upgrade, the upgraded agent is considered to have zero failed upgrades \(for future upgrades\).

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
-   If the MID Server is unavailable, agents fall back to the Install Server at `https://install.service-now.com`. To enable agent fallback, modify the base system checks to specify the install server as the download path. `runUpgrade.rb --path=auto`

If your agents use a custom download server, configure the **agent-upgrade-url-path** key in the agent's `acc.yml` file. This setting takes priority over the default sources.

## Rollout strategy

Use a phased approach to reduce risk when upgrading a large agent fleet:

1.  Upgrade one agent from the UI to confirm the process works end-to-end.
2.  Upgrade 5–10 agents from the list view, selecting agents across different operating systems.
3.  Perform a full rollout by enabling the scheduled job or running the background script.

-   **[Upgrade an agent in an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/upgrade-agent-from-instance.md)**  
Perform selective self-upgrade instead of bulk upgrade for enhanced efficiency when working with agents that are difficult to access, such as agents deployed in the cloud. You can perform selective upgrade on up to 50 agents at a time.
-   **[Upgrade multiple agents in an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/upgrade-multiple-agents-from-instance.md)**  
When performing selective upgrade of an agent in an instance, you can select multiple instances to upgrade at once.
-   **[Run a mass upgrade via the scheduled Agent Client Collector upgrade job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/enable-agent-upgrade-scheduled-job.md)**  
Activate the built-in scheduled job to upgrade all eligible Agent Client Collector agents automatically in rate-limited batches.
-   **[Run a mass Agent Client Collector upgrade using a background script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/run-agent-mass-upgrade-script.md)**  
Trigger an immediate upgrade of all eligible Agent Client Collector agents without waiting for the next scheduled job run.
-   **[Repeat high-volume upgrade for failed agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/repeat-upgrade.md)**  
If high-volume upgrade fails for specific agents, you must clear the problematic agents' history to re-enable upgrade. If the target upgrade version changes, you don't need to clear the agents' history, as the agents upgrade with the next scheduled high-volume upgrade.
-   **[Configure proxies when performing MID-less upgrade using a CDN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/cdn-upgrade-proxies.md)**  
Create proxies for added security when upgrading MID-less agents via a Content Delivery Network \(CDN\). You add proxy servers to the sn\_agent\_proxy table on the ServiceNow instance.
-   **[Configure a download proxy for Agent Client Collector upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/configure-agent-upgrade-proxy.md)**  
Add a proxy server entry so that agents behind a corporate proxy can download upgrade packages from the ServiceNow Content Delivery Network \(CDN\).

**Parent Topic:**[Deploying Agent Client Collector on servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-server-deployment.md)

