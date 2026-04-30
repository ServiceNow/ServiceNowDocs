---
title: Resolving Service Graph Connector issues
description: You can use the Service Graph Connector Support Tools application to initiate a chatbot conversation with a virtual agent and resolve an issue or perform a general analysis on a Service Graph Connector installed on your instance.Resolve the Service Graph Connector issues or perform a general analysis using the Troubleshooting module available for Service Graph Connectors.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [service graph connector, connector, resolve connector issues]
breadcrumb: [Service Graph Connector Support Tools, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Resolving Service Graph Connector issues

You can use the Service Graph Connector Support Tools application to initiate a chatbot conversation with a virtual agent and resolve an issue or perform a general analysis on a Service Graph Connector installed on your instance.

If a user with the admin role has installed the Service Graph Connector Support Tools application, you can initiate a chat conversation with a virtual agent to resolve Service Graph Connector issues. The application includes prebuilt conversations as a response to an issue type.

You can use the prebuilt conversations to debug and resolve the following types of issues:

-   **Connection issues**

    Depending on the data source selected, the virtual agent suggests you to update or set required properties, run the Workflow Studio action corresponding to the connector manually, and verify the response from the data source using HTTP logs.

-   **Data issues**

    The virtual agent suggests you to check for customizations in Identification and Reconciliation engine \(IRE\) rules, reconciliation rules, business rules, and mappings. Review the field and import causing the issue, reprocess the import row, and view the complete transformation information. Also, suggests to perform additional troubleshooting steps.

-   **Performance issues**

    Depending on the data source and import set selected, the virtual agent suggests you to make a basic performance check and review the history of the Configuration Management Database \(CMDB\) integration executions.

-   **Mapping issues**

    The virtual agent suggests you to review mappings for input and output fields using the IntegrationHub ETL store app.


**Parent Topic:**[Service Graph Connector Support Tools](cmdb-sgc-support-tools.md)

## Resolve a Service Graph Connector issue

Resolve the Service Graph Connector issues or perform a general analysis using the Troubleshooting module available for Service Graph Connectors.

### Before you begin

[Install Service Graph Connector Support Tools](../task/sgc-cmdb-troubleshooting-install.md)

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Troubleshooting**.

2.  In the Now Support window, select **Click here to start a new conversation**.

3.  Select **Show me everything**.

4.  Select **Service Graph Connector Help**.

5.  Select a help option.

    |Option|Description|
    |------|-----------|
    |**Debug a specific Service Graph Connector**|Select to resolve an issue with a Service Graph Connector installed on your instance.|
    |**General analysis**|Select to analyze an import row or a Configuration Management Database \(CMDB\) integration execution.|

6.  Based on the selected help option, follow the help instructions to resolve an issue or perform a general analysis.

7.  Close the conversation by selecting **End the chat**.


