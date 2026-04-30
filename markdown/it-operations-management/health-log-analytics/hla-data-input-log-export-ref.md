---
title: ServiceNow Log Export data input configuration fields
description: Description of the fields on the ServiceNow Log Export data input configuration form.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [HLA, Health Log Analytics, ServiceNow, system logs, log data, data input, configuration, fields]
breadcrumb: [Data input configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# ServiceNow Log Export data input configuration fields

Description of the fields on the ServiceNow Log Export data input configuration form.

<table id="table_pgv_vvw_chc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the new data input. This field is required.

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data.**Important:** The service instance field is pre-populated with a value. Changing this value is necessary only if there is a compelling reason to do so. Consider the implications carefully before making any changes.

</td></tr><tr><td>

Certificate password alias

</td><td>

The credential alias you created in **Basic Auth Credentials**. This field is required.For more information, see the Before you begin section in [Configure a ServiceNow Log Export data input in Health Log Analytics manually](../task/hla-data-input-log-export.md).

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the data input to help identify it.

</td></tr><tr><td>

Log level

</td><td>

The log level indicating the severity of the log messages.The available log levels are:

-   INFO: Information messages representing service actions. This is the default log level.
-   ERROR: Non-fatal error messages.
-   WARN: Warning messages indicating potential issues.

</td></tr><tr><td>

Status

</td><td>

Status of the data input: Active or Not Active. This field is read-only.

</td></tr><tr><td>

Disabled since

</td><td>

The time when the data input stopped or failed. This field is read-only.

</td></tr></tbody>
</table>**Parent Topic:**[Data input configuration field descriptions](../concept/hla-data-input-config-fields.md)

