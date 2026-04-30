---
title: Manually configure the Metric Intelligence extension
description: Configure the MID Server Metric Intelligence extension to enable the MID Server to pull raw metrics from external systems, to detect anomalies and report anomalies to the instance along with raw data. This MID Server Metric Intelligence extension is required and must be running in order for your system to be able to collect Metric Intelligence data.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Get started with Metric Intelligence, Activating Metric Intelligence, Metric Intelligence, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Manually configure the Metric Intelligence extension

Configure the MID Server Metric Intelligence extension to enable the MID Server to pull raw metrics from external systems, to detect anomalies and report anomalies to the instance along with raw data. This MID Server Metric Intelligence extension is required and must be running in order for your system to be able to collect Metric Intelligence data.

## Before you begin

See [Get started with Metric Intelligence](get-started-metrics.md) for the high level steps of setting up Metric Intelligence.

Role required: evt\_mgmt\_admin

## About this task

The MID Server Metric Intelligence extension normalizes the raw data and then transmits the data to the instance. If the extension detected any anomalies above a specified threshold, they are sent to the instance.The extension runs for as long as it is enabled. This provides a persistent connection to the MID Server to constantly listen for raw Metric Intelligence data from external systems.

The MID Server Metric Intelligence extension:

-   Receives raw metric data, batches them and sends them to the instance at specified intervals.
-   Detects anomalies and sends a report to the instance.
-   The information that is sent to the ServiceNow instance is relevant for Metric Intelligence, so data processing is efficient.

The MID Server Metric Intelligence extension does not provide any API calls. However, when the **Enable REST Listener** option is selected, the extension adds a handler for the supported REST APIs.

**Note:**  

-   Only upon configuring the Metric Intelligence extension, the Metric Intelligence MID Servers actually join the distributed cluster for Metric Intelligence.
-   After the initial configuration, the first metric is not included in the metrics data. 
-   There is a delay of one minute in receiving metric information from the synchronization of the instance with the MID Server.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Profiles and Deployments** &gt; **Metric Intelligence**.

2.  In the Metric Intelligence Metrics Contexts list, click **New**.

3.  Fill in the fields, as appropriate.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name for this extension for easy identification.

</td></tr><tr><td>

Short description

</td><td>

A description of this extension.

</td></tr><tr><td>

Status

</td><td>

This field is auto-populated with the status of the extension. The field is blank until the extension is started. After issuing a command to the extension, one of the following values is displayed: -   **Started**: The extension is running.
-   **Stopped**: The extension is not running.
-   **Offline**: The MID Server is down.
-   **Error**: The extension failed with an error \(the error message is displayed in **Error Message**\).
-   **Warning**: A run-time exception has occurred. The extension continues to work.


</td></tr><tr><td>

Error Message

</td><td>

Message describing any error that causes a command, such as **Start** or **Stop**, to fail. This field appears when the value in the **Status** field is **Error** and also when the value in the **Status** field is **Warning**.

</td></tr><tr><td>

Execute on

</td><td>

Location for running this extension. When configuring this option for use with Metric Intelligence, set to **Specific MID Server**. Then specify the MID Server with **Operationalintelligence** as a supported application and the **Metrics** capability.

</td></tr><tr><td>

MID Server

</td><td>

The name of the designated MID Server, which is configured with **Operationalintelligence** as a supported application and the **Metrics** capability.

</td></tr><tr><td>

Executing on

</td><td>

\[Read-Only\] The name of the MID Server on which the extension is running. This field shows the name of the MID Server even if the MID Server is down. If the user stops the extension, this field is empty.

</td></tr></tbody>
</table>4.  When using the Push method for collecting Metric Intelligence data, the MID Server Metric Intelligence extension must be configured with the **Enable REST Listener** enabled. This option enables a listener so that a REST endpoint can receive raw metric data. The raw metric data is then placed in the regular data flow where the data is sent to the instance and the anomaly detector looks for anomalies. When selected, it adds a handler to the web server to listen for any metrics that are pushed to the MID Server. When this option is selected, the Web Server extension, which starts a Web Server on the MID Server, must also be configured. For more information, see [Configure the MID Web Server extension](configure-mid-web-server-extension.md).

5.  Right-click the form heading and select **Save**.

6.  Under **Related Links** click **Start** to save the Metric Intelligence data in this extension and start the extension.

    |Related Link|Description|
    |------------|-----------|
    |Start|Starts the extension on the configured MID Server if it is currently not running.|
    |Stop|Stops the running extension on the configured MID Server. No action is taken if the extension is not running.|
    |Restart|Stops, then starts the extension on the configured MID Server.|
    |Test|The test is not relevant to Metric Intelligence. Parameters are not tested or validated when **Test** is run.|
    |Update parameters|Sends the latest saved parameters to the extension.|


