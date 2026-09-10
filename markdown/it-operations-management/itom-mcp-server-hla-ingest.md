---
title: MID-less log ingestion for HLA from an MCP Client
description: Set up MID-less log ingestion integrations for Health Log Analytics \(HLA\) directly from an AI-enabled MCP Client, without opening the ServiceNow UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-mcp-server-hla-ingest.html
release: australia
topic_type: concept
last_updated: "2026-08-18"
reading_time_minutes: 2
breadcrumb: [Use the ITOM MCP Server Console, AI in ITOM, IT Operations Management]
---

# MID-less log ingestion for HLA from an MCP Client

Set up MID-less log ingestion integrations for Health Log Analytics \(HLA\) directly from an AI-enabled MCP Client, without opening the ServiceNow UI.

## Using an MCP Client to set up a MID-less integration

If the HLA app is installed on your ServiceNow instance, the ITOM MCP Server Console lets you set up HLA integrations for MID-less log data ingestion. You can set up integrations from any AI-enabled MCP Client. You can use an MCP Client, such as AWS Claude, to create the integrations entirely through natural-language prompts, without navigating to the Integrations Launchpad.

The HLA ingest tools associated with the ITOM MCP Server Console enable you to perform the following tasks from the MCP Client:

-   Find existing MID-less ingest integrations by name.
-   Create an ingest integration or rename an existing one. The MCP Client returns the integration ID, HTTP endpoint, gRPC endpoint, and access token for a newly created integration.
-   Turn an integration on or off. An integration must be deactivated before it can be renamed.
-   Generate a new access token for an integration. The previous token remains valid until its original expiration.

## Workflow

MID-less ingestion integration setup is part of the ITOM MCP Server Console workflow:

1.  An administrator opens their MCP Client application and describes the integration they need.

    For example: "Create an OTel ingestion integration named otel-prod."

    **Note:** By default, integrations are created in an inactive state. However, the MCP tools are capable of creating an active integration. For example, tell the MCP Client: "Create an active OTel ingestion integration named otel-prod."

2.  The MCP Client sends the request to the ITOM MCP Server Console using the Model Context Protocol \(MCP\).
3.  The ITOM MCP Server Console authenticates the user against ServiceNow role-based access control.
4.  The ITOM MCP Server Console creates or updates the ingest integration record in HLA.
5.  The ITOM MCP Server Console returns the integration details, including endpoint and token information, to the MCP Client.

**Related topics**  


[Set up MID-less log ingestion using an MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-mcp-server-hla-ingest-setup.md)

[Use the ITOM MCP Server Console to perform ITOM tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/use-itom-mcp-server.md)

[MID-less log streaming for HLA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-midless-streaming.md)

