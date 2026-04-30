---
title: Established connections
description: Access data from external sources directly in the ServiceNow AI Platform, without copying any data to your instance using zero copy connections.
locale: en-US
release: yokohama
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: concept
last_updated: "2025-03-07"
reading_time_minutes: 3
breadcrumb: [Exploring Workflow Data Fabric Hub, Workflow Data Fabric Hub, Data and Automation]
---

# Established connections

Access data from external sources directly in the ServiceNow AI Platform, without copying any data to your instance using zero copy connections.

## Key benefits

-   Access external data without the complexity and maintenance involved with extract, transform, and load \(ETL\) processes.
-   Minimize security risks associated with copying and storing data in multiple locations.
-   Maintain data accuracy by avoiding errors associated with data replication.
-   View external data assets and create data fabric tables with mapped data.

Zero copy connections enable access to external data locally, while reducing storage consumption and minimizing security risks typically associated with duplicating data across multiple systems.

In the Workflow Data Fabric Hub, a connection admin can navigate to the **Available connectors** tab to view primary and community connectors and create a zero copy connection. After the connection is established, the connection admin can grant access to a data steward. The data steward can then access the zero copy connection from the **Established connections** tab to create a data fabric table.

![Established connections in Workflow Data Fabric Hub.](../image/wdf-zc-connections.png "Established connections in Workflow Data Fabric Hub")

## Required ServiceNow AI Platform roles

The df\_connection\_admin role is required to create and manage zero copy connections.

A role containing the df\_data\_steward role is required to access established connections and create data fabric tables.

## Accessing established connections

View established connections by navigating to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Established connections** or **All** &gt; **Workflow Data Fabric Hub** &gt; **Established connections**.

## Monitoring connection status

Determine whether a connection requires an update by checking the status on the **Established connections** tab.

-   **Connected**

    The connection to the data source has been tested and established.

-   **Deactivated**

    The connection to the data source has been deactivated by the connection admin.

-   **Needs configuration**

    The connection attributes or authentication information are missing from the connection details.

-   **Needs mapping**

    The connection has been tested and established, but the data isn't mapped to a data fabric table.

-   **Not connected**

    The connection details have been added, but the connection to the data source isn't working.


## Data steward access

The connection admin determines which data stewards can access a specific connection by granting the df\_data\_steward role to one or more roles on the **Access Controls** tab in an established connection.

The data steward's primary goal is to provide quality data to consumers to meet their business needs. Additionally, data stewards have the following responsibilities:

-   Understanding business applications and the data that users need.
-   Communicating data access requirements to integration admins.
-   Creating data fabric tables and mapping data from external sources.
-   Maintaining the quality and integrity of data.

## Use cases

-   Access data from an external data source without importing and storing it on your instance. Customer order information is often stored in an external Customer Relationship Management \(CRM\) system, with the data ultimately residing in an external data lake such as Snowflake. When a customer calls to report a product issue, an agent working on the ServiceNow AI Platform opens a request and accesses the customer's full order history directly from Snowflake. The customer's order history stays in Snowflake, the system of record, but is available to the agent in real time on the ServiceNow AI Platform.
-   Provide end-to-end details to agents with real-time data from an outside source. When a customer calls to make a warranty service claim against a vehicle, an agent working on the ServiceNow AI Platform can access extended warranty details from an external data lake in real time using a zero copy connection. The customer service agent can update the service request ticket with the latest warranty details directly from the data lake, ensuring the latest warranty information is used in the service ticket.

For more information, see [Managing zero copy connections in Workflow Data Fabric Hub](managing-connections-wdf.md).

