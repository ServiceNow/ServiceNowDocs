---
title: Configure event collection from SolarWinds monitor
description: Configure the SolarWinds monitor connector instance to receive events from the SolarWinds monitor.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure event collection from SolarWinds monitor

Configure the SolarWinds monitor connector instance to receive events from the SolarWinds monitor.

## Before you begin

Supported versions:

-   SAM 6.2.1
-   NPM 2020.2

**Note:** The SolarWinds monitor connector instance can import events from:

-   Network Performance Monitor \(NPM\)
-   SolarWinds Service &amp; Application Monitor \(SAM\)

The SolarWinds monitor connector instance requires a credential that lets the instance access SolarWinds monitor accounts. You can use an existing credential or [create a new one](create-credentials-solarwinds.md). The provided user must have access to the SolarWinds API to receive events from the SolarWinds connector.

Role required: evt\_mgmt\_admin and evt\_mgmt\_integration

## About this task

This connector has the **debug** and **logPayloadForDebug** log parameters enabled. The **debug** parameter logs debug messages, such as calls made to the source system to retrieve events. The **logPayloadForDebug** parameter logs event and metric payloads from the source system. Once debugging is complete, set this parameter to **false** to prevent overloading the system.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Type a descriptive name for the SolarWinds monitor connector.|
    |Description|Type a description for the use of the SolarWinds monitor event collection instance.|
    |Connector Definition|Select **Solarwinds\_v2**.|
    |Host IP|Specify the SolarWinds monitor IP address.|
    |Credential|Select the credential with basic authentication that you created for this connector. For more information, see [Create SolarWinds monitor credentials](create-credentials-solarwinds.md).|
    |Event collection last run time|The last run time value of the scheduled job. This field is updated automatically.|
    |Last event collection status|The last event collection status. This field is updated automatically.|
    |Event collection schedule \(seconds\)|The frequency in seconds that the system checks for new events from the SolarWinds monitor server.|
    |Last error message|The last error message received by the connector is automatically updated.|

4.  Right-click the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

5.  In the Connector Instance Values section, specify these fields:

    |Field|Value|
    |-----|-----|
    |initial\_sync\_in\_days|Specify how many days the initial pull must contain to retrieve events. The default value is 7 days.|
    |nodes\_custom\_properties|Specify the SolarWind monitor property names that are associated with the relevant node. This information is added to the **Additional Information** field of the event in JSON format. The SolarWinds monitor custom properties are user-defined fields, for example, country, building, or serial number, that you can associate with monitored network objects. Separate multiple entries with a comma.|
    |port|Specify the value of the port. By default, the value is 17774.|

6.  Name of a MID Server.

    If no MID Server is specified, an available MID Server that has a matching IP range is used. In the MID Servers for Connectors section, specify a MID Server that is up and valid. You can configure several MID Servers. If the first is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section. The privileges that are required for the user account that is used for the MID Server to collect events from SolarWinds monitor is that of evt\_mgmt\_integration.

7.  Click **Test connector** to verify the connection between the MID Server and the SolarWinds monitor connector.

    If the test fails, follow the instructions that are issued by the error to correct the problem and then run another test.

    **Note:** Use a network tool, such as ping, to verify credential correctness and network connectivity from the MID Server to SolarWinds monitor.

8.  After a successful test, select the **Active** check box and then click **Update**.


-   **[Create SolarWinds monitor credentials](create-credentials-solarwinds.md)**  
Create credentials to access SolarWinds monitor.

**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

**Related topics**  


[Configure a pull connector](t_EMConfigureConnectorInstance.md)

