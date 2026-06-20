---
title: Enable OAuth with inbound REST
description: Using OAuth, you can pass a user ID and password once, and then use a token for subsequent REST requests instead of submitting credentials with each request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/api-reference/rest-api-explorer/t\_EnableOAuthWithREST.html
release: yokohama
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [REST APIs, Web services, API implementation, API implementation and reference]
---

# Enable OAuth with inbound REST

Using OAuth, you can pass a user ID and password once, and then use a token for subsequent REST requests instead of submitting credentials with each request.

## About this task

OAuth can improve system security by reducing the number of times you submit user credentials. You can use OAuth to authenticate REST requests.

## Procedure

1.  Activate the OAuth 2.0 plugin.

    See  to learn how to activate plugins.

2.  Set the system property **com.snc.platform.security.oauth.is.active** to true.

3.  Navigate to **System OAuth &gt; Application Registry**.

4.  Click **New** and then click **Create an OAuth API endpoint for external clients**.

5.  Record the **client\_id** and **client\_secret** values from the previous step to use when requesting an access token.

    **Note:** The example shown is about creating OAuth API endpoint using password grant type. You can also configure OAuth API endpoint using other grant types. For more information, see .

6.  To get an access token, use your REST client, such as cURL or Postman, to send a request to the OAuth endpoint \(`oauth_token.do`\).

    Format the request as a URL-encoded HTTP POST body and include the required parameters.

7.  Record the access token and refresh token from the response.

8.  Submit the access token with subsequent REST requests.


-   **[REST OAuth example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/api-reference/rest-api-explorer/r_RESTOAuthExample.md)**  
This example shows how to authenticate an inbound REST request using OAuth.

**Parent Topic:**[REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/api-reference/rest-api-explorer/c_RESTAPI.md)

