---
title: Configure OAuth 2.0 authentication for the Anglepoint integration
description: Configure OAuth 2.0 authentication to enable users to access Anglepoint integration resources through APIs using OAuth tokens.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the API authentication method, Creating a connection for the Anglepoint integration, Authorized SAM Provider \(ASP\) integrations for IBM, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Configure OAuth 2.0 authentication for the Anglepoint integration

Configure OAuth 2.0 authentication to enable users to access Anglepoint integration resources through APIs using OAuth tokens.

## Before you begin

Role required: admin

## Procedure

1.  From your ServiceNow instance, create an OAuth API endpoint.

    The Anglepoint Elevate platform uses the OAuth API endpoint to request the OAuth tokens that authorize access to the Anglepoint integration resources on your ServiceNow instance.

    Refer to Create an endpoint for clients to access the instance for instructions on how to create an OAuth API endpoint.

    **Important:** After you successfully create an OAuth API endpoint, copy the values in the **Client ID** and **Client Secret** fields. Save them in a secure location for later use.

2.  From the Anglepoint Elevate platform, create an API connection to your ServiceNow instance.

    The API connection enables you to securely transfer data between the Anglepoint Elevate platform and your ServiceNow instance.


## Result

The Anglepoint Elevate platform sends the credential information that you specified for your API connection to `https://*&lt;servicenow-instance-url&gt;*.service-now.com/oauth_token.do` using an HTTP Post request. Your ServiceNow instance responds to the request by generating OAuth tokens and then sending them to the Anglepoint Elevate platform. The Anglepoint Elevate platform can then use these tokens to make API requests for accessing the Anglepoint integration resources on your ServiceNow instance.

**Parent Topic:**[Configuring the API authentication method for the Anglepoint integration](../concept/configuring-auth-method-anglepoint-integration.md)

