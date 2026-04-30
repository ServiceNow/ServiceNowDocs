---
title: Create credential records for the Microsoft Exchange Online spoke
description: Authorize the Microsoft Exchange Online spoke actions by creating credential records for the application registered in the Microsoft Azure portal. The Microsoft Exchange Online connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: yokohama
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up Microsoft Office 365 integration for Walk-up Experience, Integrate Microsoft Office 365 calendar with Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Create credential records for the Microsoft Exchange Online spoke

Authorize the Microsoft Exchange Online spoke actions by creating credential records for the application registered in the Microsoft Azure portal. The Microsoft Exchange Online connection and credential alias uses these credentials to authorize actions.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message, `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the record. For example, `Exchange_Online_Credentials`.|
    |Active|Option to use the credential record.|
    |OAuth Entity Profile|OAuth profile created during the registration of Microsoft Exchange Online spoke as an OAuth provider with **Default Grant Type** as **Authorization Code**. For example, `Microsoft Exchange Online`.|
    |Applies to|MID Servers that can use this credential. For example, select **All MID Servers**.|
    |Order|Order that the credentials are used. For example, enter `100`.|

5.  Right-click the form header and click **Save**.

6.  To generate the OAuth token, click the **Get OAuth Token** related link.

7.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

8.  Click **New**.

    The system displays the message, `What type of Credentials would you like to create?`

9.  Select **OAuth 2.0 Credentials**.

10. On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the record. For example, `Exchange_Online_Credentials_clientCred`.|
    |Active|Option to use the credential record.|
    |OAuth Entity Profile|OAuth profile created during the registration of Microsoft Exchange Online spoke as an OAuth provider with **Default Grant Type** as **Client Credentials**. For example, `Microsoft Exchange Online_clientCredentials default_profile`.|
    |Applies to|MID Servers that can use this credential. For example, select **All MID Servers**.|
    |Order|Order that the credentials are used. For example, enter `100`.|

11. Right-click the form header and click **Save**.

12. To generate the OAuth token, click the **Get OAuth Token** related link.


## Result

The credential records for the Microsoft Exchange Online spoke are created.

**Parent Topic:**[Set up Microsoft Office 365 integration for Walk-up Experience](setup-walkup-msoffice365-cal-integ.md)

