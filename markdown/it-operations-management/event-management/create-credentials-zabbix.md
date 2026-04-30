---
title: Create Zabbix server credentials
description: Create credentials to access Zabbix server.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure event collection from Zabbix server, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create Zabbix server credentials

Create credentials to access Zabbix server.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

3.  Select **Basic Auth Credential**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique and descriptive name for this credential. For example, you might call it `Zabbix authentication`.|
    |User name|Name to identify the user.|
    |Password|Password to use this credential.|
    |Active|Option to enable the use of this credential.|
    |Order|The order \(sequence\) in which the platform tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order. Default value: `100`|

5.  Click **Submit**.


## Result

The Basic Auth credential for use with the Zabbix server connector is created.

**Parent Topic:**[Configure event collection from Zabbix server](t_EMConfigureZabbixConnector.md)

**Related topics**  


[Credentials and connection information](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

