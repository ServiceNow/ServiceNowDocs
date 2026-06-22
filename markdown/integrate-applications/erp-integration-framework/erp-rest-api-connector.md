---
title: REST API connector for Zero Copy Connector for ERP
description: Use the REST API connector to connect to any RESTful API with standardized API specification formats.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-rest-api-connector.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-06-08"
reading_time_minutes: 2
keywords: [zero, copy, connector, erp, canvas, data hub, integration, rest, api, openapi, swagger, postman]
breadcrumb: [Add an entity to a model, Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# REST API connector for Zero Copy Connector for ERP

Use the REST API connector to connect to any RESTful API with standardized API specification formats.

## REST API connector

REST APIs can be used to access business data from ERP \(Enterprise Resource Planning\) systems. Integrating these APIs requires manual processes. The REST API connector solves this by providing a reusable, low-code integration layer.

## Configure REST service connections

REST connections use the HTTP connection template. For more information, see [Create an HTTP\(s\) connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/create-https-connection.md).

## Authenticate securely

The connector supports the following authentication options:

-   Basic Auth: A username and password \(Base64-encoded\). For more information, see [Basic authentication credential](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_BasicAuthCredentialsForm.md).
-   JWT \(JSON Web Token\): A bearer token authentication. For more information, see [JWT Bearer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/jwt-bearer.md).
-   API Key: A key passed as a header or query parameter. For more information, see [API key credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/API-key-credential-form.md) .
-   OAuth 2.0: A token authentication with automatic token refresh. For more information, see [Manage OAuth tokens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/t_ManageTokens.md).

ServiceNow Vault stores credentials securely. For more information, see [Exploring ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/exploring-servicenow-vault.md).

The system validates that the configured credential type matches one of the authentication schemes defined in the API specification before allowing execution.

## Import REST API definition into the Zero Copy Connector for ERP Model Manager

Import a REST API definition using one of the following methods:

-   Use Swagger/OpenAPI URL and provide a public URL pointing to a spec file. The system extracts the service name from the URL automatically. You can edit the service name before adding the service. After the service is added, all endpoints matching the current operation type become available for selection.
-   Upload a Swagger/OpenAPI JSON or Swagger/OpenAPI YAML file.

## Map data to your data model

After you import a REST service, use the Model Manager to define entities and map API response fields to the data model. For more information, see [Add a REST entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/add-a-rest-entity-to-a-model-operation.md).

## MID Server Support

If your REST API runs on-premises or behind a firewall, you can route API calls through a MID Server. The connection record includes a midServerName property that routes traffic through the designated MID Server. Cloud-hosted APIs can connect directly without a MID Server. For more information, see [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-landing.md).

## REST API connector tables

For information about the REST API connector tables that support Zero Copy Connector for ERP, see [REST API connector for Zero Copy Connector for ERP tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-rest-api-tables.md).

**Parent Topic:**[Add an entity to a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/add-an-entity-to-model.md)

