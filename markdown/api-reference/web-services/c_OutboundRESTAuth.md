---
title: Outbound REST authentication
description: Outbound REST messages support multiple types of authentication.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [REST, Outbound, Web services, API implementation, API implementation and reference]
---

# Outbound REST authentication

Outbound REST messages support multiple types of authentication.

Different web service providers may require a specific type of authentication. Outbound REST supports the following authentication formats.

-   Basic authentication using a username and password
-   OAuth 2.0 using an OAuth provider and profile
-   Mutual authentication using protocol profiles

## Limitations of RESTMessage

The following capabilities are supported in the REST Step \(IntegrationHub\) but are not available in the RESTMessageV2 scripted API:

|Limitation|Description|
|----------|-----------|
|Mutual authentication on MID Server|mTLS \(client certificate authentication\) is not supported when routing REST calls through a MID Server. Mutual authentication via RESTMessageV2 is supported only for direct instance calls.|
|Multipart with attachments|Multipart Content-Type requests for sending file attachments are not supported.|
|Custom authentication \(Authentication Algorithm\)|Custom authentication profiles using the Authentication Algorithm framework are not available.|
|AWS authentication \(Authentication Algorithm\)|AWS Signature Version 4 authentication via the Authentication Algorithm framework is not supported.|
|Retry policy for outbound calls|Built-in configurable retry policies for automatic retries on transient failures are not available. Custom retry logic must be implemented in script.|

**Note:** You can use the REST Step on IntegrationHub for these capabilities.

## Overriding REST authentication

You can define authentication for a REST message, or individually for each HTTP method. HTTP methods inherit authentication from their parent REST message record when the HTTP method **Authentication type** is **Inherit from parent**, which is the default value.

You can disable authentication for a specific HTTP method by setting the **Authentication type** field to **No authentication**, or specify authentication that is different from the parent REST message by selecting basic auth or OAuth.

## Authentication requirements

Authentication requirement for REST Outbound are as follows:

-   Outbound REST supports mutual authentication only when using basic authentication. Mutual authentication is not available with OAuth 2.0.
-   OAuth 2.0 can be used only with messages that are not configured to use a MID Server. You cannot send OAuth 2.0 authenticated messages through a MID Server. Also, mutual authentication is not supported with MID Server.
-   When scripting new REST messages configured with authentication you must use the RESTMessageV2 API. The legacy RESTMessage APIs do not support current authentication formats.
-   AWS credentials or any other custom authentication are supported only with the [REST step](https://www.servicenow.com/docs/access?context=rest-request-action-designer&version=australia&pubname=australia-integrate-applications&ft:locale=en-US), not with the RestMessage API.

-   **[Configure a REST message with basic auth](../task/t_ConfigureRESTMsgBasicAuth.md)**  
Configure an outbound REST message to provide basic authentication credentials with each request.
-   **[Configure a REST message with OAuth](../task/t_ConfigureARESTMessageWithOAuth.md)**  
You can configure an outbound REST message to send OAuth credentials with the request.
-   **[Outbound REST mutual authentication](c_OutboundRESTMutualAuthentication.md)**  
Mutual authentication causes the web service provider and consumer to authenticate with each other before communicating.

**Parent Topic:**[Outbound REST web service](c_OutboundRESTWebService.md)

