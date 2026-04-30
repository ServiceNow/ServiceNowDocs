---
title: Edge Delta REST integration configuration fields
description: Description of the fields on the Edge Delta REST integration configuration form for Health Log Analytics.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Edge Delta, REST, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Integration configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Edge Delta REST integration configuration fields

Description of the fields on the Edge Delta REST integration configuration form for Health Log Analytics.

For the Edge Delta REST integration setup procedure, see [Set up an Edge Delta REST integration for Health Log Analytics](../task/il-connector-hla-edgedelta-rest.md).

<table id="table_vkg_k5h_chc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration name

</td><td>

Unique name of this integration. For example: My Edge Delta REST integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

</td></tr><tr><td>

MID web server

</td><td>

The MID Web Server to use. This field is required.

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. This field is required.

</td></tr><tr><td>

Port

</td><td>

The port for the MID Server.This field is read-only. It is auto-populated when the MID Web Server is chosen.

</td></tr><tr><td>

Transport

</td><td>

The transport method used for streaming log messages to your ServiceNow instance: REST. This field is read-only.

</td></tr><tr><td>

MID server name

</td><td>

The MID Server to which the log data is pushed.This field is auto-populated when the MID Web Server is chosen. It is read-only.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr></tbody>
</table>**Parent Topic:**[Integration configuration field descriptions](../concept/hla-connector-config-fields.md)

