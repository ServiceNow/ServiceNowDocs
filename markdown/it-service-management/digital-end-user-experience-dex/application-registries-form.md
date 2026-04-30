---
title: Application Registries form
description: The Application Registries form presents elaborate data on the form's fields and their corresponding descriptions.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [DEX Desktop Assistant reference, Reference, Digital End-User Experience, IT Service Management]
---

# Application Registries form

The Application Registries form presents elaborate data on the form's fields and their corresponding descriptions.

You must have the Desktop Assistant administrator \[sn\_dex\_desktop.admin\] role to access the form.

<table id="table_vjt_js4_1xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the application.

</td></tr><tr><td>

Client ID

</td><td>

Unique identifier for your application that is issued by the service provider.

</td></tr><tr><td>

Client Secret

</td><td>

Secret key that is used to authenticate your application with the service provider's API.

</td></tr><tr><td>

Redirect URL

</td><td>

URIs that the service provider should redirect the user to after authentication is complete. This is where your application receives the authorization code or access token.

</td></tr><tr><td>

Logo URL

</td><td>

URL of your application's logo image.

</td></tr><tr><td>

Public Client

</td><td>

Option to indicate whether the application is publicly accessible. Examples of public clients include mobile apps, web applications, and JavaScript-based applications.

</td></tr><tr><td>

Comments

</td><td>

Additional context or information about a particular request or response.

</td></tr><tr><td>

Application

</td><td>

Client application that is requesting authorization to access a protected resource or service on behalf of a user.

</td></tr><tr><td>

Accessible from

</td><td>

IP addresses or domains that are authorized to access your OAuth client.When you register your OAuth client with a service provider, you may be required to provide a list of IP addresses or domains that are allowed to make requests to the service provider's API on behalf of your client.

</td></tr><tr><td>

Active

</td><td>

Status of an access token. When you grant your application permission to access your resources using OAuth, the service provider issues an access token that your application uses to make API requests.

</td></tr><tr><td>

Refresh Token Lifespan

</td><td>

The duration of a user's session before requiring reauthentication in your application.

</td></tr><tr><td>

Access Token Lifespan

</td><td>

Refers to the period of time during which an access token is considered valid for use by an application.

</td></tr><tr><td>

Default Grant type

</td><td>

Refers to the default method used by an OAuth 2.0 authorization server to grant access tokens to client applications.

</td></tr></tbody>
</table>To return to the OAuth details page, see [Configure Open Authorization details](../task/configure-oauth-details.md).

**Parent Topic:**[DEX Desktop Assistant reference](dex-desktop-experience-reference.md)

