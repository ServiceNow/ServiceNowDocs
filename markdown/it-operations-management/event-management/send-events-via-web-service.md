---
title: Pushing events to the instance using web service API
description: You can use a web service interface, supported by ServiceNow, that operates on the JSON object as the data input and output format.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Pushing events to the instance using web service API

You can use a web service interface, supported by ServiceNow, that operates on the JSON object as the data input and output format.

## Before you begin

Role required: evt\_mgmt\_integration

## About this task

To insert records in the event \[em\_event\] table with a single call, use this web service API:

`https://<instancename>.service-now.com/api/global/em/jsonv2`

**Note:** Business rules on the event table are not invoked when this URL is used.

Do not add additional fields to an event by adding a custom field to the event table \[em\_event\]. However, additional fields should be included in the **Additional information** \[additional\_info\] field of the event. For more information about how to include additional fields in events, see [Custom alert fields](../concept/populate-custom-alert-fields.md).

The URL in the format: `http://<instancename>.service-now.com/em_event.do?JSONv2&sysparm_action=insertMultiple` is also supported in case you do want to activate Business rules. However, the performance of the first URL is superior.

To work with the URL that ends with `=insertMultiple`, add the following properties, with their respective values, to the MID Server:

-   "mid.probe.event.queue.compress" - value: false
-   "mid.probe.event.bulk\_size" - value: 100
-   "mid.probe.event.endpoint.url" - value: em\_event.do?JSONv2%26sysparm\_action=insertMultiple

## Procedure

1.  Send the request with these headers:

<table id="table_mwb_yfk_lx"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td>

String

</td><td>

The acceptable type for this message.The default value is `application/json`.

</td></tr><tr><td>

Content-Type

</td><td>

String

</td><td>

The content type for this message.The default value is `application/json`.

</td></tr><tr><td>

POST

</td><td>

String

</td><td>

The request type is POST, with one or more trailing records.

</td></tr></tbody>
</table>2.  One or more events in JSON format can be sent as the payload of the web service call.

    Event fields that should be populated are:

<table id="table_eqx_mgk_lx"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

source

</td><td>

The name of the event source type. For example, SCOM or SolarWinds.

</td></tr><tr><td>

event\_class

</td><td>

Specific instance of the **source**. For example, `SCOM 2012 on 10.20.30.40`

</td></tr><tr><td>

node

</td><td>

The **node** field should contain an identifier for the Host \(Server/Switch/Router/etc.\) that the event was triggered for. The value of the **node** field can be one of the following identifiers of the Host: -   Name
-   FQDN
-   IP
-   Mac Address
If it exists in the CMDB, this value is also used to bind the event to the corresponding ServiceNow CI.

</td></tr><tr><td>

resource

</td><td>

If the event refers to a device, such as, Disk, CPU, or Network Adapter, or to an application or service running on a Host, the name of the device or application must be populated in this field. For example, `Disk C:\` or `Nic 001` or `Trade web application`.

</td></tr><tr><td>

metric\_name

</td><td>

Name of the metric that triggered the alert. For example, `Used Memory` or `Total CPU utilization`.

</td></tr><tr><td>

type

</td><td>

The type of event. This type might be similar to the **metric\_name** field, but is used for general grouping of event types.

</td></tr><tr><td>

message\_key

</td><td>

This value is used for de-duplication of events. For example, there might be two events for the same CI, where one event has CPU of 50% and the next event has CPU of 99%. Where both events must be mapped to the same ServiceNow alert, they should have the same message key. The field can be left empty, in which case the field value defaults to `source+node+type+resource+metric_name`. The **message\_key** should be populated only when there is a better identifier than the default.

</td></tr><tr><td>

severity

</td><td>

Severity of the event. ServiceNow values for severity range from 1 – Critical to 5 – OK, with the severity of 0 – Clear. Original severity values should be sent as part of the additional information.

</td></tr><tr><td>

additional\_info

</td><td>

This field is in JSON key/value format, and is meant to contain any information that might be of use to the user. It does not map to a pre-defined ServiceNow event field. Examples include IDs of objects in the event source, event priority \(if it is not the same as severity\), assignment group information, and so on. Values in the **Additional information** field of an Event that are not in JSON key/value format are normalized to JSON format when the event is processed.

</td></tr><tr><td>

time\_of\_event

</td><td>

Time when the event occurred on the event origin. The format is: yyyy-MM-dd HH:mm:ssThe specified time must be according to GMT.

</td></tr><tr><td>

resolution\_state

</td><td>

Optional – To indicate that an event has been resolved or no longer occurring, some event monitors use ‘clear’ severity, while other event monitors use a ‘close’ value for severity. This field is used for those monitors proffering the latter. Valid values are `New` and `Closing`.

</td></tr></tbody>
</table>3.  To create multiple records with a single call, trigger the event web service using the following URL, where the &lt;instance name&gt; variable is replaced with the name of the required instance:

    `https://<instancename>.service-now.com/api/global/em/jsonv2`

    Example showing the payload for two events that are sent in a single web service call:

    ```
    {
      "records": [
        {
          "source": "SCOM",
          "event_class": "SCOM 2012 on scom.server.com",
          "resource": "D:",
          "node": "name.of.node.com",
          "metric_name": "Percentage Logical Disk Free Space",
          "type": "Disk space",
          "severity": "4",
          "description": "The disk D: on computer V-W2K8-abc.abc.com is running out of disk space. The value that exceeded the threshold is 38% free space.",
          "additional_info": {
            "scom-severity": "Medium",
            "metric-value": "38",
            "os_type": "Windows.Server.2008"
          }
        },
        {
          "source": "SCOM",
          "event_class": "SCOM 2012 on scom.server.com",
          "resource": "MSSQL-database-name",
          "node": "other.node.com",
          "metric_name": "DB Allocated Size (MB)",
          "type": "Database Storage",
          "severity": "3",
          "description": "High number of active connections for MSSQL-database-name running on name.of.node.com. Active connections exceed 5000.",
          "additional_info": {
            "scom-severity": "Medium",
            "metric-value": "38",
            "os_type": "Windows.Server.2008"
          }
        }
      ]
    }
    ```

4.  To create one record with a single call, trigger the event web service using the following URL, where the &lt;instancename&gt; variable is replaced with the name of the required instance:

    `https://<instancename>.service-now.com/api/global/em/jsonv2`

    Example showing the payload for one event that is sent in a single web service call:

    ```
    {
      "records": [
        {
          "source": "SCOM",
          "event_class": "SCOM 2007 on scom.server.com",
          "resource": "C:",
          "node": "name.of.node.com",
          "metric_name": "Percentage Logical Disk Free Space",
          "type": "Disk space",
          "severity": "4",
          "description": "The disk C: on computer V-W2K8-dfg.dfg.com is running out of disk space. The value that exceeded the threshold is 41% free space.",
          "additional_info": {
            "scom-severity": "Medium",
            "metric-value": "38",
            "os_type": "Windows.Server.2008"
          }
        }
      ]
    }
    ```

    Example: cURL request:

    ```
    {
      curl -X POST "https://<instancename>.service-now.com/api/global/em/jsonv2" \
      --header "Content-Type: application/json" \
      --user "username:password" \
      --data '{
        "records": [
          {
            "source": "SCOM",
            "event_class": "SCOM 2007 on scom.server.com",
            "resource": "C:",
            "node": "name.of.node.com",
            "metric_name": "Percentage Logical Disk Free Space",
            "type": "Disk space",
            "severity": "4",
            "description": "The disk C: on computer V-W2K8-dfg.dfg.com is running out of disk space. The value that exceeded the threshold is 41% free space.",
            "additional_info": {
              "scom-severity": "Medium",
              "metric-value": "38",
              "os_type": "Windows.Server.2008"
            }
          }
        ]
      }'
     
    ```


**Related topics**  


[Pushing events to the MID Server using web service API](../concept/event-collection-via-MID-using-push.md)

