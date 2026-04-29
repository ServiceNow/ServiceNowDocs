---
title: Create credential for Microsoft Teams Communication
description: Setup credentials for Microsoft Teams Communication spoke.
locale: en-US
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connect Workplace Reservation Management with Microsoft Teams, Configure Workplace Reservation Management portal, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create credential for Microsoft Teams Communication

Setup credentials for Microsoft Teams Communication spoke.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message, `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record.|
    |Active|Option to actively use the credential record.|
    |OAuth Entity Profile|OAuth profile created in the application registration of the provider.|
    |Applies to|MID Servers that can use this credential. For example, select **All MID Servers**.|
    |Order|Order that the credentials are used. For example, enter `100`.|
    |Credential alias|Unlock, search and select the `sn_msteams_com_spk.MSTeamsCommunicationsSpoke` Connection &amp; credential alias record.|

5.  **Save** the form.

    Right-click the form header and click **Save**.

6.  To generate the OAuth token, click the **Get OAuth Token** related link.


**Parent Topic:**[Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md)

**Previous topic:**[Setup OAuth connectivity between ServiceNow and Microsoft Teams Graph](setup-connectivity-between-servicenow-and-microsoft-teams-graph.md)

**Next topic:**[Create connection and credential for Microsoft Teams Graph](create-connection-and-credentials-alias-for-microsoft-teams-graph.md)

