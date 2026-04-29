---
title: Client credentials grant workflow
description: Authenticate a client application using a client credentials workflow. The client credentials grant workflow is used by back-end services or system integrations to access ServiceNow APIs without user involvement.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Client Credentials Grant, Inbound integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Client credentials grant workflow

Authenticate a client application using a client credentials workflow. The client credentials grant workflow is used by back-end services or system integrations to access ServiceNow® APIs without user involvement.

## Before you begin

Role required: `oauth_admin, mi_admin, admin`

## About this task

This workflow describes how a client application \(back-end service or system integration\) authenticates directly with ServiceNow using its client credentials without user interaction. The application requests an access token using its client ID and client secret, which ServiceNow validates before issuing the token. The client then uses this token to access ServiceNow APIs. ServiceNow validates each request before returning the appropriate response.

![Client credentials grant workflow](../../machine-identity/images/mic-client-credentials-workflow.png "Client credentials grant workflow")

## Procedure

1.  **The client application makes a token request** to the ServiceNow end point with the following parameters:

    ```
    Method: POST
    Endpoint: https://<servicenow_base_url>/oauth_token.do
    ```

<table id="table_xlf_y33_vfc"><thead><tr><th>

Parameter

</th><th>

Required

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`grant_type`

</td><td>

Yes

</td><td>

OAuth 2.0 grant type.Example: `client_credentials`

</td></tr><tr><td>

`client_id`

</td><td>

Yes

</td><td>

Unique identifier for the client application.Example:Y`OUR_CLIENT_ID`

</td></tr><tr><td>

`client_secret`

</td><td>

Yes

</td><td>

Secret associated with the client ID.Example:`YOUR_CLIENT_SECRET`

</td></tr><tr><td>

`scope`

</td><td>

Optional

</td><td>

Requested permissions for the access token.Example:`incident_read``incident_write`

</td></tr></tbody>
</table>2.  ServiceNow validates the credentials and returns the access token.

3.  Make an API request with the access token.

    Include the access token in the `Authorization` header of each API request.

    ```
    Method: POST
    Endpoint: https://<servicenow_base_url>/api/now/incident  
    Authorization: Bearer YOUR_ACCESS_TOKEN
    ```

4.  ServiceNow validates the token and returns the appropriate API response.

    **Note:** Use the client credentials grant workflow only with trusted, server-side applications. Maintain the `client_secret` securely. Ensure that you don’t use the `client_secret` in client-side environments such as browsers or mobile apps.


