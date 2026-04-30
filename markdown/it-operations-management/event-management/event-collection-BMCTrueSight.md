---
title: Event collection from BMC TrueSight and BMC TrueSight\_v2
description: The MID WebService Event Collector enables you to collect JSON formatted event messages sent from BMC TrueSight Operations Management \(TrueSight\), previously known as BMC ProactiveNet Performance Management \(BPPM\), utilizing event stream notification capabilities.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Event collection from BMC TrueSight and BMC TrueSight\_v2

The MID WebService Event Collector enables you to collect JSON formatted event messages sent from BMC TrueSight Operations Management \(TrueSight\), previously known as BMC ProactiveNet Performance Management \(BPPM\), utilizing event stream notification capabilities.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Ensure that you:

-   Deploy and start the MID Server. See [MID Server configuration](https://www.servicenow.com/docs/access?context=c_MIDServerConfiguration&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
-   Configure and start the MID Web Server. See [Configure the MID Web Server extension](configure-mid-web-server-extension.md).
-   Configure and start the MID WebService Event Collector. See [Configure the MID WebService Event Collector Context](configure-em-context-extension.md).

Role required: evt\_mgmt\_admin

## About this task

JSON formatted event messages are sent from BMC TrueSight. The MID Server transforms the collected event messages by parsing them using the TransformEvents\_bmcTrueSight script include, located here: **Event Management** &gt; **Integrations** &gt; **Listener Transform Scripts**. In the Listener Transform Scripts page, click **TransformEvents\_bmcTrueSight**.

The default format of the URL to push event messages from BMC TrueSight to the MID Server is `http://<MID_Server_IP>:<MID_Web_Server_Port>/api/mid/em/inbound_event?Transform=TransformEvents_bmcTrueSight`.

The default format of the URL to push event messages from BMC TrueSight\_v2 to the MID Server is `http://<MID_Server_IP>:<MID_Web_Server_Port>/api/mid/em/inbound_event?Transform=TransformEvents_bmcTrueSight_v2`.

<table id="table_bbq_cmk_k2b"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MID\_Server\_IP

</td><td>

IP address of the MID Web Server Extension.

</td></tr><tr><td>

MID\_Web\_Server\_Port

</td><td>

Listening port of the MID Web Server Extension.

</td></tr><tr><td>

MID\_Web\_Server\_User

</td><td>

Username for the MID Web Server Extension.

</td></tr><tr><td>

MID\_Web\_Server\_Password

</td><td>

Password of the user of the MID Web Server Extension. However, encode the password in BASE64. For example, if the MID Web Server Extension password is `admin`, in this case use `YWRtaW4=` as the password for MID\_Web\_Server\_Password. To determine the BASE64 value, you can use the utility at this website: [https://www.base64encode.org/](https://www.base64encode.org/)

</td></tr></tbody>
</table>The following procedure describes the collection of JSON formatted event messages using basic authentication. For more information about supported authentication methods, see [Configure the MID Web Server extension](configure-mid-web-server-extension.md).

## Procedure

1.  In BMC TrueSight, set the MID WebService Event Collector as the target for BMC TrueSight notification, using these parameters:

    |Variable|Description|
    |--------|-----------|
    |serverHost|Name of the BMC TrueSight server.|
    |port|Number of the BMC TrueSight port.|

2.  In the message body and generic BMC URL, replace the parameters with the values in the preceding table and connect to BMC TrueSight.

    Use the BMC Publish-Subscribe REST approach to create a stream event subscription and send event messages in JSON format. The generic format of the BMC URL to create a stream event subscription is: `http|https://<serverHost>:<port>/bppmws/api/stream/subscribe?dataType=event`. For example: `http://TrueSight1server:40/bppmws/api/stream/subscribe?dataType=event`.


## Result

|Event field|Event message|
|-----------|-------------|
|node|mc\_host|
|type|mc\_object\_class|
|metric\_name|mc\_parameter|
|resource|mc\_object|
|severity|severity|
|time\_of\_event|date\_reception|
|description|msg|

## Example

Example, showing the message body.

```

{
"action": "create",
"data": {
"mc_abstracted": [],
"itsm_operational_category3": "",
"mc_object_class": "CPU",
"source": "MySource",
"adapter_host": "",
"itsm_operational_category2": "",
"itsm_location": "",
"itsm_operational_category1": "",
"mc_abstraction": [],
"mc_tool_id": "",
"mc_original_priority": "PRIORITY_1",
"event_handle": "3172",
"mc_modhist": [],
"mc_tool_class": "",
"mc_origin": "",
"mc_tool_uri": "",
"mc_service": "",
"mc_smc_type": "",
"mc_object_owner": "",
"mc_object": "CPU_0",
"mc_notes": [],
"itsm_model_version": "",
"mc_origin_key": "",
"mc_tool_address": "",
"mc_ueid": "mc.pncell_bmcswetsom96.1829b8ed.0",
"mc_bad_slot_names": [],
"date": "20161114081525.000000-300",
"itsm_item": "",
"mc_timeout": "0",
"mc_priority": "PRIORITY_1",
"itsm_type": "",
"itsm_manufacturer": "",
"mc_tool_key": "",
"itsm_product_name": "",
"mc_smc_impact": "NOT_ELECTED",
"mc_parameter": "MEMFreeMem",
"mc_bad_slot_values": [],
"itsm_incident_id": "",
"mc_incident_report_time": "0",
"mc_event_model_version": "1.1.00",
"mc_relationships": "0/0",
"CLASS": "EVENT",
"mc_using_organization": "",
"mc_tool_sev": "",
"mc_parameter_threshold": "",
"mc_smc_effects": [],
"mc_smc_priority": "0",
"itsm_company": "",
"date_reception": "1479129325",
"mc_smc_alias": "bmcswetsom96_2",
"pn_detail_diag_count": "0",
"mc_effects": [],
"mc_object_uri": "",
"mc_date_modification": "1479129325",
"mc_incident_time": "0",
"status": "OPEN",
"msg": "Free Memory Low",
"pn_detail_diag": "0",
"mc_host": "bmcswetsom97",
"repeat_count": "69",
"mc_host_address": "",
"mc_tool_suggestion": "",
"mc_using_organization_id": "",
"mc_collectors": ["1.1", "3.1.1", "4.1", "5.1"],
"mc_account": "",
"mc_long_msg": "",
"mc_owner": "",
"mc_history": ["pncell_bmcswetsom96:3172"],
"itsm_category": "",
"mc_host_class": "",
"mc_tool_rule": "",
"mc_local_reception_time": "1479129325",
"mc_associations": [],
"mc_relation_source": "",
"mc_propagations": [],
"mc_client_address": "172.16.173.131",
"itsm_incident_status": "",
"mc_tool_time": "0",
"mc_origin_class": "",
"mc_tool": "",
"mc_action_count": "0",
"mc_cause": "0",
"mc_origin_sev": "",
"mc_host_id": "0",
"mc_event_relations": [],
"mc_operations": [],
"mc_event_category": "CONFIGURATION_MANAGEMENT",
"pn_device_name": "",
"mc_arrival_time": "1479129325",
"severity": "OK",
"mc_notification_history": [],
"mc_smc_causes": [],
"mc_acl": [],
"mc_original_severity": "CRITICAL",
"duration": "0",
"mc_location": "Unknown",
"mc_smc_id": "",
"mc_parameter_value": "20",
"administrator": "",
"mc_event_subcategory": "OTHER",
"mc_parameter_unit": ""
},
"subscriptionId": "af18f6ba-a2d3-4574-81c8-7f366ca70ebd",
"type": "EVENT"
}
```

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

