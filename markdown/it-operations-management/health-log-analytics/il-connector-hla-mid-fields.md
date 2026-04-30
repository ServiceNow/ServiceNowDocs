---
title: MID Server integration configuration fields
description: Description of the fields on the MID Server integration configuration forms for Health Log Analytics.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-04-07"
reading_time_minutes: 1
keywords: [MID Server, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Configure MID Server integrations, Set up integrations from Integrations Launchpad, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# MID Server integration configuration fields

Description of the fields on the MID Server integration configuration forms for Health Log Analytics.

<table id="table_vct_hvs_32c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MID server name

</td><td>

The name of the MID Server from which the integration collects log messages and streams them to the instance. **Note:** You can only create one MID Server integration per available MID Server. If an existing MID Server integration or data input uses the same MID Server, you can't create an additional one for this MID Server.

This field is required.

</td></tr><tr><td>

Integration Name

</td><td>

The name of the integration. When you select the MID Server name, this field is auto-populated with the selected MID Server. This field is read-only.

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. This field is required. By default, it is set to ServiceNow MID Server.**Note:** This field is only available for MID Server integrations created in version 36.0.17 or later versions.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr></tbody>
</table><table id="table_acx_5vs_32c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default timezone

</td><td>

The time zone of events that the system will use if a log does not specify the time zone.By default, the system uses GMT in such cases, but you can specify a different time zone.

</td></tr><tr><td>

Sub sample drop ratio

</td><td>

The ratio of events to drop. The default value is -1.

</td></tr><tr><td>

Sub sample receive ratio

</td><td>

The ratio of events to receive. The default value is -1.

</td></tr><tr><td>

Max length in bytes

</td><td>

The maximum length of log messages, in bytes. The default value is 32,766.

</td></tr><tr><td>

Character encoding

</td><td>

The character encoding for this data input. The default value is UTF-8.

</td></tr><tr><td>

Drop if queue is full

</td><td>

Option for selecting to discard logs if many processes are waiting in the queue to access the MID Server.

</td></tr></tbody>
</table>**Parent Topic:**[Configure MID Server integrations](../task/il-connector-hla-mid.md)

