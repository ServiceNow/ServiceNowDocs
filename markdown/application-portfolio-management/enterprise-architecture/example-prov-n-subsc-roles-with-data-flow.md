---
title: Example: Provider and subscriber with data flow directions
description: The provider and subscriber roles are independent of the data flow direction. The following example illustrates how the same provider and subscriber pairing can support both outgoing and incoming data flow directions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/enterprise-architecture/example-prov-n-subsc-roles-with-data-flow.html
release: australia
product: Enterprise Architecture
classification: enterprise-architecture
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [Working with digital integrations, Working with digital integration management in Enterprise Architecture Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Example: Provider and subscriber with data flow directions

The provider and subscriber roles are independent of the data flow direction. The following example illustrates how the same provider and subscriber pairing can support both outgoing and incoming data flow directions.

**Use case:** Provision employee data to create human case agents

-   **Provider Business Application:** Corporate repository, for example, Active Directory
-   **Subscriber Business Application:** ServiceNow platform

This integration supports two data flow directions:

-   **Outgoing: Provider to Subscriber**

    Active Directory runs a scheduled job and pushes the latest employee updates to the ServiceNow platform every four hours. The provider \(Active Directory\) initiates the connection, so the data flow direction is outgoing.

-   **Incoming: Subscriber to Provider**

    The ServiceNow platform connects through a MID Server to the on-premises corporate repository, which exposes an LDAP interface, and pulls the latest changes every four hours. The subscriber \(ServiceNow platform\) initiates the connection, so the data flow direction is incoming.


In both cases, Active Directory remains the provider because it owns the digital interface. The **Data Flow Direction** field reflects which application initiates the connection, not which application owns the data.

**Parent Topic:**[Working with digital integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/enterprise-architecture/eaw-work-with-digital-integrations.md)

