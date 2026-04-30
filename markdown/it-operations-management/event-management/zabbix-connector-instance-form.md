---
title: Zabbix connector instance form
description: The Zabbix connector instance form displays the fields you must fill in when creating a Zabbix connector instance.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-03-28"
reading_time_minutes: 1
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Zabbix connector instance form

The Zabbix connector instance form displays the fields you must fill in when creating a Zabbix connector instance.

<table id="table_byp_mhz_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the Zabbix metric connector instance.

</td></tr><tr><td>

Description

</td><td>

Brief explanation of the purpose or use of the connector instance.

</td></tr><tr><td>

Connector Definition

</td><td>

Connector definition to be used by the connector.Select **Zabbix Metrics**.

</td></tr><tr><td>

Host IP

</td><td>

Host IP address of the host where the Zabbix server collects metrics.

</td></tr><tr><td>

Credential

</td><td>

Credentials required to access the Zabbix database. Select the search icon and select the Basic Auth credential.

-   Name: Provide the unique name for Zabbix cred.
-   UserName: Provide Zabbix server username
-   Password: Provide Zabbix server password
-   Select **Submit**.

</td></tr><tr><td>

Metric collection

</td><td>

Option is pre-selected and read-only.

</td></tr><tr><td>

Metric collection schedule \(seconds\)

</td><td>

Time interval \(in seconds\) at which the connector retrieves metrics from the Zabbix server.Default: 60 seconds.

</td></tr><tr><td>

Active

</td><td>

Option to activate the connector instance.

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

