---
title: Deploying Agent Client Collector on servers
description: When deploying the Agent Client Collector, perform deployment and management tasks on your environment's servers.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Deploying Agent Client Collector on servers

When deploying the Agent Client Collector, perform deployment and management tasks on your environment's servers.

Server deployment uses MID Servers to connect your agents to a ServiceNow instance. Agents deployed on data center servers open WebSocket connections to your MID Servers, which relay data to your instance. You manage the sizing, certificates, and load balancing of the MID Server.

Use server deployment when your agents are in controlled environments such as data centers, where you are already running MID Servers and want to keep traffic on your network. Agent Client Collector Monitoring \(ACC-M\) and Agent Client Collector Log Analytics \(ACC-L\) require server deployment, and you can deploy Agent Client Collector for Visibility - Content \(ACC-VC\) with servers as well.

-   **[Configuring Agent Client Collector with a MID Server](acc-configuring-with-mid.md)**  
Configure the Agent Client Collector with a MID Server to enable communication between network servers and the ServiceNow instance.
-   **[Agent Client Collector installation on a Linux OS system](acc-install-linux-concept.md)**  
Install Agent Client Collector on a system that uses a Linux OS, either using a single-line command script, or following the installation procedure to embed in your own package distribution mechanism. The installation procedure provides consistency when using package distribution solutions.
-   **[Agent Client Collector installation on a Windows machine](acc-windows-install-concept.md)**  
When installing the Agent Client Collector on a Windows machine, either download an installation file and use a wizard to install the agent manually, or use silent installation to automate agent installation and configuration. Manual installation enables you to test the agent on a single system, while silent installation enables you to deploy the agent at scale.
-   **[Create and edit Agent Client Collector plugins](../task/create-edit-assets.md)**  
You can edit the default plugins, or you can add new plugins, as needed. Creating and editing plugins customizes the Agent Client Collector monitoring capabilities.
-   **[Optimize distribution of agents to MID Servers](../task/acc-redistribute-agents-mid.md)**  
Optimize the distribution of agents by allowing redistribution from one MID Server to another. Agents will always be connected to the MID Server with the fastest response time.
-   **[View the Agent Client Collector configuration file for an agent](../task/acc-yml-view.md)**  
View the `acc.yml` Agent Client Collector configuration file without having to access the host server by retrieving the file from an agent.
-   **[Create an Agent Client Collector configuration data file](../task/create-acc-config-data-file.md)**  
Create an Agent Client Collector configuration data file and associate it with check definitions so that you can view the information about your instance. You can also add or delete an attachment to the configuration data files, which are used by check definitions during check executions.
-   **[Validate plugins on the MID Server](../task/validate-assets-mid-server.md)**  
Validate plugins on your MID Server to ensure that they match the plugins on your ServiceNow instance. Validating plugins ensures that the instance provides accurate data on all of your MID Server plugins.
-   **[Validate plugins on agents](../task/validate-assets-agents.md)**  
Validate plugins on your agents to ensure that they match the plugins on your ServiceNow instance. Validating plugins ensures that the instance provides accurate data on all of your agents' plugins.
-   **[Using proxy agents in Agent Client Collector](proxy-agent.md)**  
You can use a proxy agent to monitor the health and performance of your configuration items \(CIs\) even if the agent is in the cloud or any place that is external to your host server.
-   **[Enable log monitoring in a Linux environment](../task/acc-enable-log-monitoring-linux.md)**  
To enable monitoring logs in a Linux environment, select the relevant policy and assign specific check parameters to the policy. When log monitoring is enabled and a specified string is discovered in the log being monitored, the system creates an event.
-   **[Enable log monitoring in a Windows environment](../task/acc-enable-log-monitoring-windows.md)**  
To enable monitoring logs in a Windows environment, select the relevant policy and assign specific check parameters to the policy. When log monitoring is enabled and a specified string is discovered in the log being monitored, the system creates an event.
-   **[Select the Azure policies to activate for metric collection](../task/select-policies-azure.md)**  
Activate the Azure policies that come with the Agent Client Collector base system so that Azure virtual machines can collect metrics. These metrics help you monitor the configuration items \(CIs\) in the CMDB.
-   **[Use the Agent Client Collector Health Dashboard](../task/acc-health-dashboard.md)**  
The Agent Client Collector Health Dashboard enables you to monitor the status of the agents in your system.
-   **[Agent Client Collector Discovery](acc-discovery.md)**  
Discover CIs in your environment by using Agent Client Collector for Visibility - Content \(ACC-VC\) Discovery. ACC-VC works with both horizontal IP-based Discovery, and you can also use push-based Discovery.
-   **[Agent Client Collector Log Analytics setup](accl-setup.md)**  
Configure Agent Client Collector Log Analytics on your ServiceNow instance either with or without using guided setup.
-   **[Collect web usage data using Agent Client Collector for Visibility - Content](../task/collect-web-data-usage-accvc.md)**  
Track website visits across your organization and gain visibility into web applications your users access using Agent Client Collector for Visibility - Content \(ACC-VC\).

**Parent Topic:**[Agent Client Collector](acc-landing-page.md)

