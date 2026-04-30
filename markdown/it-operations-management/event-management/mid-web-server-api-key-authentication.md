---
title: Configure MID Web Server API key authentication
description: Authenticate incoming requests from clients to the MID Web Server extension using API key authentication. API authentication is a secure and simple way to authenticate your request. You can create or modify a MID Web Server API key.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure the MID Web Server extension, MID Web Server, Event Management setup, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure MID Web Server API key authentication

Authenticate incoming requests from clients to the MID Web Server extension using API key authentication. API authentication is a secure and simple way to authenticate your request. You can create or modify a MID Web Server API key.

## Before you begin

Create a MID Web Server extension to use API Key authentication, as described in [Configure the MID Web Server extension](configure-mid-web-server-extension.md). Ensure that you select **API Key** in the extension's **Authentication Type** field.

Role required: event\_mgmt\_admin

## About this task

By default, the maximum number of API keys you can create on an instance is 10. To change this number, modify the **mid.webserver.max.api.keys** property value on the System Properties page.

When working in the global domain while Domain Separation is enabled, API keys are available to all extensions, regardless of their domain. When working in a specific domain, API keys are available to extensions in that domain, its parent domains, and the global domain.

You can configure API keys to expire on a specified date.

When creating a new extension with API key authentication \(or updating an existing one to use API key authentication\), the system checks for an available API key for the extension. If there is no available API key, the system creates one.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Profiles and Deployments** &gt; **MID Web Server API Key**.

2.  Either create a new API key or modify an existing API key.

    -   To create a new API key:
        1.  Select **New**.
        2.  On the MID Web Server API Key form, fill in the fields.

<table id="table_bn5_25k_lrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the API key.

</td></tr><tr><td>

Active

</td><td>

Option for activating the API key.

</td></tr><tr><td>

Authentication key

</td><td>

Read-only encoded value of the authentication key. No value appears until after you configure the key.

</td></tr><tr><td>

Expires

</td><td>

Option for setting an expiration date for the API key.Expired, deactivated, or deleted API keys are not accepted by the web server extension.

</td></tr></tbody>
</table>        3.  Select **Submit** to save the API key.

            The API key appears on the Mid Web Server API Keys page.

    -   To modify an existing API key:
        1.  Navigate to **MID Server** &gt; **Profiles and Deployments** &gt; **MID Web Server API Key**.
        2.  Select an API key on the page.
        3.  In the **Related Links** section, select **View API Key**.
        4.  Copy the API key that appears in the MID Web Server dialog box.

            When connecting to a MID Web Server extension configured with API Key authentication, place an API key that the extension has access to in the Authorization header of the request in the following format:

            `Key <API_KEY>`

            where `<API_KEY>` is the value of the API key displayed after selecting **View API Key**.

        5.  Select **Submit**.

