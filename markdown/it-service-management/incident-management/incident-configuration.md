---
title: Configuring Incident Management
description: You can configure the incident form and other incident features, such as incident categories and UI behavior. The ITSM guided setup helps you configure incident management on your ServiceNow instance.
locale: en-US
release: zurich
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Incident Management, IT Service Management]
---

# Configuring Incident Management

You can configure the incident form and other incident features, such as incident categories and UI behavior. The ITSM guided setup helps you configure incident management on your ServiceNow instance.

## Configuration overview

Configure the Incident form in the base system to follow ITIL best practices. The administrator can configure the incident form and use the form designer to customize it. You can copy or create child incident to reduce the effort of configuring the functionality of an open incident.

![Configure the incident form](../image/config-form-layout.png "Incident form configuration")

|Menu option|Description|
|-----------|-----------|
|[Form design](https://www.servicenow.com/docs/access?context=c_FormDesign&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)|Administrators or users with the personalize\_form role can use the form design feature to quickly create new or change existing form views. Form design is an alternative to configuring forms that combines several configuration options into one tool.|
|[Form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)|Administrators or users with the personalize\_form role can configure a form to show or hide fields from a view. You can create new fields on the table associated with the form.|
|[Related lists](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)|Related lists display records in another table that have a relationship with the current record. Administrators or users with the personalize\_form role can configure related lists to appear on the form.|

## Using guided setup to implement Incident Management

IT Service Management guided setup provides a sequence of tasks that help you configure Incident Management on your ServiceNow instance. To open ITSM guided setup, navigate to **Guided Setup** &gt; **ITSM Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

-   **[Quick start tests for Incident Management](../../../administer/atf-quick-start-tests/reference/quick-start-tests-im.md)**  
Validate that Incident Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
-   **[Incident Management properties](../reference/incident-management-properties.md)**  
Incident Management properties are used to control features such as copying and creating child incidents. The major incident properties control the promotion of major incident candidates to major incidents.
-   **[Incident categories and subcategories](../reference/r_CategorizingIncidents.md)**  
Categorization of incidents helps in routing to the right team and saves a lot of time in troubleshooting and bringing the service to normalcy.
-   **[Define priority lookup rules](../task/def-prio-lookup-rules.md)**  
Define impact and urgency of an incident to calculate the priority. The priority calculation can then be used to prioritize work and drive service level agreements.
-   **[Define assignment rules for incidents](../task/t_DefinAnAssignRuleIncidents.md)**  
Define assignment rules to identify the right group or the user which is skilled to work on an incident.
-   **[Incident templates and record producers](incident-templates-record-producers.md)**  
Templates simplify the process of submitting new records by populating fields automatically. A template ensures consistency in the way information about the incident is captured. A record producer is a specific type of catalog item that allows end users to create task-based records, such as incident records, from the service catalog.
-   **[View incident notifications](../task/t_ViewIncidentNotification.md)**  
View incident notifications that are sent during specific events in an incident life cycle. These notifications are sent to various recipients including the ESS and the ITIL users.
-   **[Configure default user for auto-closing incidents](../task/change-default-user.md)**  
Change the default user who last updated an incident to the user you mention for auto-closing incidents.
-   **[Applying CSDM guidelines to Incident Management](itsm-incident-use-case-product-view.md)**  
Incident Management supports the incident management process with the ability to identify and log incidents, classify and prioritize incidents, assign incidents to appropriate users or groups, escalate, resolve, and report incidents. The goal of this product view is to help you to understand how Incident Management key entities work with the core CSDM framework.
-   **[Incident ticketing integrations](c_IncidentTicketingIntegrations.md)**  
An incident ticketing integration exchanges ticket data between your ServiceNow instance and a third-party system.
-   **[Configuring Microsoft Outlook to create incidents and VTB tasks](create-incident-outlook.md)**  
To create incidents and VTB tasks, or to chat with a virtual agent from within your Outlook email, activate and deploy the ServiceNow Add-in for Microsoft Outlook.

**Parent Topic:**[Incident Management](c_IncidentManagement.md)

