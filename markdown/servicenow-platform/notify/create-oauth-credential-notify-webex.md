---
title: Create an OAuth credential record for Notify with Cisco Webex
description: Create a credential record for the Notify with Cisco Webex account.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Notify Cisco Webex Connector, Configure, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an OAuth credential record for Notify with Cisco Webex

Create a credential record for the Notify with Cisco Webex account.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill these values.

<table id="oauth-notify-webex"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, Cisco Webex Teams Cred.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

OAuth Entity Profile

</td><td>

OAuth profile created during the registration of Cisco Webex Teams as an OAuth provider. For example, Cisco Webex Teams OAuth Profile.

</td></tr><tr><td>

Applies to

</td><td>

Option to specify if the credential applies to all MID Servers in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use this credential in the **MID servers** field.

</td></tr><tr><td>

Order

</td><td>

Order to apply this credential. For example, `100`.

</td></tr><tr><td>

Credential alias

</td><td>

Credential alias associated with the spoke.

</td></tr></tbody>
</table>5.  Right-click the form header and click **Submit**.

6.  Select the **Get OAuth Token** related link.

    You must log in to Cisco Webex account to retrieve the token details.

    Enter the email address of the Cisco account that connects your ServiceNow instance with Cisco Webex portal. This email address should be unique and can’t be assigned to any user. Ex: cisco\_servicenow@webex.com.

    On successful authentication, a confirmation message is displayed on the header.


**Parent Topic:**[Configure Notify Cisco Webex Connector](../concept/setup-cisco-webex-notify.md)

