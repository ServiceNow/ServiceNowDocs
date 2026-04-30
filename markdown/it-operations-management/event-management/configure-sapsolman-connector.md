---
title: Configure SAP Solution Manager connector
description: Configure the SAP Solution Manager \(Solman\) connector instance to enable communication between the SAP Solution Manager and Event Management.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure SAP Solution Manager connector

Configure the SAP Solution Manager \(Solman\) connector instance to enable communication between the SAP Solution Manager and Event Management.

## Before you begin

Role required: admin

Supported versions: Tested on SAP Solution Manager 7.2. Might also work on other versions.

## About this task

This configuration enables you to update the SAP Solution Manager with the statuses that have been updated by ServiceNow. For general information about the SAP Solution Manager, see [SAP configurations enabling the SAP Solution Manager connector](../concept/sap-manager-connector.md).

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New** and create a connector instance.

3.  Fill in the fields on the form.

<table id="table_bqf_1m2_sbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for the SAP Solman connector.

</td></tr><tr><td>

Description

</td><td>

Description for the use of the SAP Solman event collection instance.

</td></tr><tr><td>

Active

</td><td>

Option that activates the connector instance. Select this option only after running a successful test.

</td></tr><tr><td>

Connector definition

</td><td>

The vendor and protocol used to gather events from the external event source. Select **SAP Solman**.

</td></tr><tr><td>

Host IP

</td><td>

The IP address where SAP Solman is installed.

</td></tr><tr><td>

Credential

</td><td>

Required credentials entered either by selecting them from the results of a search through the search icon ![Search icon](../image/search-icon.png) or by clicking **New**. or creating them. If you create credentials, save them using a unique and recognizable name, such as `SAPSOLMANOPS`.

</td></tr><tr><td>

Event collection last run time

</td><td>

The last run time value. Automatically updated.

</td></tr><tr><td>

Last event collection status

</td><td>

The last run time status. Automatically updated.

</td></tr><tr><td>

Event collection schedule \(seconds\)

</td><td>

The frequency in seconds that the system checks for new events from SAP Solman.

</td></tr><tr><td>

Bi-directional

</td><td>

Ensure that you select this option to invoke the bi-directional exchange of values to-and-from the external event source. The **Last bi-directional** status option appears only when selecting this option.

</td></tr><tr><td>

Last bi-directional status

</td><td>

This field appears only when **Bi-directional** is selected. This field is automatically populated with the most recent bi-directional status.

</td></tr><tr><td>

Last error message

</td><td>

Last error message. Automatically updated.

</td></tr><tr><td>

Connector Instance Values section

</td><td>

The parameters that are specific to SAP Solman, automatically displayed when saving the form.

</td></tr><tr><td>

MID Servers \(MID Server for Connectors section\)

</td><td>

MID Server that is up and valid. You can configure several MID Servers so that if the first server is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order in which their details are entered into the MID Server for Connectors section. If no MID Server is specified, an available MID Server that has a matching IP range is used.

</td></tr></tbody>
</table>4.  Right-click the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

5.  In the Connector Instance Values section, specify the default connector instance values.

    -   **Client**: Default value = `001`
    -   **Port**: Default value = `8000`
6.  Right-click the form header and select **Save**.

7.  Click **Test Connector** to verify the connection between the MID Server and the connector.

    If the test fails, follow the instructions in the error message and then run another test.

    **Note:** Use a network tool such as `ping` to verify the credentials and the network connectivity from the MID Server to the SAP Solman monitor.

8.  After a successful test, select the **Active** check box and click **Update**.


-   **[SAP configurations enabling the SAP Solution Manager connector](../concept/sap-manager-connector.md)**  
Configure your SAP environment to work with the ServiceNow Event Management platform so you can use the SAP Solution Manager connector.

**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

**Related topics**  


[Use the SAP Solution Manager Push connector](sap-push-connector.md)

