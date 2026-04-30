---
title: Set up SSH credentials to the MID Server
description: Palo Alto Networks Firewall sends API calls to the MID Server. As such, ensure that SSH credentials have been created for the MID Server.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Palo Alto Networks - Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up SSH credentials to the MID Server

Palo Alto Networks Firewall sends API calls to the MID Server. As such, ensure that SSH credentials have been created for the MID Server.

## Before you begin

-   The Orchestration plugin must be activated.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Orchestration** &gt; **Credentials &amp; Connections** &gt; **Credentials**.

2.  Click **New**.

3.  In the Interceptor screen, click **SSH Credentials**.

4.  Fill in the fields, as needed.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name for the credential.|
    |Active|Select this check box to activate this credential.|
    |Applies to|Select **All MID servers** or **Specific MID servers**.|
    |MID Servers|If you selected **Specific MID servers**, click the lock icon and select the MID Servers you want to apply these credentials to.|
    |Order|Select the order to which the credentials are tried by the server. Smaller numbers are tried first.|
    |User name|Enter the user name of the user associated with these credentials, if any.|
    |Password|If you entered a **User name**, enter the user's password.|
    |Tag|Enter a tag to be used for search criteria. The **Tag** field should contain the same value as the **Name**.|


