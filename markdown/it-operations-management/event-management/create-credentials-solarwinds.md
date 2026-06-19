---
title: Create SolarWinds monitor credentials
description: Create a Basic Auth credential in ServiceNow to store the SolarWinds user name and password that the SolarWinds monitor connector uses to access the SolarWinds API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/create-credentials-solarwinds.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure event collection from SolarWinds monitor, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create SolarWinds monitor credentials

Create a Basic Auth credential in ServiceNow to store the SolarWinds user name and password that the SolarWinds monitor connector uses to access the SolarWinds API.

## Before you begin

-   Role required: evt\_mgmt\_admin
-   Make sure that you have a SolarWinds account with access to the SolarWinds API.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

3.  Select **Basic Auth Credential**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique and descriptive name for this credential. For example, you might call it `SolarWinds authentication`.|
    |User name|Enter the user name of the SolarWinds account that the connector uses to access the SolarWinds API.|
    |Password|Enter the password for the SolarWinds account.|
    |Active|Option to enable the use of this credential.|
    |Order|The order \(sequence\) in which the platform tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order. Default value: `100`|

5.  Click **Submit**.


## Result

The credential for use with the SolarWinds monitor connector is created.

**Parent Topic:**[Configure event collection from SolarWinds monitor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/t_EMConfigureSolarwindsConnectorJS.md)

**Related topics**  


[bundle-psec.r-credentials]

