---
title: Configuring Incident Management
description: You can configure the Incident form and other incident features, such as incident categories and UI behavior. The ITSM guided setup helps you configure Incident Management on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/incident-configuration.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Incident Management, IT Service Management]
---

# Configuring Incident Management

You can configure the Incident form and other incident features, such as incident categories and UI behavior. The ITSM guided setup helps you configure Incident Management on your ServiceNow instance.

## Configuration overview

Configure the Incident form in the base system to follow ITIL general guidelines. The administrator can configure the Incident form and use the form designer to customize it. You can copy or create a child incident to reduce the effort of configuring the functionality of an open incident.

\[Omitted image "config-form-layout.png"\] Alt text: Form layout configuration for the Incident form

|Menu option|Description|
|-----------|-----------|
|[Form design](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_FormDesign.md)|Administrators or users with the personalize\_form role can use the form design feature to quickly create new or change existing form views. Form design is an alternative to configuring forms that combines several configuration options into one tool.|
|[Form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md)|Administrators or users with the personalize\_form role can configure a form to show or hide fields from a view. You can create new fields on the table associated with the form.|
|Related lists|Related lists display records in another table that have a relationship with the current record. Administrators or users with the personalize\_form role can configure related lists to appear on the form.|

## Using guided setup to implement Incident Management

IT Service Management guided setup provides a sequence of tasks that help you configure Incident Management on your ServiceNow instance. To open ITSM guided setup, navigate to **Guided Setup** &gt; **ITSM Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/guided-setup.md).

-   **[Quick start tests for Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/quick-start-tests-im.md)**  
Validate that Incident Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
-   **[Incident Management properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/incident-management-properties.md)**  
Incident Management properties control features such as copying and creating child incidents. The major incident properties control the promotion of major incident candidates to major incidents.
-   **[Incident categories and subcategories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/r_CategorizingIncidents.md)**  
Incident categories and subcategories help route incidents to the right team and reduce troubleshooting time. The base system includes predefined categories and subcategories that administrators can extend.
-   **[Define priority lookup rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/def-prio-lookup-rules.md)**  
Define impact and urgency combinations that determine incident priority and the SLA for each priority for an organization. Only administrators and data lookup administrators can configure these rules.
-   **[Define an assignment rule for incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/t_DefinAnAssignRuleIncidents.md)**  
Define assignment rules to automatically assign incidents to the group or user who has the skills to work on them.
-   **[Incident templates and record producers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/incident-templates-record-producers.md)**  
Templates simplify the process of submitting new records by populating fields automatically. A template helps you capture incident information consistently. A record producer is a specific type of catalog item that allows end users to create task-based records, such as incident records, from the service catalog.
-   **[View incident notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/t_ViewIncidentNotification.md)**  
View incident notifications that are sent during specific events in an incident life cycle. Recipients include employee self-service \(ESS\) users and users with the itil role.
-   **[Configure the default user for auto-closing incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/change-default-user.md)**  
Specify the user that appears in the Updated by field when incidents are closed automatically.
-   **[Applying CSDM guidelines to Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/itsm-incident-use-case-product-view.md)**  
Applying CSDM guidelines to Incident Management connects incidents to services, service offerings, and CIs so that you can see business impact and route incidents to the correct groups.
-   **[Incident ticketing integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/c_IncidentTicketingIntegrations.md)**  
An incident ticketing integration exchanges ticket data between your ServiceNow instance and a third-party system.
-   **[Configuring Microsoft Outlook to create incidents and VTB tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/create-incident-outlook.md)**  
To create incidents and VTB tasks, or to chat with a virtual agent from within your Outlook email, activate and deploy the ServiceNow Add-in for Microsoft Outlook.

**Parent Topic:**[Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/c_IncidentManagement.md)

