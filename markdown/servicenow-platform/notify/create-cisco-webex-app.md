---
title: Create a Cisco Webex app
description: Create an app in Cisco portal to make outbound calls from an incident using Webex.
locale: en-US
release: zurich
product: Notify
classification: notify
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Notify Cisco Webex Connector, Configure, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a Cisco Webex app

Create an app in Cisco portal to make outbound calls from an incident using Webex.

## Before you begin

Role required: Cisco admin

## Procedure

1.  Log in to Cisco admin portal.

2.  Navigate to **Start Building Apps** &gt; **Start Building Apps** &gt; **Create a New App** &gt; **Create an Integration**.

3.  On the form, fill the details for the integration app.

    1.  **Will this integration use a mobile SDK**: Select **No**.

    2.  **Integration name**: Option to provide the name for the Notify with Cisco Webex app.

    3.  **Icon**: Option to choose an icon for the app.

        Select upload to select an icon for the Cisco Webex app.

    4.  **Description**: A brief description of the app.

    5.  **Redirect URI\(s\)**: URL of your ServiceNow instance.

        The URL should be of the format: "http://&lt;instance\_url&gt;/oauth\_redirect.do" where &lt;instance\_url&gt; is your instance URL.

    6.  **Scopes**: Option to select the scopes that are required for conference calls.

        Select **meeting:admin\_participants\_read**, **meeting:admin\_schedule\_read**, **meeting:admin\_schedule\_write**, and **spark:all**.

    7.  Select **Add Integration**.

        The app is successfully created. Save the **Client ID** and **Client Secret** by clicking on the **Copy** button in a notepad.

        You must update the **Client ID** and **Client Secret** values in your ServiceNow instance.


**Parent Topic:**[Configure Notify Cisco Webex Connector](../concept/setup-cisco-webex-notify.md)

