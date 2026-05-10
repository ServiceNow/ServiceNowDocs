---
title: Third-party data integration components
description: These components require configuration by the system administrator to use third-party data integration with Agent Workspace for CSM.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Third-party data integration for CSM, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Third-party data integration components

These components require configuration by the system administrator to use third-party data integration with Agent Workspace for CSM.

## OAuth 2.0 –JWT Bearer grant type

JWT Bearer is the OAuth 2.0 grant type supported for the third-party data integration feature. It allows server-to-server API interactions between the ServiceNow instance and external API providers without requiring any user intervention.

The third-party application admin is used as the subject claim of the JWT that the ServiceNow instance creates and passes to the third-party application instance. This is done to get the access token which is used to make the REST API call to fetch records from the third-party application table.

## Credentials and connections

IntegrationHub takes advantage of aliases to manage connection information and credentials when integrating with external systems. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. IntegrationHub only requires an alias, which then resolves to use the correct credentials and connection information during runtime.

For more information, see the following topics:

-   [Introduction to credentials, connections, and aliases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/credentials-connections-alias.md)
-   [Create connection attributes for IntegrationHub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/create-connection-attributes.md)

## Remote tables

The Tables \(sys\_db\_object\) table contains a record for each table in the database, including remote tables. For remote table records, the **Remote Table** flag is checked on the record form.

The columns in a remote table are mapped to the columns in a third-party application table from which the data is being pulled. The remote table script definition stores this information. Table definitions for remote tables reside on the ServiceNow AI Platform. The table rows, or external records, are stored in memory while a user views the data in a list or form.

For more information about remote tables, see [Create a remote table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/remote-tables/create-remote-table.md).

When creating a remote table for use with IntegrationHub, pay special attention to the caching interval and choose an interval based on your workflow and the volatility of the third-party data. If the caching interval is too short, this can result in unnecessary connections to the third-party application. If the caching interval is too long, this can result in out-of-date third-party data being presented in Agent Workspace for CSM.

## Remote table script definitions

Use a script definition to retrieve and cache data for a remote table by running the script against an external data source. Remote table script definitions store the following information:

-   Name
-   Active
-   Table
-   Script
-   Cache TTL
-   Domain
-   Domain path

For more information about script definitions, see [Create a script definition for a remote table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/remote-tables/create-remote-table-script.md).

