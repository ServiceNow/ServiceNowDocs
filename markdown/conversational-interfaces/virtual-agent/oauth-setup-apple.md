---
title: OAuth setup for Apple Messages for Business
description: Integrate your Identity Provider \(IdP\) with Apple Messages for Business using OAuth2 authentication.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Conversational Integration with Apple Messages for Business, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# OAuth setup for Apple Messages for Business

Integrate your Identity Provider \(IdP\) with Apple Messages for Business using OAuth2 authentication.

## Connect Apple Messages for Business to your ServiceNow® instance

Complete the following steps on the Apple Messages for Business site to connect your Apple Messages for Business account to your ServiceNow® instance.

1.  Go to the Apple Messages for Business page \(register.apple.com\) and log in to your Messages for Business account.
2.  Go to the **Integrated OAuth2 Authentication** section.
3.  Add the Authorization URL from your Identity Provider \(IdP\) to the **OAuth URL** field.
4.  Add the Token URL from your IdP to the **Token URL** field.
5.  Add the Client ID from your IdP to the **Client Identifier** field.
6.  Refer to the [Apple documentation](https://register.apple.com/resources/messages/msp-rest-api/type-interactive#authentication-message) for further instructions on configuring OAuth2 authentication on your Apple Messages for Business account.

## Set up OAuth on your ServiceNow® instance

1.  Go to your ServiceNow® instance to set up OAuth.
2.  Create a new record in the Application Registries \(oauth\_entity\) table using these instructions: [Use a third-party OAuth provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/t_UseAThirdPartyOAuthProvider.md).
    -   Use the grant type **Authorization code**.
    -   Add the **Token URL**.
3.  Create a new record in the OAuth Entity Scopes \(oauth\_entity\_scope\) table using these instructions: [Specify an OAuth scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/t_SpecifyAnOAuthScope.md). If you have multiple scopes, then add a new record for each scope, and create a corresponding Entity Profile Scope record for each scope.
4.  Create a new record in the Connection and Credential Aliases \(sys\_alias\) table using these instructions: [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-alias.md). This connection alias is used for fetching the http connection record which you create in the next step.
5.  Create a new record in the HTTP\(s\) Connection \(http\_connection\) table using these instructions: [Create an HTTP\(s\) connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/create-https-connection.md).
    -   Type of connection - Select HTTP\(s\) Connection
    -   Set the Connection alias to the `sys_alias` record created in previous step.

    -   Set the connection url to fetch the user information API as per your IdP. \(For example:`https://<your-idp-app>.com/api/v1/users`\)
6.  Create a Profile Parser Action using Workflow Studio. See the code snippets shown here for an example: [Create a profile parser action for Apple Messages for Business](create-profile-parser-action-apple.md). See [Building actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/actions.md) for more details.
7.  Create a new record in the Provider Application Authentications \(sys\_cs\_provider\_app\_authentication\) table using these instructions:
    -   Set the Provider Channel Identity to your provider app \(`sys_cs_provider_application`\)
    -   Set the OAuth Entity Profile to the `oauth_entity_profile` record created with your OAuth Provider \(`oauth_entity`\) record.
    -   Set the Profile API Connection to the `http_connection` record created previously.

    -   Set the Profile Response Parser Action to the `sys_hub_action_type_definition` record that you have defined.

