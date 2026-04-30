---
title: Configure event collection from vRealize
description: Configure the VMware vRealize Operations \(vRealize or vRealize\_V2\) connector instance to receive events from the vRealize Operations Log and Event Management servers. vRealize uses basic authentication. vRealize\_V2 uses token-based authentication.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure event collection from vRealize

Configure the VMware vRealize Operations \(vRealize or vRealize\_V2\) connector instance to receive events from the vRealize Operations Log and Event Management servers. vRealize uses basic authentication. vRealize\_V2 uses token-based authentication.

## Before you begin

Role required: evt\_mgmt\_admin

Supported version: 8.10.0.

**Note:** Connect to vRealize using a local account with at least Read-only vRealize Operations permission. You can use an existing credential or [create a new one](create-credentials-vrealize.md).

## About this task

This connector has the **debug** and **logPayloadForDebug** log parameters enabled. The **debug** parameter logs debug messages, such as calls made to the source system to retrieve events. The **logPayloadForDebug** parameter logs event and metric payloads from the source system. Once debugging is complete, set this parameter to **false** to prevent overloading the system.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New** and create a vRealize Operations connector instance with the following details:

    |Field|Value|
    |-----|-----|
    |Name|Specify a unique name for the vRealize Operations connector instance.|
    |Host IP|Specify the vRealize Operations IP address.|
    |Credential|Select the credential with basic authentication that you created for this connector. vRealize\_V2 uses token-based authentication providing that the user can generate the token. For more information, see [Create vRealize credentials](create-credentials-vrealize.md).|
    |Schedule \(seconds\)|The frequency in seconds that the system checks for new events from vRealize Operations.|
    |Description|Type a description for the use of the vRealize Operations connector.|
    |Connector definition|The vendor and protocol used to gather events from the external event source. Select **vRealize** or **vRealize\_V2** \(vRealize\_V2 is located in the Event Management connectors scope\).|
    |Last error message|The last error message is automatically updated.|
    |Last run time|The last run time value is automatically updated.|
    |Last run status|The last run time status is automatically updated.|
    |MID Servers \(MID Server for Connectors section\)|Optional. Name of a MID Server. If no MID Server is specified, an available MID Server that has a matching IP range is used. In the MID Servers for Connectors section, specify a MID Server that is up and valid. You can configure several MID Servers. If the first is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section.|

3.  Right-click the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

4.  In the Connector Parameters section, specify the values of the mandatory vRealize Operations parameters.

    1.  **port**: Default value = `443`.

    2.  **protocol**: Default value = `https`.

    3.  **days\_from**:

        Number of days worth of data to be pulled on the first event collection run. Default value = `14`. The **days\_from** option is available only when using vRealize\_V2.

5.  Click **Test connector** to verify the connection between the MID Server and the vRealize Operations connector.

6.  If the test fails, follow the instructions that are issued by the error to correct the problem and then run another test.

    **Note:** Use a network tool, such as ping, to verify credential correctness and network connectivity from the MID Server to vRealize.

7.  After a successful test, select **Active** and then click **Update**.


-   **[Create vRealize credentials](create-credentials-vrealize.md)**  
Create credentials to access vRealize.

**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

**Related topics**  


[Configure a pull connector](t_EMConfigureConnectorInstance.md)

