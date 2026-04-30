---
title: Create SolarWinds monitor credentials
description: Create credentials to access SolarWinds monitor.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure event collection from SolarWinds monitor, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Create SolarWinds monitor credentials

Create credentials to access SolarWinds monitor.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

3.  Select **Basic Auth Credential**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique and descriptive name for this credential. For example, you might call it `SolarWinds authentication`.|
    |User name|Name to identify the user.|
    |Password|Password to use this credential.|
    |Active|Option to enable the use of this credential.|
    |Order|The order \(sequence\) in which the platform tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order. Default value: `100`|

5.  Click **Submit**.


## Result

The credential for use with the SolarWinds monitor connector is created.

**Parent Topic:**[Configure event collection from SolarWinds monitor](t_EMConfigureSolarwindsConnectorJS.md)

**Related topics**  


[Credentials and connection information](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

