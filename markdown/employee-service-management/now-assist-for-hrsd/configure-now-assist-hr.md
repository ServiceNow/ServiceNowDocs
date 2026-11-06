---
title: Configure ServiceNow Otto for HR Service Delivery \(HRSD\)
description: Set up ServiceNow Otto for HRSD by installing plugins, assigning roles, preparing your data, and configuring skills, guardrails, and AI agents so employees can get faster, more accurate HR support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.html
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure ServiceNow Otto for HR Service Delivery \(HRSD\)

Set up ServiceNow Otto for HRSD by installing plugins, assigning roles, preparing your data, and configuring skills, guardrails, and AI agents so employees can get faster, more accurate HR support.

## Configuration overview

1.  [Install AI for HR Service Delivery plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/install-ai-hrsd-plugins.md)

    Install the plugins that provide AI capabilities for HR Service Delivery.

2.  [Assign roles to admins and users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/otto-for-hrsd-roles.md)

    Give the right users the roles they need to access and manage Otto features.

3.  \(Optional\) [Configure the HRSD MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/configure-hrsd-mcp-server.md)

    Set up the HRSD MCP server so external AI clients, like Claude, can connect to HRSD tools.

4.  [Check data readiness](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/check-data-readiness.md)

    Verify that your HR data, such as knowledge articles and cases, is complete and ready before you deploy AI Agents.

5.  [Configure ServiceNow Otto for HRSD skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/customize-nahr-skill.md)

    Turn on the skills your organization needs and adjust their settings.

6.  [Configure sensitivity detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/config-na-sd-filters.md)

    Set the content sensitivity levels and filters that screen the inputs and outputs.

7.  Set up the AI agents and the Galileo plugin that support Otto’s automated tasks.
    -   [Configure HCM AI agents from the HR Service Delivery AI Agent Collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/configure-hcm-agents.md)
    -   [Configure HR AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/configure-voice-agents.md)
    -   [Configure ServiceNow Otto for HRSD – Galileo Inside](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/configuring-galileo-inside.md)

-   **[Install AI for HR Service Delivery plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/install-ai-hrsd-plugins.md)**  
Install the plugins that provide AI capabilities for HR Service Delivery.
-   **[Check data readiness](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/check-data-readiness.md)**  
Review a snapshot of your HR data health to find gaps before you deploy AI agents. The HR Data Readiness Dashboard scores 32 metrics across six readiness areas. Each metric is flagged red, yellow, or green. Use the results to decide what to fix before you configure AI agents.
-   **[Configure ServiceNow Otto for HRSD skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/customize-nahr-skill.md)**  
Learn which AI skills are auto-activated and which require you to activate and configure. Alternatively, you can duplicate a generative AI skill to experiment with skill settings and configure the skill to fit your business needs.
-   **[Configure sensitivity detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/config-na-sd-filters.md)**  
Configure sensitivity detection in the ServiceNow Otto for HR Service Delivery \(HRSD\) application.
-   **[HRSD MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/hrsd-mcp-server.md)**  
The HRSD MCP Server allows HR agents and employees to securely access Case and Knowledge Management features through AI applications like Claude.
-   **[Configure Gen AI Virtual Agent for HRSD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/use-genai-ec.md)**  
Requesters can use a conversational, generative AI experience to submit catalog item requests in Virtual Agent. This streamlined experience increases self-service and reduces operating costs.
-   **[Configure the ServiceNow Otto for HRSD Virtual Agent topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/config-va-topics.md)**  
Enable employees to place requests to the Human Capital Management \(HCM\) system using the ServiceNow Otto for HRSD Virtual Agent topics in Employee Center.
-   **[Configure HCM AI agents from the HR Service Delivery AI Agent Collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/configure-hcm-agents.md)**  
Enable employees to place requests to the Human Capital Management \(HCM\) system using the ServiceNow Otto for HR Service Delivery \(HRSD\) agent collection.
-   **[Configure HR AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/configure-voice-agents.md)**  
Enable employees to complete tasks, resolve issues, and access information through a conversational experience.
-   **[Configuring the Now Assist Context Menu for HR Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/customize-now-context-hrsd.md)**  
Customize a Now Assist skill so that agents can use the generative AI skills in HR Agent Workspace and Core UI.
-   **[Configure ServiceNow Otto for HRSD – Galileo Inside](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/configuring-galileo-inside.md)**  
Enable users to access functionality and benefits of the ServiceNow Otto for HRSD – Galileo Inside \[sn\_hr\_na\_galileo\] plugin by completing a short installation and configuration process.
-   **[RCA approvals for ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/run-rca-now-assist-hrsd.md)**  
After you install ServiceNow Otto for HR Service Delivery \(HRSD\), you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request.

**Parent Topic:**[ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/now-assist-hrsd.md)

