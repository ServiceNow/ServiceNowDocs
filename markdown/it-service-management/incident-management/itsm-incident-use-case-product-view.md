---
title: Applying CSDM guidelines to Incident Management
description: Applying CSDM guidelines to Incident Management connects incidents to services, service offerings, and CIs so that you can see business impact and route incidents to the correct groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/itsm-incident-use-case-product-view.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configuring Incident Management, Incident Management, IT Service Management]
---

# Applying CSDM guidelines to Incident Management

Applying CSDM guidelines to Incident Management connects incidents to services, service offerings, and CIs so that you can see business impact and route incidents to the correct groups.

Features of Incident Management that get the most benefit from the CSDM include:

-   Agent Workspace gives agents the information they need to quickly prioritize and resolve incidents. CSDM-populated CI and service data surfaces business impact context directly on the incident form, reducing time spent gathering context.
-   The major incident workbench provides a single-pane view to identify, track, and resolve high-impact incidents. CSDM service modeling surfaces impacted services and dependent CIs in real time on the workbench.
-   The native mobile app enables agents to quickly view and respond to tasks on the go. CSDM-populated CI data helps keep incident context and service relationships available to agents in the field.
-   Incident deflection encourages self-help by displaying related knowledge base articles. Accurate CI classification in CSDM improves the relevance of article suggestions.
-   Drag-and-drop functionality on the visual task board improves collaboration on incident tasks. CSDM service relationships help route tasks to the correct assignment groups.
-   Performance Analytics provides detailed insights into performance trends. CSDM-aligned service hierarchies enable accurate reporting by business service and service offering.

For more information about CSDM health and data quality, see [Incident Management considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/itsm-incident-use-case-trouble.md).

Incident Management includes a form you can use to report incidents.

\[Omitted image "incident-form.png"\] Alt text: Elements on the Incident form with fields and related list.

The Incident form references the following attributes and related lists.

1.  Service — References the \[cmdb\_ci\_service\] table.
2.  Service Offering \(attribute\) — References the \[service\_offering\] table. Displays the service offerings affected by the incident in the Service Offerings related list.
3.  Configuration Items — References the \[cmdb\_ci\] table.
4.  Affected/Causal CIs — Related list \[task\_ci\] table. You can select application services as CIs on the Incident form.
5.  Impacted Services — Related list \[task\_cmdb\_ci\_service\] table.
6.  Service Offering — Related list \[task\_service\_offering\] table.

-   **[Incident Management and CSDM tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/itsm-incident-use-case.md)**  
Incident Management manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Incident Management.
-   **[Incident Management use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/itsm-incident-use-case-example.md)**  
Incident Management helps restore normal service operation while minimizing impact to your business and maintaining the quality of your data.
-   **[Set up the Incident Management form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/csdm-inc-mgt-form-configure.md)**  
Configure the Incident form to see the impact of an incident and then restore affected services. The CSDM framework enables you to view rich context for incidents: the CIs involved in the incident and the service offerings, business applications, and business services that the incident affects.
-   **[Incident Management considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/itsm-incident-use-case-trouble.md)**  
When you implement the CSDM framework, consider how business applications and application services relate to Incident Management, including when to use an application service on the Incident form.

**Parent Topic:**[Configuring Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/incident-configuration.md)

