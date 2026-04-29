---
title: OAuth API request parameters
description: Learn about the OAuth API request parameters that access token requests use.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create an endpoint for clients to access the instance, Old Inbound integrations experience, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# OAuth API request parameters

Learn about the OAuth API request parameters that access token requests use.

**Note:** The content-type of the OAuth API should be application/x-www-form-urlencoded. A content-type of application/json results in an unspecified error.

<table id="table_awk_zyv_yq"><thead><tr><th>

Request parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

grant\_type

</td><td>

\[Required\] The type of credentials authorizing the request for an access token. This parameter must have one of the following values:-   **password**: A set of user credentials to authorize the access token request. Specify the user credentials in the username and password parameters.
-   **refresh\_token**: An existing refresh token authorizes the access token request. Specify the refresh token in the refresh\_token parameter.

</td></tr><tr><td>

client\_id

</td><td>

\[Required\] Auto-generated unique ID of the client application requesting the access token.

</td></tr><tr><td>

client\_secret

</td><td>

\[Required\] Shared secret string that the instance and the OAuth application use to authorize communications with one another.

</td></tr><tr><td>

username

</td><td>

User account name that authorizes the access token request. This parameter is required for access token requests with a **grant\_type** of **password**.

</td></tr><tr><td>

password

</td><td>

Password for the user account that authorizes the access token request. This parameter is required for access token requests with a **grant\_type** of **password**.

</td></tr><tr><td>

refresh\_token

</td><td>

Existing refresh token that authorizes the access token request. This parameter is required for access token requests with a **grant\_type** of **refresh\_token**.

</td></tr></tbody>
</table>## Requests Using User Credentials

The instance requires clients to provide user login credentials when first authorizing the client or when authorizing the creation of a new refresh token. This type of request always returns two tokens:

-   An access token
-   A refresh token

The instance verifies that the user is active, not currently locked out, and has an interactive session. If any of these conditions are false, the instance does not produce an access token. Access requests made within the expiration time of the access token always return the current access token.

**Note:** This type of authorization grant relies on TLS encryption to protect the user credentials during transmission.

The following example illustrates requesting an access token with a set of user credentials \(Spaces have been added to improve readability\).

```

$ curl -d"grant_type=password&client_id=be3aeb583ace210011c15b24a43e25d8
&client_secret=client_password
&username=admin&password=admin" 
https://instancename.service-now.com/oauth_token.do
```

## Requests Using a Refresh Token

The instance can use an existing refresh token to create a new access token. This type of request returns only an access token. The instance confirms that the refresh token has not expired before generating a new access token. Access requests made within the refresh token expiration time always return the current refresh token. Transmitting refresh tokens is generally more secure than transmitting user credentials. The following example illustrates requesting an access token with an existing refresh token \(Spaces have been added to improve readability\).

```

$ curl -d"grant_type=refresh_token&client_id=be3aeb583ace210011c15b24a43e25d8
&client_secret=client_password
&refresh_token=w599voG89897rGVDmdp12WA681r9E5948c1CJTPi8g4HGc4NWaz62k6k1K0FMxHW40H8yOO3Hoe" 
https://instancename.service-now.com/oauth_token.do
```

