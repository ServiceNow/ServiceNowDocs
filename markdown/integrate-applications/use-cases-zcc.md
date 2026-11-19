---
title: Use cases
description: Common real-world scenarios for zero copy connections and data fabric tables, showing how each feature solves common enterprise data access challenges.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/use-cases-zcc.html
release: australia
topic_type: concept
last_updated: "2026-11-11"
reading_time_minutes: 3
keywords: [zero copy connectors use cases, data fabric use cases, zero copy connection scenarios]
breadcrumb: [Explore, Zero Copy Connectors, Workflow Data Fabric]
---

# Use cases

Common real-world scenarios for zero copy connections and data fabric tables, showing how each feature solves common enterprise data access challenges.

## Zero copy connections

|Use case|Description|
|--------|-----------|
|Access data from an external data source without importing and storing it on your instance.|Customer order information is often stored in an external CRM system, with data residing in a data lake such as Snowflake. When a customer calls to report a product issue, an agent opens a request on the ServiceNow AI Platform. The agent accesses the customer's full order history directly from Snowflake. The customer's order history stays in Snowflake but is available to the agent in real time on the ServiceNow AI Platform.|
|Provide end-to-end details to agents with real-time data from an outside source.|When a customer calls to make a warranty service claim, an agent on the ServiceNow AI Platform can access extended warranty details from an external data lake. The agent uses a zero copy connection to retrieve the data in real time. The agent can update the service request ticket with the latest warranty details directly from the data lake.|
|Access data across multiple ServiceNow instances without replication.|With the ServiceNow Remote Instance connector, you can access records from other instances locally, without moving, duplicating, or setting up complex ETL processes. For example, if you manage several ServiceNow instances and need to consolidate data for reporting, designate one instance as your central processing instance. Create zero copy connections to query tables on your other instances in real time. Data remains in its original location and isn't persisted on the processing instance. This helps you maintain compliance with data residency requirements while gaining unified visibility across your organization.|

## Data fabric tables

<table id="table_uc_dft"><thead><tr><th>

Use case

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Unify data from multiple sources.

</td><td>

A manufacturer experiences an outage when a key piece of machinery fails, stopping production. Asset inventory data and maintenance personnel data are stored locally in the instance. Historical asset maintenance records and real-time sensor data are stored in an external data lake. To help prevent failures and outages, service technicians need all this data in one place. Using data fabric tables, sensor data is fed to the data lake and analyzed by machine learning, generating a failure score. When the score crosses a threshold, an alert triggers a maintenance request flow, creating a case assigned to a service technician. The technician reviews the case and accesses inventory data from the instance alongside maintenance records and real-time sensor data from the external data lake, all in one place. The technician makes an informed decision and acts to address the issue before another outage occurs.

</td></tr><tr><td>

Retrieve real-time data in an application.

</td><td>

An application can include both a physical table and a data fabric version of the same table. The admin can choose to populate the physical table through data import. Alternatively, users can access real-time data from an external data source using the data fabric table.

</td></tr><tr><td>

Analyze data and generate AI-guided insights using AI Data Explorer.

</td><td>

Create visualizations and analyses of fetched data through a conversational interface in AI Data Explorer. For more information, see [Use AI to explore data with AI Data Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/ai-data-explorer.md). **Note:** You must first add the relevant data fabric tables to the Semantic Table Configuration \[sn\_query\_gen\_table\_config\] table in Query Generation. For more information, see[Add a table to the semantic data layer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/add-table-semantic-layer.md).

</td></tr><tr><td>

Enhance the performance of AI experiences using the Knowledge Graph.

</td><td>

Enhance the performance of Now Assist Virtual Agent, AI agents, and generative AI skills by using data fabric tables in the Knowledge Graph application. For more information, see[Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph-landing.md).

</td></tr></tbody>
</table>