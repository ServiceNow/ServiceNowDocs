---
title: Third-party data integration solution overview
description: A typical enterprise ecosystem includes enterprise resource planning \(ERP\), sales management, and service management systems. There are multiple options for implementing the integrations between these systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/csm-third-party-data-overview.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Third-party data integration for CSM, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Third-party data integration solution overview

A typical enterprise ecosystem includes enterprise resource planning \(ERP\), sales management, and service management systems. There are multiple options for implementing the integrations between these systems.

In this example, the ERP system manages customer data \(for example, Accounts\).

\[Omitted image "csm-typical-enterprise-it-ecosystem.png"\] Alt text: Chart of an enterprise ecosystem in which the Enterprise Resource Planning system manages the integration between ServiceNow Service Management and Salesforce Sales Management applications.

When a new account is acquired, it is created first in the ERP system and then account data is transferred to Salesforce and ServiceNow \(1\).

During this process, new accounts are created in Salesforce and ServiceNow. The ServiceNow account record is updated with the Salesforce account ID attribute that holds the reference to the Salesforce account record. The Salesforce account ID is later used to match account records between ServiceNow and Salesforce and also to retrieve opportunity data from Salesforce.

When an agent accesses an account in Agent Workspace for CSM, a list of related opportunities for this account is retrieved from Salesforce in real-time and presented to the agent.

This example assumes that the flow has been implemented and executed and that the ServiceNow account records contain valid Salesforce account IDs. This example also uses the following configuration:

-   Connectivity between a ServiceNow and Salesforce.
-   Integration using Integration Hub and remote tables.

## Integration architecture

ServiceNow integrates with Salesforce through the OAuth 2.0 Bearer Token Flow.

\[Omitted image "csm-third-party-data-integration-architecture.jpg"\] Alt text: Diagram of the integration between ServiceNow account records and Salesforce Opportunity records using the IntegrationHub spoke.

\[Omitted image "csm-third-party-data-integration-hub-architecture.jpg"\] Alt text: Diagram of the script and query processing between the Salesforce Opportunity remote table and Integration Hub.

