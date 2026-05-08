---
title: REST API integration configuration fields
description: Description of the fields on the REST API integration configuration forms for Health Log Analytics.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [REST API, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Integration configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# REST API integration configuration fields

Description of the fields on the REST API integration configuration forms for Health Log Analytics.

For the REST API integration setup procedure, see [Set up a REST API integration for Health Log Analytics](../task/il-connector-hla-rest-api.md).

**Note:** REST API integrations support only UTF-8 encoding for incoming data.

<table id="table_cvy_5yl_ndc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Name

</td><td>

Unique name of this integration. For example: My REST API integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

</td></tr><tr><td>

MID web server

</td><td>

The MID Web Server to use. This field is required.

</td></tr><tr><td>

Service instance

</td><td>

The service instance \(formerly the application service\) to which to bind the log data. This field is required.**Note:** If no relevant service instance exists, Create a service instance and add CIs \(Configuration Items\) to it. Set the status of the new service instance to Operational.

</td></tr><tr><td>

Transport

</td><td>

The protocol used for streaming log messages to your ServiceNow instance: REST. This field is read-only.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr><tr><td>

MID server name

</td><td>

The MID Server to which the log data is pushed.This field is auto-populated when the MID Web Server is chosen. It is read-only.

</td></tr><tr><td>

Port

</td><td>

The port for the MID Server.This field is read-only. It is auto-populated when the MID Web Server is chosen.

</td></tr></tbody>
</table>**Parent Topic:**[Integration configuration fields](../concept/hla-connector-config-fields.md)

