---
title: Datadog connector instance form
description: The Datadog connector instance form displays the fields you must fill in when creating a Datadog connector instance.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-10-29"
reading_time_minutes: 1
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Datadog connector instance form

The Datadog connector instance form displays the fields you must fill in when creating a Datadog connector instance.

<table id="table_byp_mhz_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the Datadog metric connector instance.

</td></tr><tr><td>

Description

</td><td>

Description for the use of connector instance.

</td></tr><tr><td>

MID Server

</td><td>

Select the MID Server configured with the Datadog capability.

</td></tr><tr><td>

Credential

</td><td>

Select the API Key Credential that you made in the authentication step.If this credential does not exist, create a new credential, as follows:

1.  Ensure that you have an access token with Read Metric \(metrics.read\) permissions, created on the Datadog UI.
2.  Select **New** after selecting the search icon.
3.  Select **API Key Credentials**.
4.  In the **API Key** field, enter the access token from the Datadog UI.
5.  In the **Name** field, enter a descriptive name to uniquely identify the credential.
6.  Fill in any other relevant fields, and select **Submit**.

</td></tr><tr><td>

Metric collection schedule \(seconds\)

</td><td>

Time interval \(in seconds\) at which the metric connector pulls metrics from the Datadog server. Default: 60.

</td></tr><tr><td>

Host IP

</td><td>

Enter the base URL for your Datadog API endpoint \(e.g., api.datadoghq.com\).

</td></tr></tbody>
</table>**Note:** For collecting cloud-native metrics \(e.g., from AWS, Azure, GCP\), it is recommended to set the collection schedule to 300 seconds \(5 minutes\). This accounts for potential data latency from the cloud provider to the Datadog platform.

To go back to the procedure page, see [Configure the Datadog metrics connector instance](../task/configure-datadog-connector.md).

**Parent Topic:**[Event Management reference](event-management-reference.md)

