---
title: Personal authentication
description: Personal authentication lets each user connect to a data source with their own credentials. Queries return only the data that the user can access at the source, not the full data set available to a shared service account.View, renew, or revoke your personal access tokens for zero copy connections.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/personal-auth-zcc.html
release: brazil
topic_type: concept
last_updated: "2026-11-13"
reading_time_minutes: 2
keywords: [personal authentication, per-user authentication, user-level access, end-user credentials, OAuth on behalf of the user, row-level security, alternative to a service account, personal access tokens, Personal Integrations Dashboard, renew token, revoke token]
breadcrumb: [Explore, Zero Copy Connectors, Workflow Data Fabric]
---

# Personal authentication

Personal authentication lets each user connect to a data source with their own credentials. Queries return only the data that the user can access at the source, not the full data set available to a shared service account.

Personal authentication uses the Personal integration type for OAuth 2.0 credentials on the ServiceNow AI Platform. For platform details, see [Personal authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/personal-authentication.md) in the ServiceNow AI Platform Security documentation.

## Service account compared with personal authentication

|Attribute|Service account \(System\)|Personal authentication \(Personal\)|
|---------|--------------------------|------------------------------------|
|Who signs in|The connection uses the selected OAuth entity profile for all users of the connection. This is the default option.|Each user authenticates individually with their own credentials before they can access data through the connection.|
|Data returned|Data that the service account can access.|Only data that the signed-in user can access at the source.|
|Token management|The ServiceNow AI Platform OAuth framework manages the token life cycle.|Each user can view, renew, or revoke their personal access token. Users with the df\_connection\_admin role can manage tokens from Zero Copy Connector Hub. Users without that role can manage tokens from the Personal Authentication dashboard in Integration Hub.|
|Expired or missing token|Not applicable.|An alert appears when the user tries to access data assets for the connection, with a link to sign in again.|

## Supported connectors

|Connector|Support tier|Personal authentication|Authentication method|Field reference|
|---------|------------|-----------------------|---------------------|---------------|
|Databricks|Primary|Supported|OAuth \(Access Token\)|[Databricks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/databricks-zcc.md)|
|Microsoft SQL Server|Primary|Supported|OAuth \(Access Token\)|[Microsoft SQL Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/sqlserver-zcc.md)|
|Oracle DB|Primary|Supported|OAuth \(Access Token\)|[Oracle DB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/oracle-zcc.md)|
|Snowflake|Primary|Supported|OAuth \(Access Token\)|[Snowflake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/snowflake-zcc.md)|
|Teradata|Primary|Supported|OAuth \(Access Token\)|[Teradata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/teradata-zcc.md)|

**Related topics**  


[Set up personal authentication for a connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/setup-personal-auth-zcc.md)

## Manage your personal access tokens

View, renew, or revoke your personal access tokens for zero copy connections.

### Before you begin

Role required: df\_connection\_admin.

Users without this role can manage tokens from the Personal Authentication dashboard in Integration Hub instead. See [Personal Authentication dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/integration-hub/personal-auth-dashboard.md).

### About this task

Users can view, renew, or revoke their personal access tokens. If a token expires or is missing, an alert appears when the user tries to access data assets for the connection. The alert includes a link to log in again.

### Procedure

1.  Navigate to Zero Copy Connector Hub.

2.  Open the connection that uses personal authentication.

3.  Under **Access Token**, select **Get OAuth Token** to renew your token, or select the option to revoke it.


