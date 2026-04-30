---
title: Configure the MID WebService Event Collector Context
description: Configure the MID WebService Event Collector Context to provide a URL method to push event messages from an external source to the MID Server.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the MID WebService Event Collector Context

Configure the MID WebService Event Collector Context to provide a URL method to push event messages from an external source to the MID Server.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Role required: evt\_mgmt\_admin

## About this task

The default format of the URL to push event messages from an external source to the MID Server is `http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/em/jsonv2`. This URL provides good performance.

From an external source, to push event messages that are not in jsonv2 format, the format of the URL is: `http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/em/inbound_event?Transform={Name_of_Transform_Script}`, where the *\{Name\_of\_Transform\_Script\}* variable is the full name of the script and always begins with the text: `TransformEvents_`.

For example, assume the following values:

-   \{MID\_Server\_IP\}: 10.118.69.27
-   \{MID\_Web\_Server\_Port\}: 8097
-   Transform script name: EventsToProcess

The URL to be used is therefore: `http://10.118.69.27:8097/api/mid/em/inbound_event/TransformEvents_EventsToProcess`

**Note:**

-   The URL in the format `http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/em/{transform_script_name}`is also supported.
-   The date format for events is yyyy-M-d h:mm:ss.

    If you receive an event whose date is in a different format, you must use a `{transform_script_name}` that is appropriate for the incoming event's date format. If you do not, the event will not be processed correctly.

    For example, if an event arrives on June 27, 2019 at 11:25 AM with a listed date of **2019/06/27/ 11:25:00 a**, use a `{transform_script_name}` with a date format of **yyyy/MM/dd/ HH:mm:ss a** to match the format of the received event.


## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **MID WebService Event Listener**.

2.  In the MID WebService Event Collector Contexts list, click **New**.

3.  On the form, fill in the fields.

<table id="table_od5_flc_bx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name for this collector for easy identification.

</td></tr><tr><td>

Short description

</td><td>

Enter a brief, meaningful description of this collector.

</td></tr><tr><td>

MID Web Server Extension

</td><td>

Specify and then start the MID Web Server extension. The supported authentication methods are listed in the **Authentication Type** field of the MID Web Server extension. For information about how to configure a MID Web Server extension, see [Configure the MID Web Server](configure-mid-web-server-extension.md).

</td></tr><tr><td>

Status

</td><td>

This field is auto-populated with the status of the MID Web Server extension. This field is blank until the MID Web Server extension is started. After issuing a command to the MID Web Server extension, one of the following values is displayed: -   **Started**: The collector is running.
-   **Stopped**: The collector is not running.
-   **Offline**: The MID Server is down.
-   **Error**: The collector failed with an error \(the error message is displayed in **Error Message**\).
-   **Warning**: A run-time exception has occurred.


</td></tr><tr><td>

Execute on

</td><td>

**Specific MID Server** or **Specific MID Server Cluster**, as defined on the specified MID Web Server extension.

</td></tr><tr><td>

MID Server

</td><td>

The **Specific MID Server** or **Specific MID Server Cluster**, as defined on the specified MID Web Server extension.

</td></tr><tr><td>

Executing on

</td><td>

The name of the MID Server on which the MID Web Server extension is running.

</td></tr></tbody>
</table>4.  Right-click the form heading and click **Save**.

5.  Under **Related Links**, click **Start** to start the collector.

    |Related Link|Description|
    |------------|-----------|
    |Start|If it is not running, start the collector. This action verifies that a web service API endpoint with the Event Management application is running on the MID Server.|
    |Stop|Stops the running collector on the configured MID Server. If the collector is not running, no action is taken.|
    |Restart|Stops, then starts the collector on the configured MID Server.|
    |Update parameters|Sends updated parameters to the collector. Parameters are also updated when the Event Management MID Server context extension is updated. If you click this control when the collector is not running, no update is made.|


## Example

**Showing the use of the URL to transform JSON v2 formatted event messages**

Assume that JSON v2 formatted event messages are sent to the MID Server. When using the `jsonv2` URL, there is no need to use a script include.

|Field|Value|
|-----|-----|
|MID\_Server\_IP|10.218.64.27|
|MID\_Web\_Server\_Extension\_Port|8097|
|Event message format|jsonv2|

Replace the variables in the default format of the URL `http://<my-instance>.service-now.com/api/global/em/jsonv2`with values from the preceding table:`http://10.218.64.27:8097/api/global/em/jsonv2`

**Example showing the URL to push messages not in jsonv2 format**

The format of the URL to push event messages from an external source that are not in jsonv2 format is `http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/em/inbound_event/Transform={Name_of_Transform_Script}` where the \{Name\_of\_Transform\_Script\} variable is the full name of the script and always begins with the text: TransformEvents\_. The script name must be specified as the `Transform` header parameter and must always start with the prefix `TransformEvents_`.

For this example, assume that the script name is EventsToProcess, the URL is therefore:`http://10.138.64.27:8097/api/mid/em/inbound_event/TransformEvents_EventsToProcess`

**Example showing JSON v2 formatted event messages**

**Note:** When copying and pasting the text following, hidden characters might also be copied and can cause unexpected results.

```

curl -v -H "Accept: application/json" -H "Content-Type: application/json" -X POST --data "{
    "records":
    [ {
         \"source\" : \"Simulated\",
        \"node\" : \"nameofnode\",
        \"type\" : \"High Virtual Memory\",
        \"resource\" : \"C:\",
        \"severity\" : \"5\",
        \"description\" : \"Virtual memory usage exceeds 98%\",
        \"ci_type\":\"cmdb_ci_app_server_tomcat\",
        \"additional_info\":\"{\\\"name\\\":\\\"My Airlines\\\"}\"
      },
      {
      \"source\" : \"Simulated\",
      \"node\" : \"01.myairlines.com\",
      \"type\" : \"High CPU Utilization\",
      \"resource\" : \"D:\",
      \"severity\" : \"5\",
      \"description\" : \"CPU on 01.my.com at 60%\"
      }
   ]
}" -u UserName:Password http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/em/jsonv2

```

## Example

**Example showing JSON v2 formatted event messages with MID Web Server API key**

**Note:** When copying and pasting the text following, hidden characters might also be copied and can cause unexpected results.

```

curl --location -g --request POST 'http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/em/jsonv2' \
--header 'Accept: application/json' \
--header 'Content-Type: application/json' \
--header 'Authorization: key <mid_webserver_api_key>' \
--data-raw '{
   "records":
    [ {
         \"source\" : \"Simulated\",
        \"node\" : \"nameofnode\",
        \"type\" : \"High Virtual Memory\",
        \"resource\" : \"C:\",
        \"severity\" : \"5\",
        \"description\" : \"Virtual memory usage exceeds 98%\",
        \"ci_type\":\"cmdb_ci_app_server_tomcat\",
        \"additional_info\":\"{\\\"name\\\":\\\"My Airlines\\\"}\"
      },
      {
      \"source\" : \"Simulated\",
      \"node\" : \"01.myairlines.com\",
      \"type\" : \"High CPU Utilization\",
      \"resource\" : \"D:\",
      \"severity\" : \"5\",
      \"description\" : \"CPU on 01.my.com at 60%\"
      }
   ]
}'
```

**Related topics**  


[Configure the MID Web Server extension](configure-mid-web-server-extension.md)

[Event collection from BMC TrueSight](event-collection-BMCTrueSight.md)

[Event collection from Microsoft Azure Monitor](event-collection-MicrosoftAzure.md)

[Event collection from Google Cloud Platform](event-collection-GCP.md)

