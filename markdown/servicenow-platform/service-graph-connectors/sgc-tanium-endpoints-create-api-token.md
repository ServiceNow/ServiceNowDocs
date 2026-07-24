---
title: Create an API token
description: Create an API token to be used by the Service Graph Connector for Tanium Endpoints.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-create-api-token.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-06-08"
reading_time_minutes: 1
breadcrumb: [Configure the Tanium environment, Tanium Endpoints, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create an API token

Create an API token to be used by the Service Graph Connector for Tanium Endpoints.

## Before you begin

Role required: Tanium administrator

For more information, see [Creating API tokens for ServiceNow](https://help.tanium.com/bundle/Security-Operation-Integration/page/ServiceNow_Integrations/Create_API_key.htm).

## Procedure

1.  Log in to the **Tanium Endpoint Console**.

2.  Navigate to **Administration** &gt; **Permissions** &gt; **API Tokens**.

3.  Select **New API Token**.

4.  Configure the following values:

    -   **Notes**: Enter the integration name and the ServiceNow instance.
    -   **Expiration**: Set the value to more than `7 days` \(recommended\). ServiceNow rotates tokens automatically every seven days.
    -   **Trusted IP Addresses**: Enter the IP addresses of the ServiceNow MID Server or instance.
5.  Select **Create**.

6.  Copy the token and store the token information securely.


## What to do next

Provide the API token to the ServiceNow administrator who configures the data source for the Service Graph Connector for Tanium Endpoints.

