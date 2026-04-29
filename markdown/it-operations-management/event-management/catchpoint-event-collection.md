---
title: Integrate Catchpoint events
description: Integrate Catchpoint with Event Management by adding an alert webhook in the Catchpoint platform.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Catchpoint events

Integrate Catchpoint with Event Management by adding an alert webhook in the Catchpoint platform.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Role required: evt\_mgmt\_admin

## About this task

Configure the Event Management environment for the collection of events from Catchpoint by authenticating Catchpoint as a data source. In the Catchpoint platform, set your ServiceNow AI Platform as the rest endpoint using a webhook.

## Procedure

1.  In the Catchpoint platform, create an alert webhook destination.

    1.  Login to the Catchpoint platform.

    2.  Navigate to **Catchpoint** &gt; **Setting** &gt; **API** &gt; **Alert Data Webhook** to set the webhook endpoint.

    3.  In the API Alert Webhook, provide the following details.

<table id="table_fs2_xss_2tb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Any name based on your requirement.

</td></tr><tr><td>

URL

</td><td>

The default format of the URL to push events from Catch Point to the ServiceNow AI Platform instance, `https://<username>:<password>@<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=catchpoint`.

</td></tr><tr><td>

On Failure Alert

</td><td>

The email address for the API Alert webhook.

</td></tr><tr><td>

Notification Trigger

</td><td>

Select based on your requirement. The default value is 3.

</td></tr><tr><td>

Add the following headers

</td><td>

-   Authorization: **Basic \{Base 64 \| username:password\}**
-   Content-Type: **application/json**


</td></tr><tr><td>

Format

</td><td>

Select **Template** and add the following template:```
{
"Source": "CatchPoint",
"severity": "${notificationLevelId}",
"alertType": "${AlertType}",
"time_of_event": "${alertCreateDateUtc(YYYY-MM-DD HH:MI:SS)}",
"monitorType": "${Switch(${MonitorTypeId},'0', 'IE','2', 'Object','3','Emulated','8', 'Ping','9', 'Tracert','10', 'DNS-Traversal','11', 'Ping-TCP','12', 'DNS-Exp', '13','DNS-Direct', '14','Tracert-UDP', '15', 'Port-TCP','16', 'FTP','17', 'Data-Push-API','18', 'Chrome','19', 'Playback', '20', 'Playback-Mobile', '21', 'SMTP', '22', 'Port-UDP', '23', 'Ping-UDP', '24', 'Streaming', '25', 'API', '26', 'Mobile',
 '27', 'SFTP', '28', 'SSH', '29', 'Tracert-TCP')}",
"testName": "${TestName}",
"testId": "${TestId}",
"testUrl": "${TestUrl}",
"testPath": "${testPath}",
"testLink": "${testLink}",
"productName": "${ProductName}",
"clientId": "${ClientId}",
"productId": "${productId}",
"nodeName":"${nodeDetails("${nodeName}")}",
"nodeClientServerAddress":"${nodeDetails(\"${NodeClientAddress},\"),}",
"nodeServerAddress":  "${nodeDetails(\"${nodeServerAddress},\"),}",
"Labels" : "${testLabels}",
"addtionalInformation": "Test initial URL: ${testUrl}\n\nAlert type: ${AlertType}\n\nScatter Chart: ${scatterplotChartURL}\n\nWaterfall Chart: ${waterfallChartURL}\n\nTest properties: ${testLink}\n\nTest time of run / Test time of alert (Central Time): ${reportDateLocal(YYYY-MM-DD HH:MI:SS)} / ${alertCreateDateLocal(YYYY-MM-DD HH:MI:SS)}"}

```

</td></tr></tbody>
</table>2.  For the HTTP Endpoint monitoring tests, in the ServiceNow instance, create a CI.

    **Note:** The Catchpoint connector supports multiple types of monitoring tests such as Endpoint, Networking, and others. The following steps apply only to the HTTP Endpoint monitoring tests.

    1.  Navigate to **Configuration** &gt; **CI Class Manager**.

    2.  Click **Hierarchy** and search for **HTTP\(S\) Endpoint**.

    3.  In the CI Type field, select **cmdb\_ci\_endpoint\_http**.

    If the services are not modeled, then you should manually add the CIs under the \[cmdb\_ci\_endpoint\_http\] table. Also, the manual endpoint should be removed before the automatic discovery of services. For other type tests CI bindings, you can create Event rules based on their requirements.


## Result

Alerts start flowing from the Catchpoint connector into the Event Management plugin. The following table shows how the Catchpoint severity mapping translates into the ServiceNow mapping.

|Catchpoint severity|ServiceNow severity|
|-------------------|-------------------|
|0|Warning|
|1|Critical|
|2/3|Clear|

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

