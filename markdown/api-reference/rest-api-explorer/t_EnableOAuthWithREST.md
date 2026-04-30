---
title: Enable OAuth with inbound REST
description: Using OAuth, you can pass a user ID and password once, and then use a token for subsequent REST requests instead of submitting credentials with each request.
locale: en-US
release: zurich
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [REST APIs, Web services, API implementation, API implementation and reference]
---

# Enable OAuth with inbound REST

Using OAuth, you can pass a user ID and password once, and then use a token for subsequent REST requests instead of submitting credentials with each request.

## About this task

OAuth can improve system security by reducing the number of times you submit user credentials. You can use OAuth to authenticate REST requests.

This video demonstrates how to authenticate to REST APIs using OAuth.

How to authenticate to REST APIs using OAuth

## Procedure

1.  Activate the OAuth 2.0 plugin.

    See [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) to learn how to activate plugins.

2.  Set the system property **com.snc.platform.security.oauth.is.active** to true.

3.  Navigate to **System OAuth &gt; Application Registry**.

4.  Click **New** and then click **Create an OAuth API endpoint for external clients**.

5.  Record the **client\_id** and **client\_secret** values from the previous step to use when requesting an access token.

    **Note:** The example shown is about creating OAuth API endpoint using password grant type. You can also configure OAuth API endpoint using other grant types. For more information, see [OAuth inbound](https://www.servicenow.com/docs/access?context=oauth-inbound&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

6.  To get an access token, use your REST client, such as cURL or Postman, to send a request to the OAuth endpoint \(`oauth_token.do`\).

    Format the request as a URL-encoded HTTP POST body and include the required parameters.

7.  Record the access token and refresh token from the response.

8.  Submit the access token with subsequent REST requests.


-   **[REST OAuth example](../reference/r_RESTOAuthExample.md)**  
This example shows how to authenticate an inbound REST request using OAuth.

**Parent Topic:**[REST APIs](../concept/c_RESTAPI.md)

