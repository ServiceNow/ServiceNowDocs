---
title: Set up MID-less log ingestion using an MCP Client
description: Create, configure, and activate MID-less log ingestion integrations for Health Log Analytics from an MCP Client.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-mcp-server-hla-ingest-setup.html
release: australia
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 2
breadcrumb: [MID-less log ingestion for HLA, Use the ITOM MCP Server Console, AI in ITOM, IT Operations Management]
---

# Set up MID-less log ingestion using an MCP Client

Create, configure, and activate MID-less log ingestion integrations for Health Log Analytics from an MCP Client.

## Before you begin

Verify that:

-   The ITOM Gateway is set up and configured on your ServiceNow instance. For more information, see [MID-less log streaming via ITOM Gateway in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-midless-streaming.md).
-   The ITOM MCP Server Console is active on your instance.
-   Your MCP Client application is connected to the ITOM MCP Server Console with valid OAuth credentials.
-   The Health Log Analytics plugin is installed on your instance.

For more information about setting up MID-less integrations from an MCP Client, see [MID-less log ingestion for HLA from an MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-mcp-server-hla-ingest.md).

Role required: evt\_mgmt\_admin or sys\_admin \(for JWT provider and token configuration\)

## Procedure

1.  Open your MCP Client application.

2.  In the MCP Client application, ask to create a MID-less integration.

    Use natural language. For example: "Create an OTel integration named otel-prod."

    If no integration with that name exists, the integration is created in a draft, inactive state. The following information is returned:

    -   Integration ID
    -   HTTP endpoint
    -   gRPC endpoint
    -   Access token
3.  Review the returned integration details.

4.  Ask the MCP Client to activate the integration.

5.  Request the setup information for your integration type.

    The following table lists what to ask for, based on integration type.

    |Integration type|What to do|
    |----------------|----------|
    |**OTel**|Ask your MCP Client to generate an OTel collector `exporters` configuration block, then add it to your `collector.yaml` file.|
    |**Other MID-less integration types**|Ask your MCP Client to help you complete the setup information specific to that integration type outside ServiceNow. For example, for Amazon Data Firehose, ask it to help you set up a Firehose stream in your AWS account.|

6.  Ask the MCP Client to rename the integration.

    **Note:** The integration must be inactive to be renamed. The integration is automatically deactivated, renamed, and reactivated.


## Result

The integration is active and ready to receive log data at the returned endpoint. On the Integrations Launchpad, the integration tile is available in the **Installed integrations** tab.

## What to do next

Verify that log data is arriving in HLA.

To rotate credentials, ask the MCP Client to refresh the integration's token. The previous token remains valid until its original expiration.

