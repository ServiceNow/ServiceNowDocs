---
title: Dynatrace connector instance form
description: The Dynatrace connector instance form displays the fields you must fill in when creating a Dynatrace connector instance.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Event Management reference, Event Management, ITOM Health, IT Operations Management]
---

# Dynatrace connector instance form

The Dynatrace connector instance form displays the fields you must fill in when creating a Dynatrace connector instance.

<table id="table_byp_mhz_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the Dynatrace metric connector instance.

</td></tr><tr><td>

Description

</td><td>

Description for the use of connector instance.

</td></tr><tr><td>

Connector Definition

</td><td>

The connector definition to be used by the connector.Select **Dynatrace Metrics**.

</td></tr><tr><td>

Host IP

</td><td>

Hostname/IP address of the Dynatrace server.

</td></tr><tr><td>

Credential

</td><td>

Select the search icon and select the existing API key credential.If this credential does not exist, create a new credential, as follows:

1.  Ensure that you have an access token with Read Metric \(metrics.read\) permissions, created on the Dynatrace UI.
2.  Select **New** after selecting the search icon.
3.  Select **API Key Credentials**.
4.  In the **API Key** field, enter the access token from the Dynatrace UI.
5.  In the **Name** field, enter a descriptive name to uniquely identify the credential.
6.  Fill in any other relevant fields, and select **Submit**.

</td></tr><tr><td>

Metric collection

</td><td>

Selected by default. Read-only.

</td></tr><tr><td>

Metric collection schedule \(seconds\)

</td><td>

Time interval \(in seconds\) at which the metric connector pulls metrics from the Dynatrace server. Default: 60.

</td></tr><tr><td>

Active

</td><td>

Select to activate the connector instance.

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

