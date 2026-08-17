---
title: Use generative AI in ServiceNow Otto for ITOM
description: Use the ServiceNow ServiceNow Otto for ITOM application to view alert or incident analyses using generative AI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-use.html
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [generative AI for IT Operations Management, generative AI for ITOM, alert analysis]
breadcrumb: [ServiceNow Otto for ITOM, IT Operations Management]
---

# Use generative AI in ServiceNow Otto for ITOM

Use the ServiceNow® ServiceNow Otto for ITOM application to view alert or incident analyses using generative AI.

Alert analyses include human-readable briefs of the alert and additional technical information to help you investigate the alert more effectively. The analyses are provided in English, irrespective of the language used in the alert description.

For more information about the ServiceNow Otto for IT Operations Management \(ITOM\) application, see [ServiceNow Otto for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom.md).

**Important:** Some generative AI skills, AI agents, and agentic workflows are turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Domain separation and generative AI

By default, all skills exist in the global domain. When you use AI in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, AI only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/next-experience-pickers.md).\)

## Documentation in this section

See the following documentation to learn more about using ServiceNow Otto for ITOM skills.

-   **[View an alert analysis by ServiceNow Otto in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/alert-summarization-now-assist.md)**  
View an alert analysis by ServiceNow Otto for an alert on the alert's Overview tab in the Service Operations Workspace. Alert analyses include a human-readable brief of the alert and technical information to help you investigate the alert more effectively.
-   **[View an alert analysis by ServiceNow Otto in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/alert-summary-now-assist-express-list.md)**  
View an alert analysis created using generative AI. Alert analyses include a human-readable brief of the alert and technical information to help you investigate the alert more effectively.
-   **[View an alert group analysis by ServiceNow Otto in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/alert-group-analysis-el.md)**  
View an alert group analysis created using generative AI. The analysis offers a simplified, human-readable description of the alert group and technical information to help you investigate it more efficiently.
-   **[View an error analysis by Now Assist in Agent Client Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/agent-errors-now-assist.md)**  
View an error analysis created by Now Assist using generative AI. Error analyses enable asking questions on a specific agent's error or error code.
-   **[Save the by ServiceNow Otto alert analysis summary as alert group description](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/alert-group-descr-now-assist-el.md)**  
Save the human-readable summary generated by ServiceNow Otto in the Alert analysis as the description of an alert group.
-   **[Generate an alert group description in Express List using ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/alert-group-descr-generate-el.md)**  
Use AI to generate a meaningful description of an alert group in Express List that encompasses all the alerts within the group. The generated description replaces the original description of the group.
-   **[Launch an alert analysis from the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/alert-analysis-now-assist-panel.md)**  
Initiate an alert analysis from the ServiceNow Otto panel. The alert analysis displays directly in the panel for convenient review.
-   **[Create an incident from an alert with ServiceNow Otto in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/create-incident-now-assist-el.md)**  
Create an incident with a human-readable, AI-generated description from the Express List pane by using ServiceNow Otto.
-   **[Speed up alert resolution with a ServiceNow Otto analysis of past related incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/nai-past-incidents.md)**  
Use AI to investigate relevant past incidents and present effective strategies used to resolve them.
-   **[Analyze a dashboard in Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/analyze-a-dashboard-in-service-observability.md)**  
Use the analyze Service Observability dashboard skill to view an analysis of a single Service Observability dashboard.
-   **[Analyze service health in Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/analyze-service-health-in-service-observability.md)**  
Use the Analyze Service Health skill to view an analysis of all Service Observability dashboards for the selected service.

**Parent Topic:**[ServiceNow Otto for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom.md)

