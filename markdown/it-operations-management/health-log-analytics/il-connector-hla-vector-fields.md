---
title: Vector Agent integration configuration fields
description: Description of the fields on the Vector Agent integration configuration forms for Health Log Analytics.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-01-26"
reading_time_minutes: 1
keywords: [Vector Agent, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Integration configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Vector Agent integration configuration fields

Description of the fields on the Vector Agent integration configuration forms for Health Log Analytics.

For the Vector Agent integration setup procedure, see [Set up a Vector Agent integration for Health Log Analytics](../task/il-connector-hla-vector.md) .

<table id="table_ttp_1wb_c3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Name

</td><td>

Unique name of this integration. For example: My Vector Agent integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

</td></tr><tr><td>

MID server name

</td><td>

The MID Server to which the Vector Agent logs are streamed. This field is required.**Note:**

-   You can select only MID Servers that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of integrations streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.
-   If log ingestion is not enabled for the selected MID Server, Health Log Analytics enables it automatically.
-   If the MID Server is down or the connection is lost, the Vector pipeline may get blocked.

</td></tr><tr><td>

Port

</td><td>

The port on the MID Server. This field is required.Choose a port within the range 6000-6200 from the array. The port must not be occupied by another process. Make sure that your organization’s security team opens the selected port on the MID Server.

</td></tr><tr><td>

Transport

</td><td>

The protocol used for streaming log messages to your ServiceNow instance: TCP.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr></tbody>
</table>**Parent Topic:**[Integration configuration field descriptions](../concept/hla-connector-config-fields.md)

