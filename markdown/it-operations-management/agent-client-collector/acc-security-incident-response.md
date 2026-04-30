---
title: Agent Client Collector Security Incident Response
description: Agent Client Collector Security Incident Response \(ACC-SIR\) enables you to automate security incident enrichment data collection and response actions using the Agent Client Collector. This functionality is measured by the Security Operations Security Incident Response \(SIR\).
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector, IT Operations Management]
---

# Agent Client Collector Security Incident Response

Agent Client Collector Security Incident Response \(ACC-SIR\) enables you to automate security incident enrichment data collection and response actions using the Agent Client Collector. This functionality is measured by the Security Operations Security Incident Response \(SIR\).

**Note:** Agent Client Collector Security Incident Response is no longer supported. For details on replacement options, see the [Deprecation guidance for Agent Client Collector Security Incident Response \[KB2249776\] article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2249776) in the Now Support Knowledge Base.

Select from a list of actions \(capabilities\) that come with the base system, to run on security incidents. The Agent Client Collector Security Incident Response functionality uses the `util.command.agent` and `util.osquery.agent` check definitions \(run by Agent Client Collector Spoke\) to run commands and OS queries on security incidents. Capabilities are part of existing system subflows in the Agent Client Collector Security Incident Response integration app. You can also add customized commands and OSquery sql queries to run on the security incidents.

For details on the plugins installed with Security Incident Response, see [Plugins or applications installed with ITOM AIOps](../../it-operations-management/reference/plugin-app-itom-health.md).

-   **[Agent Client Collector Security Incident Response capabilities](../reference/acc-sir-capabilities.md)**  
Agent Client Collector Security Incident Response capabilities that come with the base system are listed on the ACC Capabilities page \(**Agent Client Collector SIR Integration** &gt; **ACC Integration Capabilities**\). These capabilities run on security incidents to gather information about the incident.
-   **[Perform an action on a security incident](../task/acc-perform-sir-action.md)**  
Run an Agent Client Collector Security Incident Response action to gather more information on a security incident. Actions are referred to in the system as **capabilities**, and are configured with the base system.
-   **[Create an Agent Client Collector Security Incident Response command](../task/acc-create-command.md)**  
Define a command or command string to be executed on a machine referenced by a security incident. Commands are listed by operating system. For example, a `ps` command on a Windows OS retrieves the status of active Windows OS processes in the system.
-   **[Run an Agent Client Collector Security Incident Response command](../task/acc-run-commands.md)**  
Run a specified command, on a machine referenced by an incident, to retrieve information on the incident's CI. For example, if you run a `ps` command on an incident, the command retrieves the status of active processes in the system. Commands are listed according to the CI operating system associated with the security incident.
-   **[Create an Agent Client Collector Security Incident Response OSQuery](../task/acc-create-os-query.md)**  
Define an OSQuery to gather information on a security incident's CI. OSQuery provides an SQL layer on top of OS tables, and is bundled together with the Agent Client Collector as part of the base system.
-   **[Run an Agent Client Collector Security Incident Response OSQuery](../task/acc-run-os-query.md)**  
Run an OSQuery on a machine referenced by an incident to retrieve information on each incident's CI. For example, if you run a `select * from system_info` query on an incident, the query gathers all information from the OSQuery **system\_info** table.

**Parent Topic:**[Agent Client Collector](acc-landing-page.md)

