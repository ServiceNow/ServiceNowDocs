---
title: Incident ticketing integrations
description: An incident ticketing integration exchanges ticket data between your ServiceNow instance and a third-party system.
locale: en-US
release: yokohama
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Incident Management, IT Service Management]
---

# Incident ticketing integrations

An incident ticketing integration exchanges ticket data between your ServiceNow instance and a third-party system.

The advantages of an incident ticketing integration include the following items.

-   Establishing a ticket number that provides a unique key between systems.
-   Synchronizing the systems so that notifications can be triggered.
-   Transforming data for more uniform processing.
-   Tracking ticket activity for accurate reporting.

The level of data and the direction of the data that is exchanged categorizes the integration as uni-directional or bi-directional. In a uni-directional integration, a third-party system creates an incident ticket, passes data to your instance, and receives a ticket ID back as confirmation. In a bi-directional integration, incident data is exchanged, synchronized, and updated while data is sent between the systems.

For both integration types, a good practice is to implement a record-based log of the individual transactions for a given time period. If an outage occurs, a record-based log can tell you what data was exchanged, how it was transformed, when processing occurred, and if there were any errors. Record-based logs also allow you to run all the validation and transformation logic away from the main form, helping performance.

Before implementing your project, develop an integration plan in which all the implementation aspects and requirements are defined. Developing the integration plan helps you to review the current data, plan for future requirements, and identify and sequence project tasks.

-   **[Uni-directional incident ticketing integrations](c_UniDirIncidentTicketIntegrations.md)**  
Consider the requirements for an external, third-party system to create tickets. Define the data that must be sent to create a ticket, and what validation is required.
-   **[Bi-directional incident ticketing integrations](c_BiDiIncidentTicketingIntegrations.md)**  
A bi-directional integration exchanges data between your ServiceNow instance and a third-party system so that incident information is synchronized between the systems.

**Parent Topic:**[Configuring Incident Management](incident-configuration.md)

