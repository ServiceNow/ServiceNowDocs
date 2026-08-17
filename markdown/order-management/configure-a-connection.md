---
title: Create a connection for ServiceNow Quote Experience calls
description: Add a connection in CPQ to define the host, path, and authentication credentials used when ServiceNow Quote Experience calls an external system during a transaction.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-a-connection.html
release: australia
topic_type: task
last_updated: "2026-04-15"
reading_time_minutes: 2
breadcrumb: [Integrations, CPQ Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a connection for ServiceNow Quote Experience calls

Add a connection in CPQ to define the host, path, and authentication credentials used when ServiceNow Quote Experience calls an external system during a transaction.

## Before you begin

Role required: admin

## About this task

Connections are used in transaction rules only. Each connection stores the host URL, an optional path, and authentication credentials. When you configure an integration in ServiceNow Quote Experience, you select a connection and CPQ uses the stored credentials to authenticate outbound requests during a transaction.

To call an external system from a configuration rule instead, configure an external connection. For more information, see [Set up External connections for configuration rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/external-connections.md).

The following authentication types are available: bearer token, OAuth client credentials, and JWT client credentials.

## Procedure

1.  Navigate to **All** &gt; **CPQ Administration** &gt; **Utilities** &gt; **Connections**.

2.  Select **+New** to create a new connection.

3.  In the **Name** field, enter a display name for the connection.

4.  In the **Host** field, enter the base URL of the external system you want to connect to.

5.  In the **Variable name** field, enter a unique system identifier for the connection.

    This value must be unique across all connections in your instance.

6.  In the **Path** field, enter the path to append to the host URL for the target endpoint.

7.  In the **Description** field, enter additional information about the connection.

8.  In the **Integration type** field, select **External**.

9.  In the **Authentication type** field, select the credential method that the external system requires, then complete the fields for that authentication type.

<table id="choicetable_ets_krs_djc"><thead><tr><th align="left" id="d57469e224">

Authentication type

</th><th align="left" id="d57469e227">

Fields to complete

</th></tr></thead><tbody><tr><td id="d57469e233">

**Bearer token**

</td><td>

In the **Authentication token** field, enter the token used to authenticate outbound requests.

</td></tr><tr><td id="d57469e245">

**OAuth client credentials**

</td><td>

-   **Client ID**: the client identifier issued by the external system.
-   **Client secret**: the credential used with the client ID to obtain an access token.
-   **Token URL**: the URL on the external system where an access token is requested.
-   **Scope** \(optional\): the permissions granted to the token on the external system, if required.


</td></tr><tr><td id="d57469e277">

**JWT client credentials**

</td><td>

-   **Client ID**: the client identifier issued by the external system.
-   **Private key**: the private key used to sign the JWT assertion.
-   **Token URL**: the URL on the external system where an access token is requested using the signed JWT.
-   **Scope** \(optional\): the permissions granted to the token by the external system, if required.


</td></tr></tbody>
</table>10. In the **Additional headers** field, enter any HTTP headers to include in outbound requests.

    Enter one header per line. Use quoted keys and values in the following format:

    ```
    "header-name" "header-value"
    ```

    For example:

    ```
    "x-api-version" "2"
    "x-tenant-id" "acme-corp"
    ```

11. Select **Save**.


## Result

The connection is saved and available for selection when configuring integrations.

**Related topics**  


[Configuring OAuth client credentials with JWT on ServiceNow](https://www.servicenow.com/community/api-insights-forum/configuring-oauth-client-credentials-with-jwt-on-servicenow/m-p/3442933)

