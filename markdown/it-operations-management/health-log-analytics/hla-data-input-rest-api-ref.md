---
title: REST API data input configuration fields
description: Description of the fields on the REST API data input configuration form.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data input configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# REST API data input configuration fields

Description of the fields on the REST API data input configuration form.

## Basic configuration

<table id="table_xy2_chq_z4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the new data input. This field is required.

</td></tr><tr><td>

Description

</td><td>

Description of the data input.

</td></tr><tr><td>

MID Web Server

</td><td>

MID Server to which the log data is pulled.**Note:**

-   You can select only MID Servers that support basic authentication. MID Servers that support mTLS are not listed. When you select the MID Server, the **MID** and **Port** fields are completed automatically.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.

This field is required.

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. **Note:** If no relevant service instance exists, [Create an service instance](https://www.servicenow.com/docs/access?context=create-it-services&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) and add CIs to it. Set the status of the new service instance to Operational.

This field is required.

</td></tr></tbody>
</table>The following fields show read-only information:

<table id="table_fpc_shq_z4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status

</td><td>

Status of the data input.

</td></tr><tr><td>

Transport

</td><td>

Protocol used to stream the log data.This data input uses REST to stream log data to your instance.

</td></tr><tr><td>

Sources count

</td><td>

The number of log sources this data input has created.

</td></tr><tr><td>

Disabled since

</td><td>

The time when the data input stopped or failed.

</td></tr><tr><td>

Last log time

</td><td>

The time when the last log streamed in the data input.

</td></tr></tbody>
</table>**Parent Topic:**[Data input configuration field descriptions](../concept/hla-data-input-config-fields.md)

