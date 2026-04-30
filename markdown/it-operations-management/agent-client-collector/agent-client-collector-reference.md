---
title: Agent Client Collector Framework reference
description: Reference topics provide additional information about mapping and fine-tuning application services using Agent Client Collector Framework lists and forms.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector, IT Operations Management]
---

# Agent Client Collector Framework reference

Reference topics provide additional information about mapping and fine-tuning application services using Agent Client Collector Framework lists and forms.

-   **[Agent Client Collector user roles](acc-users.md)**  
Administrators can assign user roles to grant access to the Agent Client Collector. The following standard roles for the Agent Client Collector Framework \(ACC-F\) are included in the ServiceNow system with the Agent Client Collector installed on it.
-   **[Agent Client Collector Framework default checks](acc-framework-checks-policies.md)**  
Agent Client Collector Framework provides default checks with the base system.
-   **[Agent Client Collector performance and footprint for URL monitoring](acc-footprint-url-monitoring.md)**  
The following tables display the agent performance KPIs and its footprint on the host during URL monitoring data collection execution on different operation systems.
-   **[Agent Client Collector certificate revocation reasons](certificate-revocation-reasons.md)**  
The following table lists and describes the possible reasons for revoking an Agent Client Collector certificate to stop communication between the agent and ITOM cloud services.
-   **[Agent Client Collector check definition page](check-definition-form.md)**  
The fields to be configured on the Check Definition page, when creating a check definition.
-   **[Agent Client Collector data collection properties](acc-data-collection-properties.md)**  
Description of the properties that determine the behavior of Agent Client Collector data collection.
-   **[Agent Client Collector policy collection properties](acc-policy-collection-properties.md)**  
Description of the properties that determine the behavior of Agent Client Collector policy collection.
-   **[Agent Client Collector Framework configuration properties](acc-framework-configuration-properties.md)**  
Description of the properties that determine the behavior of Agent Client Collector Framework configuration.
-   **[Agent Client Collector data collection tables](acc-data-collection.md)**  
Agent Client Collector performs data collection based on the scoped apps that you've installed. Agent Client Collector Framework performs basic data collection, and Agent Client Collector for Visibility - Content performs enhanced data collection.
-   **[Account commands for LocalService, LocalSystem, and gMSA during Windows installation](gmsa-and-local-account-commands.md)**  
When installing an agent on a Windows host using a LocalService, LocalSystem, or gMSA account, you must run msi commands to enable the accounts.
-   **[Verify API is associated with a live agent](../task/acc-api-live-agent.md)**  
Call the AgentNowHandler.hasAgent API to determine if the CI is associated with a live agent. The API gets a sys\_id of the CI and returns a true/false result.
-   **[Configuration file options](acc-yml-options.md)**  
Options available in the `acc.yml` configuration file.
-   **[Synchronization properties for validating Agent Client Collector plugins](plugin-validation-reference.md)**  
Use the following properties when synchronizing public certificates from the MID Server to the Agent Client Collector.
-   **[Agent Client Collector statuses](agent-statuses.md)**  
The following table lists and describes the Agent Client Collector statuses.
-   **[Agent Client Collector log levels](acc-logs-reference.md)**  
The following table displays the available log levels which indicate the severity of Agent Client Collector events.
-   **[Agent Client Collector log rotation parameters](acc-log-rotation-reference.md)**  
If Agent Client Collector logs get too large, they can drain system resources. To ensure system efficiency, configure parameters in the `acc.yml` file by which to rotate logs out of the system's storage \(Windows default location = `C:\ProgramData\ServiceNow\agent-client-collector\config\acc.yml`. Linux default location = `/etc/servicenow/agent-client-collector/acc.yml`\).
-   **[Agent Client Collector CPU protection thresholds](acc-set-silent-reference.md)**  
When an agent meets the configured thresholds specified in the agent's `acc.yml` file, it enters CPU protection mode, either for an individual check or for all checks. Agents in CPU protection mode appear in the agent logs with the syntax `Agent Protection`.

**Parent Topic:**[Agent Client Collector](../concept/acc-landing-page.md)

