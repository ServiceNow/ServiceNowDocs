---
title: Add the OAuth Application User
description: Add the OAuth Application User field on the OAuth Entity form to use the Client Credentials grant type for OAuth inbound integrations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-security/authentication/add-oauth-application-user.html
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Client Credentials, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Add the OAuth Application User

Add the OAuth Application User field on the OAuth Entity form to use the Client Credentials grant type for OAuth inbound integrations.

## Before you begin

Role required: admin, oauth\_admin

Plugin required: OAuth 2.0.

You must create an OAuth client. For more information, see [Create an endpoint for clients to access the instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/authentication/t_CreateEndpointforExternalClients.md).

## Procedure

1.  Open the OAuth client record that was created.

2.  Select more options icon on the page header.

3.  Select **Configure** &gt; **Form Design**.

4.  On the Form Design page, add **OAuth Application User** from the list of fields.

5.  Save or Update the form.

6.  Select the user for the **OAuth Application User**.

    For example, System Administrator.\[Omitted image "add-oauth-application-user.png"\] Alt text: OAuth Application User

    **Note:**

    Use the [REST API Auth Scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/authentication/rest-api-auth-scope.md) to define the permissions of the client application, and control its access to the APIs.

7.  Save or Update the form.

    Any token request with the **Grant Type** as **Client Credentials**, **Client ID**, and **Secret** is passed for the associated OAuth Application User in ServiceNow®.

    **Note:** If the OAuth Application User isn’t selected on the OAuth client record or the Client Credentials property is set to `false`, then the token request will fail.


