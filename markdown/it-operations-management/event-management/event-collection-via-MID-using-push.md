---
title: Pushing events to the MID Server using web service API
description: Configure the MID WebService Event Collector to provide a URL method to push event messages to the MID Server.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Pushing events to the MID Server using web service API

Configure the MID WebService Event Collector to provide a URL method to push event messages to the MID Server.

The MID WebService Event Collector, by default, enables you to connect to an event generator and send event messages through the MID Server, using a URL in the format: `http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/em/jsonv2`

The JSON v2 format is the same as the format that clients use to send event messages to the instance. This URL provides good performance.

For more information, see [Configure the MID WebService Event Collector Context](../task/configure-em-context-extension.md).

**Note:** Event Management accepts events in the timezone of the MID Server through which the listener has sent the event message. If you require a different timezone, you can configure the script as required, see [Integrate with push connectors](../task/configure-listener-transform-script.md).

## URL to push custom payloads

The MID Server can also receive a custom payload in JSON, XML, or plain text format. In this case, the MID Server transforms the event messages using the script include that you provide, and then sends the events to the instance. The URL in this case is:

`http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/em/inbound_event?Transform={Transform_script_name}` For an example of a script include, see the default `TransformEvents_xmlSample` script include.

For an example of how the MID WebService Event Collector transforms JSON formatted event messages, see [Event collection from BMC TrueSight and BMC TrueSight\_v2](../task/event-collection-BMCTrueSight.md).

To send events in generic JSON format, you can use the URL in this format:

`http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/em/inbound_event?Transform=TransformEvents_MidJsonGeneric`

In this case, the `TransformEvents_MidJsonGeneric` MID script include that is provided in the base instance transforms the event messages into the event fields. All fields are added as **Additional Information** fields into the ServiceNow event that is generated.

**Note:** The URL in the format `http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/em/{transform_script_name}`is also supported.

The REST API URL for validating connectivity is: `http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/em/ping`

## Script include to transform collected events

Use the required MID Server script include to transform \(parse\) collected event messages and populate them into the mapped event field. The MID Server script include name is composed of a prefix and suffix. The prefix is the mandatory text `TransformEvents_` and the suffix is the transform name on the URL, for example, `http://{MID_Server_IP}:{MID_Web_Server_Port}/api/mid/em/xmlSample` ``. The composed script name is therefore `TransformEvents_xmlSample`.

You must supply a script include that receives the event messages in a text variable. The script must have a `transform()` function that performs the transformation and prepares the return array of Event objects. When the Event Management plugin is activated, you are provided with the `TransformEvents_xmlSample` sample include script that transforms events from XML format.

**Note:** Event fields that are not identical to fields in the event table are saved in the **Additional information** field.

## Event message headers

Specify the relevant request header value for the **Content-Type** field according to the format of the event message.

|Message format|Content-Type value|
|--------------|------------------|
|JSON|application/json|
|XML|application/xml|
|text|text/plain|

## Authentication and data security options

Options for authentication and data security:

-   **Authentication type**, which can be set to either `API Key`, `mTLS`, or `Basic`.
-   **Secure Connection**, which lets you choose whether incoming and outgoing data is secured when transmitted. If you choose the advanced secured option, it requires that you obtain a certificate from a well-known certificate authority, and then provide the **Keystore Certificate Alias** and the **Keystore Password**.
-   **Use MID Unified Keystore**, which provides encryption protection and enables you to install a custom certificate in the MID Server unified keystore. For details, see Install custom certificates in the MID Server unified key store.
-   Users must supply a script that receives the JSON, XML, or text formatted event messages in a text variable. The script must have a transform\(\) function that performs the transformation and prepares the return array of event objects. The `TransformEvents_xmlSample` include script that transforms events from XML format is provided as an example when the Event Management plugin is activated.

For more information about authentication and data security, see [Configure the MID Web Server extension](../task/configure-mid-web-server-extension.md).

**Related topics**  


[Pushing events to the instance using web service API](../task/send-events-via-web-service.md)

