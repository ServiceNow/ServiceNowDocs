---
title: REST API data input configuration fields
description: Description of the fields on the REST API data input configuration form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/health-log-analytics/hla-data-input-rest-api-ref.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Data input configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# REST API data input configuration fields

Description of the fields on the REST API data input configuration form.

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

Optional description of the data input.

</td></tr><tr><td>

MID Web Server

</td><td>

MID Server to which the log data is pulled. This field is required.**Note:**

-   When you select the MID Web Server, the **MID** and **Port** fields are completed automatically.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. This field is required.Selecting the service instance enables HLA to correlate CIs and service instances in the CMDB for root cause analysis.

**Note:** If no appropriate service instance exists, create one, add CIs to it, and set its status to Operational. For more information, see [Create a Service instance \(application service\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/create-it-services.md).

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Status|Status of the data input. This field is read-only.|
|Transport|Protocol used to stream the log data: REST. This field is read-only.|
|Sources count|The number of log sources this data input has created. This field is read-only.|
|Disabled since|The time when the data input stopped or failed. This field is read-only.|
|MID last receiving time|The time when the last log streamed in the data input.|

**Parent Topic:**[Data input configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/health-log-analytics/hla-data-input-config-fields.md)

