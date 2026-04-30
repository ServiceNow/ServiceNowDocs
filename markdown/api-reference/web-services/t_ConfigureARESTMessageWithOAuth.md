---
title: Configure a REST message with OAuth
description: You can configure an outbound REST message to send OAuth credentials with the request.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Outbound REST authentication, Outbound REST web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Configure a REST message with OAuth

You can configure an outbound REST message to send OAuth credentials with the request.

## Before you begin

Role required: web\_service\_admin and oauth\_admin

Before starting this procedure, ensure:

-   There is a REST Message record that you want to configure to use OAuth.
-   There is an OAuth provider set up in the OAuth application registry with the OAuth client information to use. For more information, see [OAuth 2.0](https://www.servicenow.com/docs/access?context=c_OAuthApplications&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
-   The OAuth provider has an associated OAuth 2.0 profile.
-   The REST message HTTP Methods are not configured to use a MID Server.

**Note:** Ensure any scripts that call this REST message use the RESTMessageV2 API. The RESTMessageV2 API is required to send authenticated REST messages via scripts.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message**.

2.  Select a REST message record.

3.  In the **Authentication type** field, select **OAuth 2.0**.

4.  In the **OAuth profile** field, select the OAuth 2.0 profile that specifies the credentials you want to send.

5.  Right-click the form header and select **Save**.

    An info message appears at the top of the form indicating that you must request a new OAuth token.

6.  Click the **Get OAuth Token** related link.

    Depending on your OAuth provider, a separate window from your provider may appear asking for confirmation before providing a token. Complete any steps required by the provider to obtain the token.


## What to do next

Test the REST message to ensure you receive the expected response. You can optionally specify different authentication settings for each HTTP method related to this REST message, overriding the parent REST message settings.

-   **[Use a third-party OAuth provider](../../../administer/security/task/t_UseAThirdPartyOAuthProvider.md)**  
Each client application must register with the instance to participate in OAuth authorization.
-   **[Outbound REST with OAuth 2.0 profile tutorial - integrating with Google Contacts API](../concept/c_OAuth2ProfileTutorialGoogle.md)**  
This tutorial explains how to use an OAuth 2.0 profile to authenticate an outbound REST message with Google to retrieve contact information.

**Parent Topic:**[Outbound REST authentication](../concept/c_OutboundRESTAuth.md)

