---
title: Enable OAuth with inbound REST
description: Using OAuth, you can pass a user ID and password once, and then use a token for subsequent REST requests instead of submitting credentials with each request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/rest-api-explorer/t\_EnableOAuthWithREST.html
release: zurich
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 1
breadcrumb: [REST APIs, Web services, API implementation, API implementation and reference]
---

# Enable OAuth with inbound REST

Using OAuth, you can pass a user ID and password once, and then use a token for subsequent REST requests instead of submitting credentials with each request.

## Before you begin

The OAuth 2.0 plugin \(com.snc.platform.security.oauth.is.active\) must be active. For activation instructions, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_ActivateAPlugin.md).

Role required: admin

## About this task

OAuth reduces the number of times you submit user credentials. After authenticating once, you use a token for subsequent REST requests.

## Procedure

1.  Set the **com.snc.platform.security.oauth.is.active** system property to `true`.

2.  Navigate to **System OAuth** &gt; **Application Registry**.

3.  Select **New**, then select **Create an OAuth API endpoint for external clients**.

4.  Record the **client\_id** and **client\_secret** values to use when requesting an access token.

    **Note:** This example uses the password grant type. You can also configure an OAuth API endpoint using other grant types. For more information, see [OAuth inbound](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/authentication/oauth-inbound.md).

5.  Use a REST client, such as cURL or Postman, to send a POST request to the OAuth endpoint \(`oauth_token.do`\).

    Format the request as a URL-encoded HTTP POST body and include the required parameters.

6.  Record the access token and refresh token from the response.

7.  Submit the access token with subsequent REST requests.


-   **[REST OAuth example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/rest-api-explorer/r_RESTOAuthExample.md)**  
This example shows how to authenticate an inbound REST request using OAuth.

**Parent Topic:**[REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/rest-api-explorer/c_RESTAPI.md)

