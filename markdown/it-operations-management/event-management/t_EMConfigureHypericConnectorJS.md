---
title: Configure event collection from Hyperic
description: Configure the Hyperic connector instance to receive events from the VMware vRealize Hyperic server.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure event collection from Hyperic

Configure the Hyperic connector instance to receive events from the VMware vRealize Hyperic server.

## Before you begin

Role required: evt\_mgmt\_admin

Supported version: 5.8.4.0.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New** and create a Hyperic connector instance with the following details:

    |Field|Value|
    |-----|-----|
    |Name|Specify a unique name for the Hyperic connector instance.|
    |Host IP|Specify the Hyperic IP address.|
    |Credential|In the Credentials form, click **New** and create the required credentials. Save the credentials using a unique and recognizable name, for example, HypericOPS.|
    |Schedule \(seconds\)|The frequency in seconds that the system checks for new events from Hyperic.|
    |Description|Type a description for the use of the Hyperic event collection instance.|
    |Connector definition|The vendor and protocol used to gather events from the external event source. Select the **Hyperic** connector definition.|
    |Last error message|The last error message is automatically updated.|
    |Last run time|The last run time value is automatically updated.|
    |Last run status|The last run time status is automatically updated.|
    |MID Servers \(MID Server for Connectors section\)|Optional. Name of a MID Server. If no MID Server is specified, an available MID Server that has a matching IP range is used. In the MID Servers for Connectors section, specify a MID Server that is up and valid. You can configure several MID Servers. If the first is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section.|

3.  Right-click the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

4.  In the Connector Parameters section, specify the values of the mandatory Hyperic parameters.

    1.  **port** Default value 7080.

    2.  **protocol** Default value http.

5.  Click **Test connector** to verify the connection between the MID Server and the Hyperic connector.

6.  If the test fails, follow the instructions that are issued by the error to correct the problem and then run another test.

    **Note:** Use a network tool, such as ping, to verify credential correctness and network connectivity from the MID Server to the Hyperic server.

7.  After a successful test, select the **Active** check box and then click **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

**Related topics**  


[Configure a pull connector](t_EMConfigureConnectorInstance.md)

