---
title: OAuth implicit grants
description: ServiceNow instances support the implicit grant of an access token.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# OAuth implicit grants

ServiceNow instances support the implicit grant of an access token.

The implicit grant type, also known as **implicit grant code flow**, allows the access token to be given directly to the client application via the user agent, which is typically the web browser or mobile device. No refresh tokens are granted. The end user must still grant access to the protected resource on the instance, just as with standard .

## OAuth implicit grant flow process

Just as with the standard authorization code flow process, the client application makes a request to use the restricted resource on the instance and the end user approves it. The request is in the form of a URL sent to the instance. The URL must include the following parameters:

-   `client_id=<the necessary client ID>`. This is mandatory to identify which protected resource the client application wants access to.
-   `response_type=token`. This is mandatory to request the access token directly \(as opposed to asking for an authorization code\). The value must be `token` for implicit grants. In the standard authorization code flow example, the response type is `code`.
-   `redirect_uri=<a URL>`: The location where the token is sent.

The authorization server sends the access token, rather than an authorization code, to client application via the user agent.

Here is an example GET request to receive the JSON payload of data for the Incident \[incident\] table:

```
https://myinstance.servicenow.com/oauth_auth.do?response_type=token&redirect_uri={the_redirect_url}&client_id={the_client_identifier}
```

If the user grants access, the token is included in the redirect \(callback\) URL:

```
https/http://{callbackURL}?access_token={the_token}
```

