---
title: Configure the Tanium environment for the Service Graph Connector for Tanium Endpoints
description: Configure your Tanium environment to import data using the Service Graph Connector for Tanium Endpoints.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-cmdb-tanium-endpoints-configure-task.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 1
breadcrumb: [Tanium Endpoints, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the Tanium environment for the Service Graph Connector for Tanium Endpoints

Configure your Tanium environment to import data using the Service Graph Connector for Tanium Endpoints.

## Before you begin

Role required: Tanium administrator

## About this task

The Service Graph Connector for Tanium Endpoints authenticates to Tanium using an API token. To follow Tanium's security best practices, the token must be bound to an identity that has only the roles required by the integration—not a privileged administrator account. For more information, see [Creating API tokens for ServiceNow](https://help.tanium.com/bundle/Security-Operation-Integration/page/ServiceNow_Integrations/Create_API_key.htm).

|Identity|Description|
|--------|-----------|
|Service account \(recommended\)|Default identity. Provides the cleanest separation of integration permissions from human users.|
|Persona|Use this identity only if your organization doesn't permit dedicated service accounts.|

After you configure an identity, create an API token. Provide the resulting API token to the ServiceNow administrator who sets up the Service Graph Connector for Tanium Endpoints.

## Procedure

1.  Configure an identity for binding the API token that is used by the Service Graph Connector for Tanium Endpoints:

    -   [Configure a service account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-configure-service-account.md) \(default identity\)
    -   [Configure a persona](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-configure-persona.md) \(alternative identity; to be used only when a service account is not permitted\)
    Create an identity that has only the roles required by the integration.

2.  [Create an API token](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-create-api-token.md)

    After configuring the identity \(service account or persona\), generate the API token to be used by the Service Graph Connector for Tanium Endpoints.


