---
title: Microsoft SQL Server authentication method fields
description: Fields that appear on the New Microsoft SQL Server Connection form depending on the selected OAuth credential type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/sqlserver-authentication-method-fields-zcc.html
release: australia
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [Microsoft SQL Server, authentication, personal authentication, zero copy connector]
breadcrumb: [Reference, Zero Copy Connectors, Workflow Data Fabric]
---

# Microsoft SQL Server authentication method fields

Fields that appear on the New Microsoft SQL Server Connection form depending on the selected OAuth credential type.

## OAuth credential type: Azure Service Principal

|Field|Description|
|-----|-----------|
|Azure tenant ID|Azure AD tenant ID for the service principal. Required.|
|Azure client ID|Client ID \(application ID\) of the Azure AD service principal. Required.|
|Azure client secret|Client secret for the Azure AD service principal. Required.|
|Azure token scope|OAuth scope requested for the Azure AD token. Not required.|

## OAuth credential type: Access Token

Select this option if you created a record in the Application Registries \[oauth\_entity\] table with a Microsoft SQL Server or IdP service principal for authentication.

This option keeps credentials within the instance and uses the ServiceNow AI Platform OAuth framework for token lifecycle management. For details on creating an OAuth entity profile, see . When configuring the profile, select **Client Credentials** as the grant type. If your OAuth provider requires scopes, add them on the OAuth Entity Scopes tab. Consult your data source or identity provider documentation for the required scope values.

Select the OAuth entity profile for your Microsoft SQL Server or IdP service principal.

Select the OAuth integration type that you want to use:

-   **System**: Use the selected OAuth entity profile for all users of this connection. This is the default option.
-   **Personal**: Require each user to authenticate individually with their own credentials before they can access Microsoft SQL Server data through this connection. Select **Get OAuth Token** to open the authentication flow in a new browser tab and sign in.

    **Note:** Each user can view, renew, or revoke their personal access token from the Personal Integrations Dashboard in the Zero Copy Connector Hub. If a user's token expires or is missing, an alert appears when that user tries to access data assets for this connection, with a link to sign in again.


**Parent Topic:**[Zero Copy Connectors reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/reference-zcc.md)

**Related topics**  


[Create a Microsoft SQL Server connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/create-sqlserver-connection-zcc.md)

