---
title: Incident templates and record producers
description: Templates simplify the process of submitting new records by populating fields automatically. A template ensures consistency in the way information about the incident is captured. A record producer is a specific type of catalog item that allows end users to create task-based records, such as incident records, from the service catalog.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Incident Management, Incident Management, IT Service Management]
---

# Incident templates and record producers

Templates simplify the process of submitting new records by populating fields automatically. A template ensures consistency in the way information about the incident is captured. A record producer is a specific type of catalog item that allows end users to create task-based records, such as incident records, from the service catalog.

You can use incident templates to quickly create incidents for similar issues.

-   An administrator or user with the template\_editor\_global role can create templates that are available to everyone.
-   An administrator can enable the global option for any personal template that a user creates so that all other users can access the template.
-   A user with the itil role can create their own templates for incidents they log frequently.

ESS users typically log incidents using a record producer in the service catalog. A template can be used to create an incident record producer. The template automatically populates fields in the incident form.

For example, an incident record producer can be created to request account access to a network server. The user who submits the incident enters variable values, such as the server name, level of access needed, and due date. The incident template assigned to the record producer populates the incident **Category**, **Subcategory**, and **Assignment Group**. These fields and values applied from the template do not appear in the record producer form.

-   **[Create incident template](../task/t_CreateAnIncidentTemplate.md)**  
Create an incident template to ensure consistency in the way information about the incident request is captured. A template also helps you to create incident easily and accurately.
-   **[Create a module that uses incident template](../task/t_UseATemplateFromAModule.md)**  
Create a module to log an incident with pre-filled field values from an existing template.
-   **[Create a record producer to log incidents](../task/t_CreateARecordProducer.md)**  
Create record producers to log incidents directly from Service Catalog.
-   **[Create a record producer using a template](../task/t_CreateRecProducWithTempl.md)**  
If a predefined incident template exists, it can be used with the record producer to fill in standard information for the incident.

**Parent Topic:**[Configuring Incident Management](incident-configuration.md)

