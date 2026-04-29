---
title: SAP configurations enabling the SAP Solution Manager connector
description: Configure your SAP environment to work with the ServiceNow Event Management platform so you can use the SAP Solution Manager connector.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure SAP Solution Manager connector, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# SAP configurations enabling the SAP Solution Manager connector

Configure your SAP environment to work with the ServiceNow Event Management platform so you can use the SAP Solution Manager connector.

When integrating your SAP environment with Event Management, the SAP Solution Manager sends events through a MID Server to Event Management, which generates an alert from the event.

After the MID Server processes events, you can perform the following actions in the SAP Solution Manager:

-   Add comments
-   Confirm alerts
-   Set status to **Externally Managed**

The following diagram illustrates the flow of data between SAP and Event Management.

![SAP Manager Connector diagram](../image/sap-manager-connector-diagram.png "SAP Solution Manager connector")

Data moves between SAP and Event Management using both Push and Pull interfaces.

-   **Pull interface**:

    The Connector Update Queues table \[em\_connector\_update\_queue\] lists manual updates of alerts and sends them to the SAP Solution Manager.

    The table's business rule identifies each manual update of alerts in Event Management and updates the connector queue with these changes. By default, changes to all alert fields are tracked. For information on adjusting this setting, see the SAP Solution Manager documentation.

    The Event Management - Queue connector processor scheduled job removes alert changes from the queue and sends them to the MID Server. By default, the system performs this process in batches of 1,000 alerts. You can customize this batch size by setting the **evt\_mgmt.max\_update\_source\_records** property.

    **Note:** You must define the Pull interface to enable bi-directional functionality in the SAP Solution Manager connector. For details, see the SAP Solution Manager documentation.

-   **Push interface**: Because SAP can only push data to an external source, the integration uses the Push interface to store alerts sent from SAP to Event Management.

    SAP alerts create events in Event Management that use both event rules and CI identification rules to create Event Management alerts.

    After Event Management creates alerts, a business rule listens for a change to the alert. If it detects a change, Event Management updates the SAP Solution Manager alerts.


-   **[Use the SAP Solution Manager Pull connector](../task/sap-pull-connector.md)**  
The SAP Solution Manager Pull connector sends information from Event Management to the SAP Solution Manager. The Pull connector sends responses received from a Push connector in a bi-directional environment.
-   **[Use the SAP Solution Manager Push connector](../task/sap-push-connector.md)**  
The MID Server web service Event Collector enables you to collect alerts sent from the SAP Solution Manager through event stream notification capabilities. The interface runs both a Push and a Pull interface to interact directly with the SAP Solution Manager.
-   **[SAP Solution Manager setup configurations](sap-solman-configurations.md)**  
As part of the SAP Solution Manager setup, you must perform several configurations to enable SAP Solution Manager to interact with Event Management.
-   **[SAP Solution Manager transaction codes](../reference/sapsolman-transaction-codes.md)**  
The transaction code abbreviations that you can use in the SAP interface when working with the SAP Solution Manager connector.

**Parent Topic:**[Configure SAP Solution Manager connector](../task/configure-sapsolman-connector.md)

**Related topics**  


[Event Management Integrations](c_EMEvent.md)

[Use the SAP Solution Manager Pull connector](../task/sap-pull-connector.md)

