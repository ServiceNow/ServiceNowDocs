---
title: Databricks authentication method fields
description: Fields that appear on the New Databricks Connection form depending on the selected OAuth credential type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/databricks-authentication-method-fields-zcc.html
release: brazil
topic_type: reference
last_updated: "2026-11-12"
reading_time_minutes: 2
keywords: [Databricks, authentication, personal authentication, zero copy connector, OAuth]
breadcrumb: [Connection form fields, Reference, Zero Copy Connectors, Workflow Data Fabric]
---

# Databricks authentication method fields

Fields that appear on the New Databricks Connection form depending on the selected OAuth credential type.

## OAuth credential type: Databricks Service Principal

Select this option if you are using a Databricks service principal for authentication.

|Field|Description|
|-----|-----------|
|OAuth client ID|Client ID issued by Databricks for authentication.|
|OAuth secret|Secret key associated with the client ID.|

## OAuth credential type: Azure Service Principal

Select this option if you are using an Azure managed service principal for authentication. This option requires a trust relationship between Databricks and Azure Entra ID.

|Field|Description|
|-----|-----------|
|OAuth client ID|Client ID issued by Azure for authentication.|
|Azure tenant ID|Azure tenant ID where your Databricks application is registered.|
|OAuth secret|Secret key associated with the client ID.|

## OAuth credential type: Access Token

Select this option if you created a record in the Application Registries \[oauth\_entity\] table with a Databricks or IdP service principal for authentication.

This option keeps credentials within the instance and uses the ServiceNow AI Platform OAuth framework for token lifecycle management. For details on creating an OAuth entity profile, see [Use a third-party OAuth provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/web-services/t_UseAThirdPartyOAuthProvider.md). When configuring the profile, select **Client Credentials** as the grant type. If your OAuth provider requires scopes, add them on the OAuth Entity Scopes tab. Consult your data source or identity provider documentation for the required scope values.

Select the OAuth entity profile for your Databricks or IdP service principal.

Select the OAuth integration type that you want to use:

-   **System**: Use the selected OAuth entity profile for all users of this connection. This is the default option.
-   **Personal**: Require each user to authenticate individually with their own credentials before they can access Databricks data through this connection. Select **Get OAuth Token** to open the authentication flow in a new browser tab and sign in.

    **Note:** Each user can view, renew, or revoke their personal access token from the Personal Integrations Dashboard in the Zero Copy Connector Hub. If a user's token expires or is missing, an alert appears when that user tries to access data assets for this connection, with a link to sign in again.


**Parent Topic:**[Connection form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/connection-form-fields-zcc.md)

**Related topics**  


[Create a Databricks connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/create-databricks-connection-zcc.md)

[Personal authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/personal-auth-zcc.md)

