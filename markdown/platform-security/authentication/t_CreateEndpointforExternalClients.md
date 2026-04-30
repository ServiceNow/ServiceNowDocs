---
title: Create an endpoint for clients to access the instance
description: Create an OAuth application endpoint for external client applications to access the ServiceNow instance.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Old inbound integrations experience, OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Create an endpoint for clients to access the instance

Create an OAuth application endpoint for external client applications to access the ServiceNow instance.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry** and then click **New**.

2.  On the interceptor page, click **Create an OAuth API endpoint for external clients** and then fill in the form.

<table id="table_sgc_qqv_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name that identifies the application that you require OAuth access for.

</td></tr><tr><td>

Client ID

</td><td>

\[Read-Only\] The auto-generated unique ID of the application. The instance uses the client ID when requesting an access token.

</td></tr><tr><td>

Client Secret

</td><td>

\[Required\] The shared secret string that both the instance and the client application or website use to authorize communications with one another. The instance uses the client secret when requesting an access token. Leave this field blank to have the instance auto-generate a client secret. To display existing client secrets, click the lock icon.

</td></tr><tr><td>

Redirect URL

</td><td>

The callback URL that the authorization server redirects to. Enter the full URLs of the clients requesting access to the resource, appended by `/oauth_redirect.do`. For example, `http://token_consumer:port/oauth_redirect.do`. Enter as many URLs as needed for all possible token consumers. The instance matches the URL of the incoming request to one of the redirect URLs. If no match is made, the instance uses the first redirect URL.

</td></tr><tr><td>

Logo URL

</td><td>

The URL that contains an image to use as the application logo. The logo appears on the approval page when the user receives a request to grant a client application access to a restricted resource on the instance.

</td></tr><tr><td>

Active

</td><td>

Select the check box to make the application registry active.

</td></tr><tr><td>

Refresh Token Lifespan

</td><td>

The number of seconds that a refresh token is valid. The instance uses the lifespan value when requesting a refresh token. By default, refresh tokens expire in 100 days \(8640000 seconds\).

</td></tr><tr><td>

Enforce Token Restrictions

</td><td>

Select to only allow tokens to be used with APIs set to allow the authentication profile. You can set grant access using an API access policy. For more information, see [Create REST API access policy](../../../integrate/authentication/task/create-api-access-policy.md).Default: Unselected.

</td></tr><tr><td>

Mobile Client

</td><td>

Represents the entity for mobile app or web. This information is used to analyze the login information with mobile or web.

</td></tr><tr><td>

Access Token Lifespan

</td><td>

The number of seconds that an access token is valid. The instance uses the lifespan value when requesting an access token. By default, access tokens expire in 30 minutes \(1800 seconds\).

</td></tr><tr><td>

Token Format

</td><td>

Format of the token to generate. The format determines the structure of a token and the information it includes.

</td></tr><tr><td>

Subject Claim

</td><td>

Field in the User \(sys\_user\) table that's used to populate the value of the subject \(sub\) claim of a JWT token. The sub claim is a piece of information that identifies the subject, or user, of the JWT token. This field only applies if the **Token Format** is JWT.

</td></tr><tr><td>

Comments

</td><td>

Additional information to associate with the application.

</td></tr><tr><td>

Client Type

</td><td>

Choose the client type, based on the type of your client. Options:-   **Iframe Embedded**
-   **Integration as a User**
-   **Integration as a Service**
To know more, see [Configure client type for OAuth and SSO records](../../../integrate/authentication/concept/client-type.md).

</td></tr></tbody>
</table>3.  Click **Submit**.


## Result

The system creates a record in the Application Registries \[oauth\_entity\] table with of type OAuth Client. When the instance actually issues tokens and authorization codes, they are stored in the table. See [Manage OAuth tokens](t_ManageTokens.md) for more information.

