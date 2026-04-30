---
title: Set up the Secureworks CTP spoke
description: Integrate the ServiceNow instance and Secureworks CTP by registering a custom application in Secureworks Portal to authenticate ServiceNow requests.Create a credential record for the Secureworks CTP Specify whether record is for a host, instance, server, custom application, or account: account. The Secureworks CTP spoke connection and credential alias uses these credentials to authorize actions.Modify the short description to provide spoke specific information.Create a connection record for your Secureworks account. The Secureworks CTP spoke connection and credential aliases use these connections to perform API actions in Secureworks portal.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Secureworks CTP Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Secureworks CTP spoke

Integrate the ServiceNow instance and Secureworks CTP by registering a custom application in Secureworks Portal to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Secureworks CTP spoke.
-   Create an API password from the Account Management section of your Secureworks CTP account.
-   Role required: admin.

## Create a credential record for the Secureworks CTP spoke

Create a credential record for the Secureworks CTP account. The Secureworks CTP spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **API Key Credentials**.

4.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, enter `Secureworks Cred`|
    |Active|Option to actively use the credential record.|
    |API Key|API key generated in your Secureworks account. Enter the API key in this format: `APIKEY username:password`|
    |Applies to|MID Servers that can use this credential.|
    |Order|Sequence in which the credential is applied.|
    |Credential alias|Alias to use the credential. Click the padlock icon and enter `sn_sw_ctp_spoke.Secureworks`|

5.  Right-click the form header and click **Submit**.


## Create a connection record for the Secureworks CTP spoke

Create a connection record for your Secureworks account. The Secureworks CTP spoke connection and credential aliases use these connections to perform API actions in Secureworks portal.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record for **Secureworks**.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `Secureworks Connection`.|
    |Credential|Credential record created for Secureworks CTP spoke. Enter the credential you created. For example`Secureworks Cred`.|
    |Connection alias|Alias record associated with this connection. The default alias is `sn_sw_ctp_spoke.Secureworks`.|
    |Connection URL|Base URL to connect to **Secureworks**. Enter: `https://api.secureworks.com`|
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|

5.  Click **Submit**.


