---
title: Install the application and configure a source for the integration
description: Install and configure the Microsoft Defender for Endpoint integration from the ServiceNow Store on your ServiceNow AI Platform instance. Start creating capability profiles using the configurations.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install the application and configure a source for the integration

Install and configure the Microsoft Defender for Endpoint integration from the ServiceNow Store on your ServiceNow AI Platform instance. Start creating capability profiles using the configurations.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Download the Microsoft Defender for Endpoint integration from the ServiceNow Store and install it.

2.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

3.  Search for the Microsoft Defender for Endpoint tile, and click **Configure**.

4.  On the form, fill in the following fields.

    | | |
    |---|---|
    |Name|Name for the Microsoft Defender for Endpoint instance configuration.|
    |Base URL|The service base URL for Microsoft Defender for Endpoint|
    |Tenant ID|The Microsoft Defender for Endpoint Tenant ID. All actions would be performed on this instance.|
    |Client ID|Client ID for the application that you have registered in the Microsoft Azure portal.|
    |Client Secret|Client secret for your registered application.|

5.  Click **Submit**.

    ![Install the application and configure a source for the integration](../image/ms_defender_tile.png "Install and configure the application")


## Result

The Microsoft Defender for Endpoint configurations list is displayed with your new configuration record. You have completed the configuration for the Microsoft Defender for Endpoint.

