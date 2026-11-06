---
title: Uni-directional incident ticketing integrations
description: In a uni-directional integration, an external third-party system creates tickets in your ServiceNow instance. Define the data that must be sent to create a ticket and the validation that is required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/c\_UniDirIncidentTicketIntegrations.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Incident ticketing integrations, Configuring Incident Management, Incident Management, IT Service Management]
---

# Uni-directional incident ticketing integrations

In a uni-directional integration, an external third-party system creates tickets in your ServiceNow instance. Define the data that must be sent to create a ticket and the validation that is required.

You can create and publish a standard web service interface for this integration. This integration responds with a ticket number on success, or with a structured error message for validation failures and processing issues. An advantage of this implementation is that you can publish once and reuse for multiple applications, provided the additional integrations follow the integration specifications. A general guideline is to create a dedicated account for each interface. Accounts provide accountability and report user statistics, and use a simple connectivity point of contact \(POC\).

## Integration plan contents

-   Firewall requirements
-   Protocols to be used
-   Required middleware \(for example, Microsoft BizTalk\)
-   Error messages
-   Validation rules

## Example using basic authentication

This implementation responds to the third-party system with the ticket ID. The import set tables function as a staging area for your data.

## Example using import sets

A variation for the inbound path uses import set tables as interface tables. In this example, the Incident\_Interface table stores a history of data as it was received and before the data was transformed. The destination Incident table can store a history of how the incident has changed over time and who changed it. The transform scripts process the import set, and the business rules run on the target table.

**Parent Topic:**[Incident ticketing integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/c_IncidentTicketingIntegrations.md)

