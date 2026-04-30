---
title: Configure OAuth entity for Notify Cisco Webex
description: Configure the Cisco Webex as an OAuth provider and allow the ServiceNow instance to request OAuth 2.0 tokens.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Notify Cisco Webex Connector, Configure, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure OAuth entity for Notify Cisco Webex

Configure the Cisco Webex as an OAuth provider and allow the ServiceNow instance to request OAuth 2.0 tokens.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **Cisco Webex Teams spoke**.

3.  Update the following values in the application registry.

    -   **Client ID**: Paste the client ID generated while creating the Cisco integration app.
    -   **Client Secret**: Paste the client secret generated while creating the Cisco integration app.
    -   **Redirect URL**: Provide your instance details of your ServiceNow instance. The URL should be of the format "http://&lt;instance\_url&gt;/oauth\_redirect.do" where &lt;instance\_url&gt; is your instance URL.
4.  Select **Update**.

5.  Select **OAuth Entity Scopes** tab.

    The following scopes are available by default:

    -   meeting:admin\_participants\_read
    -   meeting:admin\_schedule\_read
    -   meeting:admin\_schedule\_write
    -   spark:all

**Parent Topic:**[Configure Notify Cisco Webex Connector](../concept/setup-cisco-webex-notify.md)

