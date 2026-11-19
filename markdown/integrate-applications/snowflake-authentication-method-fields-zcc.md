---
title: Snowflake authentication method fields
description: Fields that appear on the New Snowflake Connection form depending on the selected authentication method.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/snowflake-authentication-method-fields-zcc.html
release: brazil
topic_type: reference
last_updated: "2026-11-12"
reading_time_minutes: 2
keywords: [Snowflake, authentication, personal authentication, zero copy connector, OAuth, JWT]
breadcrumb: [Connection form fields, Reference, Zero Copy Connectors, Workflow Data Fabric]
---

# Snowflake authentication method fields

Fields that appear on the New Snowflake Connection form depending on the selected authentication method.

## Authentication method: JWT

Select this option to use key pair authentication.

|Field|Description|
|-----|-----------|
|Private key|Private key for key pair authentication. Upload the private key file by selecting **Attach PEM file**, or copy and paste the contents of the PEM file. The content must begin with `-----BEGIN PRIVATE KEY-----` and end with `-----END PRIVATE KEY-----`.|
|Connection user|User name to connect to Snowflake.|
|Passphrase|Passphrase for the private key, if the private key is secured with a password.|
|Role|Role that determines your permissions within Snowflake.|

## Authentication method: OAuth

Select this option to use OAuth authentication, then select the OAuth credential type.

|Field|Description|
|-----|-----------|
|Client ID|Client ID from your OAuth identity provider.|
|Client secret|Client secret from your OAuth identity provider.|
|Token request URL|Token request URL from your OAuth identity provider.|
|Scope|Scope from your OAuth identity provider.|

Select **Access Token** if you created a record in the Application Registries \[oauth\_entity\] table with a Snowflake or IdP service principal for authentication.

This option keeps credentials within the instance and uses the ServiceNow AI Platform OAuth framework for token lifecycle management. For details on creating an OAuth entity profile, see [Use a third-party OAuth provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/web-services/t_UseAThirdPartyOAuthProvider.md). When configuring the profile, select **Client Credentials** as the grant type. If your OAuth provider requires scopes, add them on the OAuth Entity Scopes tab. Consult your data source or identity provider documentation for the required scope values.

Select the OAuth entity profile for your Snowflake or IdP service principal.

Select the OAuth integration type that you want to use:

-   **System**: Use the selected OAuth entity profile for all users of this connection. This is the default option.
-   **Personal**: Require each user to authenticate individually with their own credentials before they can access Snowflake data through this connection. Select **Get OAuth Token** to open the authentication flow in a new browser tab and sign in.

    **Note:** Each user can view, renew, or revoke their personal access token from the Personal Integrations Dashboard in the Zero Copy Connector Hub. If a user's token expires or is missing, an alert appears when that user tries to access data assets for this connection, with a link to sign in again.


**Parent Topic:**[Connection form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/connection-form-fields-zcc.md)

**Related topics**  


[Create a Snowflake connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/create-snowflake-connection-zcc.md)

[Personal authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/personal-auth-zcc.md)

