---
title: Uni-directional incident ticketing integrations
description: Consider the requirements for an external, third-party system to create tickets. Define the data that must be sent to create a ticket, and what validation is required.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Incident ticketing integrations, Configure, Incident Management, IT Service Management]
---

# Uni-directional incident ticketing integrations

Consider the requirements for an external, third-party system to create tickets. Define the data that must be sent to create a ticket, and what validation is required.

In this way, a standard web service interface can be created and published. This integration responds with a ticket number on success, or with a structured error message for validation failures and processing issues. An advantage of this implementation is that you can publish once and reuse for multiple applications, provided the additional integrations follow the integration specifications. A good practice is to create a dedicated account for each interface. Accounts provide accountability and report user statistics, and use a simple connectivity Point of Contact \(POC\).

## Integration plan contents

-   Firewall requirements
-   Protocols to be used
-   Required middleware \(for example, MS Biztalk\)
-   Error messages
-   Validation rules

## Example using basic authentication

This implementation responds to the third-party system with the ticket ID. The Import Set tables function as a staging area for your data.

![Uni-directional ticketing integration using basic authentication](../image/UniDirectionalTicketingIntegrationUsingBasicAuthentication.png "Uni-directional ticketing integration using basic authentication")

## Example using import sets

An implementation variation for the inbound path would be to use the Import Set Tables as interface tables. In this example, the Incident\_Interface Table stores a history of data as it was received and before the data was transformed. The destination Incident Table could store a history of how the incident has changed over time and who changed it. The transform scripts would process the import set and the business rules would run on the target table.

![Uni-directional ticketing integration using import sets](../image/UniDirectionalTicketingIntegrationUsingImportSets.png "Uni-directional ticketing integration using import sets")

**Parent Topic:**[Incident ticketing integrations](c_IncidentTicketingIntegrations.md)

