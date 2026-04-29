---
title: Applying CSDM guidelines to Incident Management
description: Incident Management supports the incident management process with the ability to identify and log incidents, classify and prioritize incidents, assign incidents to appropriate users or groups, escalate, resolve, and report incidents. The goal of this product view is to help you to understand how Incident Management key entities work with the core CSDM framework.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Incident Management, Incident Management, IT Service Management]
---

# Applying CSDM guidelines to Incident Management

Incident Management supports the incident management process with the ability to identify and log incidents, classify and prioritize incidents, assign incidents to appropriate users or groups, escalate, resolve, and report incidents. The goal of this product view is to help you to understand how Incident Management key entities work with the core CSDM framework.

Features of Incident Management that get the most benefit from the CSDM include:

-   Agent Workspace gives agents the information they need to quickly prioritize and resolve incidents.
-   The major incident workbench includes a single-pane view you can use to identify, track, and resolve high-impact incidents.
-   The native mobile app allows agents to quickly view and respond to tasks on-the-go, and can approve the requests with a single swipe.
-   Incident deflection encourage self-help by suggesting related knowledge base articles.
-   Improves collaboration on incident tasks by using drag-and-drop functionality on visual task boards.
-   Performance analytics provide detailed insights into performance trends.

Incident Management includes a form you can use to report incidents.

The incident form references the following attributes and related lists.

1.  Service — References the \[cmdb\_ci\_service\] table.
2.  Service Offering \(attribute\) — References the \[service\_offering\] table. Displays the service offerings affected by the incident in the Service Offerings related list.
3.  Configuration Items — References the \[cmdb\_ci\] table
4.  Affected/Causal CIs — Related list \[task\_ci\] table. \(The Incident form allows Application Services to be chosen as CIs\)
5.  Impacted Services — Related list \[task\_cmdb\_ci\_service\] table
6.  Service Offering — Related list \[task\_service\_offering\] table

## For more information

For more details about Incident Management, see [Incident Management](c_IncidentManagement.md).

-   **[Incident Management and CSDM tables](../reference/itsm-incident-use-case.md)**  
Incident Management manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Incident Management.
-   **[Incident Management use case](itsm-incident-use-case-example.md)**  
Incident Management restores normal service operation, while also minimizing impact to your business and maintaining the quality of your data.
-   **[Set up the Incident Management form](../task/csdm-inc-mgt-form-configure.md)**  
Configure the Incident form to see the impact of an incident and then restore affected services. The CSDM framework enables you to view rich context for incidents: the CIs involved in the incident and the service offerings, business applications, and business services that the incident affects.
-   **[Incident Management considerations](itsm-incident-use-case-trouble.md)**  
Consider these points while implementing the CSDM framework.

**Parent Topic:**[Configuring Incident Management](incident-configuration.md)

