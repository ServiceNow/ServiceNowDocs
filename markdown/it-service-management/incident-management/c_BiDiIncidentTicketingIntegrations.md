---
title: Bi-directional incident ticketing integrations
description: A bi-directional integration exchanges data between your ServiceNow instance and a third-party system so that incident information is synchronized between the systems.
locale: en-US
release: zurich
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Incident ticketing integrations, Configure, Incident Management, IT Service Management]
---

# Bi-directional incident ticketing integrations

A bi-directional integration exchanges data between your ServiceNow instance and a third-party system so that incident information is synchronized between the systems.

This integration is more complex than a uni-directional integration because it has the following requirements.

-   Comprehensive definitions of field mappings.
-   Standardization of where transformations take place: inbound, outbound, or both.
-   Consideration of the ownership of reference data.
-   How updates are performed on an ongoing basis.

Implement error handling. Include all these implementations in the integration plan.

While bi-directional implementations are developed on their own merits, you can develop a framework in the ServiceNow AI Platform that can be reused, for example, data driven validation rules.

## Integration plan contents

-   Plan contents for all the aspects needed for a bi-directional integration.
-   State models for each organization.
-   Business rule definitions for keeping the tickets synchronized.
-   Requirements to store history of individual transactions. If this form of audit is a requirement, consider creating an interface table which is populated prior to creating and updating the destination table.
-   Transformation rules for all data elements.
-   Time lines for when reference data is transported to the information system. Include requirements to perform transformations before sending the data to and from each system.
-   Statement of reference data ownership at all stages.
-   Update schema definitions.

## Example using import sets and web services

In this implementation, data authentication is done before insertion into the import set. Transform maps and scripts execute before the data reaches the Incident table. The Incident table is used to store the history of the incident records. For the outbound data path, the target table could trigger business rules before the data is queued in the outbound web service.

## Example using import sets and the ECC queue

An implementation variation for the inbound path would be to use an import set table \(in our example, the Incident Interface table\) to store historical data. Data validation is also done now, and you can clear exceptions with processing or manual intervention. The Incident table uses a Third-Party Information table as a reference, and messages are generated based on business rules.

Implementing this type of integration involves a web-service component for third-party applications for inbound data. The ECC queue is recommended for outbound data.

**Parent Topic:**[Incident ticketing integrations](c_IncidentTicketingIntegrations.md)

