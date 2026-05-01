---
title: Resource owner password credential grant workflow
description: This flow is used in legacy or highly controlled environments where secure alternatives aren't feasible. The client app directly collects and sends user credentials to ServiceNow to obtain an access token, making it suitable only for trusted internal use.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [ROPC Grant, Inbound integrations, OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Resource owner password credential grant workflow

This flow is used in legacy or highly controlled environments where secure alternatives aren't feasible. The client app directly collects and sends user credentials to ServiceNow to obtain an access token, making it suitable only for trusted internal use.

## Before you begin

Role required: `oauth_admin, mi_admin, admin`

## About this task

This procedure outlines how a trusted client application obtains an access token by directly handling user credentials and uses it to access ServiceNow APIs.

The user logs in through the app, which sends both its own credentials and the user's to ServiceNow. ServiceNow validates the credentials and issues an access token that the app uses to call APIs.

![Resource owner password credential grant workflow](../images/mic-jwt-grant-workflow.png "Resource owner password credential grant workflow")

## Procedure

1.  The user logs in to the client application.

2.  The client application sends a token request to with the following parameters:

    -   Client ID and client secret.
    -   Username and password of the user.
    **Example**

    ```
    Method: POST
    Endpoint: https://<servicenow_base_url>/oauth_token.do
    Headers: Content-Type: application/x-www-form-urlencoded 
    ```

<table id="table_cdm_km5_xfc"><thead><tr><th>

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

Specifies the OAuth grant type.

</td></tr><tr><td>

`client_id`

</td><td>

Yes

</td><td>

The unique identifier for your client application.Format: YOUR\_CLIENT\_ID

</td></tr><tr><td>

`client_secret`

</td><td>

Yes

</td><td>

The client application's secret key.Format: YOUR\_CLIENT\_SECRET

</td></tr><tr><td>

`username`

</td><td>

Yes

</td><td>

The user’s ServiceNow username.

</td></tr><tr><td>

`password`

</td><td>

Yes

</td><td>

The user’s ServiceNow password.

</td></tr><tr><td>

`scope`

</td><td>

Optional

</td><td>

Defines the level of access requested.Example:

-   incident\_read
-   incident\_write


</td></tr></tbody>
</table>3.  ServiceNow validates both the client and user credentials, and returns the access token.

4.  The client uses the access token to call ServiceNow APIs.

    **Example**

    ```
    Method: GET
    Endpoint: https://<servicenow_base_url/api/now/incident
    Authorization: Bearer YOUR_ACCESS_TOKEN
    ```

5.  ServiceNow validates the access token, and returns the API response.


