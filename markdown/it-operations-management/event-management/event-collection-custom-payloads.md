---
title: Event collection from custom payloads
description: The MID WebService Event Collector enables you to collect event information from custom payloads in JSON, XML, or plain text format.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event collection from custom payloads

The MID WebService Event Collector enables you to collect event information from custom payloads in JSON, XML, or plain text format.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Role required: evt\_mgmt\_admin

## About this task

The MID Server transforms the collected event messages and populates the Event table fields \(em\_table\) in the instance. The collection of formatted event messages is described in this procedure using basic authentication. For information about supported authentication methods, see [Configure the MID Web Server extension](configure-mid-web-server-extension.md).

The format of the required MID Server URL is: `http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/em/inbound_event?Transform={Transform_script_name}`. The name of the MID Server script include is composed by appending a suffix to the default `TransformEvents_` prefix. For information about the collection of JSON v2 event messages, see [Configure the MID WebService Event Collector Context](configure-em-context-extension.md).

**Note:** The URL in the format `http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/em/{transform_script_name}`is also supported.

## Procedure

1.  Configure the MID WebService Event Collector, see [Configure the MID WebService Event Collector Context](configure-em-context-extension.md).

2.  Start the MID WebService Event Collector.


## Example

**Transformation of XML formatted event messages using the custom payload URL**

Assume that XML formatted event messages are sent to the MID Server. Use this example to return an array of event objects from the collected event messages. The name of the MID Server script include is composed by appending a suffix to the default `TransformEvents_` prefix. For the purposes of this example, the user supplied the xmlSample script include. Using these details, the name of the MID Server script include is `TransformEvents_xmlSample`. The MID Server transforms the collected event messages by parsing the messages using the script include and then transmitting them to the instance.

|Field|Value|
|-----|-----|
|MID\_Server\_IP|10.218.64.27|
|MID\_Web\_Server\_Extension\_Port|8097|
|transform\_script\_suffix \_name|xmlSample|

Replace the variables in the URL with the values from the above table: `http://10.218.64.27:8097/api/mid/em/xmlSample`

**Note:** When copying and pasting the text below, hidden characters might also be copied and can cause unexpected results.

Example showing XML formatted event messages:

```
<records>
    <event>
    <source>My Source</source>
    <node>host1</node>
    <type>type1</type>
    <severity>3</severity>
    <description>Virtual memory usage exceeds 98%</description>
    </event>
    <event>
    <source>My Source</source>
    <node>host2</node>
    <type>type2</type>
    <severity>2</severity>
    <description>Virtual memory usage exceeds 90%</description>
    </event>
    </records>

```

**Related topics**  


[Configure the MID Web Server extension](configure-mid-web-server-extension.md)

[Configure the MID WebService Event Collector Context](configure-em-context-extension.md)

