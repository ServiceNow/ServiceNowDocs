---
title: Set up External connections for configuration rules
description: External connections enable enrichments in CPQ to retrieve data from systems outside CPQ for use in configuration rules, such as fetching third-party pricing or product attributes during a configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/external-connections.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up External connections for configuration rules

External connections enable enrichments in CPQ to retrieve data from systems outside CPQ for use in configuration rules, such as fetching third-party pricing or product attributes during a configuration.

Enrichments are scripts that run outside the rules engine and affect configurations in CPQ. The following enrichment types are available:

-   On configure/reconfigure
-   On BOM response
-   Validation
-   Picklist extension pricing
-   On request

External connections can only be called from an enrichment. When an enrichment calls an external connection, CPQ sends a request to the configured host and path, retrieves the response, and makes the data available to the enrichment script — for example, to populate pricing or product attributes in a configuration.

## External connections and connections

In CPQ, external connections and connections provide the same capability: they define the host, authentication credentials, and path used when CPQ calls an external system. The difference is where each type is used:

-   External connections are referenced in configuration rules, called from enrichment scripts that run during a configuration.
-   Connections are referenced in transaction rules, called from integrations that run in Transaction Manager.

Configure an external connection when the third-party call is triggered by a configuration event. Configure a connection when the call is triggered by a transaction event.

## Authentication for external connections

The authentication method required depends on the external system. The following options are available:

-   No authentication — use when the external connection calls an open API that does not require credentials.
-   Bearer token — use when the external system issues a static token for authentication. Supply the token directly in the connection.
-   OAuth client credentials — use when the external system requires an OAuth handshake. CPQ exchanges a client ID and secret with the authorization server to obtain an access token before each request.

## Path parameter variables

External connections support dynamic path segments using parameter variables. A parameter variable is a placeholder in the path that your enrichment script replaces with a runtime value. For example, a path defined as `/v4/latest/{{inputVariable}}` accepts a value for `inputVariable` from the calling enrichment script.

When a path uses a parameter variable, wrap the value in `encodeURIComponent()` in your enrichment script to ensure the value is safe to include in a URL.

**Related topics**  


[Create an external connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-external-connection.md)

