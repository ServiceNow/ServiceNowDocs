---
title: Service Graph Connector Support Tools
description: You can use the ServiceNow Service Graph Connector Support Tools application to resolve any issues or perform a general analysis on a Service Graph Connector installed on your instance.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [service graph connector, connector, resolve connector issues]
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector Support Tools

You can use the ServiceNow® Service Graph Connector Support Tools application to resolve any issues or perform a general analysis on a Service Graph Connector installed on your instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Key features

The Service Graph Connector Support Tools application includes prebuilt conversations as a response to an issue type and enables resolving Service Graph Connector issues and to perform a general analysis.

The application provides capability to debug and resolve the following types of issues:

-   **Connection issues**

    Depending on the data source selected, asks to update or set required properties, enables to run the Workflow Studio action corresponding to the connector manually, and provides a link to HTTP logs for verifying the response from the data source.

-   **Data issues**

    Checks for customizations in Identification and Reconciliation engine \(IRE\) rules, reconciliation rules, business rules, and mappings. Reviews the field and import causing the issue, reprocesses the import row, and provides the complete transformation information. Also, provides additional troubleshooting steps.

-   **Performance issues**

    Depending on the data source and import set selected, makes a basic performance check and reviews the history of the Configuration Management Database \(CMDB\) integration executions.

-   **Mapping issues**

    Reviews mappings for input and output fields using the IntegrationHub ETL store app.


The chatbot conversation also directs to the knowledge articles landing page in the Now Support knowledge base, if available for a connector.

-   **[Install Service Graph Connector Support Tools](../task/sgc-cmdb-troubleshooting-install.md)**  
You can install Service Graph Connector Support Tools if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.
-   **[Resolving Service Graph Connector issues](cmdb-sgc-troubleshooting.md#)**  
You can use the Service Graph Connector Support Tools application to initiate a chatbot conversation with a virtual agent and resolve an issue or perform a general analysis on a Service Graph Connector installed on your instance.

**Parent Topic:**[Service Graph Connectors](cmdb-sgc-available.md)

