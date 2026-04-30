---
title: Graph connection form
description: The following are the available fields in the Graph connection form to create a Graph connection for Microsoft SharePoint connectivity configuration.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SharePoint Online Search Connector reference, SharePoint Online Search Connector, Employee Service Management]
---

# Graph connection form

The following are the available fields in the Graph connection form to create a Graph connection for Microsoft SharePoint connectivity configuration.

<table id="table_b3g_tpg_ywb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the graph connection.

</td></tr><tr><td>

Client ID

</td><td>

Client ID of your application.

</td></tr><tr><td>

Client secret

</td><td>

Client secret of your application.

</td></tr><tr><td>

Default grant type

</td><td>

For Delegated permissions, authorization code provided for automatic access to users.For Application permissions, client credentials provided for automatic access to users.

</td></tr><tr><td>

Application

</td><td>

Global.

</td></tr><tr><td>

Authorization URL \(for Delegated permissions only\)

</td><td>

`https://login.microsoftonline.com/<Tenant ID>/oauth2/v2.0/authorize`.

</td></tr><tr><td>

Token Revocation URL \(for Delegated permissions only\)

</td><td>

`https://login.microsoftonline.com/<Tenant ID>/oauth2/v2.0/token`.

</td></tr><tr><td>

Token URL

</td><td>

`https://login.microsoftonline.com/<Tenant ID>/oauth2/v2.0/token`

</td></tr><tr><td>

Redirect URL

</td><td>

`https://<ServiceNow instance URL>/oauth_redirect.do`. For example, `[https://eesharepoint.example.com/oauth\_redirect.do](https://eesharepoint.example.com/oauth_redirect.do).`

</td></tr></tbody>
</table>