---
title: Create a remote task definition with AI assistance
description: Use AI agent to create remote task definitions \(RTD\) that trigger the assignment of a remote task. AI agent fetches table metadata and automatically generate field mappings for a remote task definition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/create-remote-task-definition-ai-assistance.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Remote task definition, Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Create a remote task definition with AI assistance

Use AI agent to create remote task definitions \(RTD\) that trigger the assignment of a remote task. AI agent fetches table metadata and automatically generate field mappings for a remote task definition.

## Before you begin

-   The provider and consumer instances must have introspection set up, including the Integration Mapping Agent and connection tools such as MCP server and MCP client.

Role required: admin

## About this task

The Integration Mapping Agent retrieves table metadata from the provider and consumer instance and automatically generates the field mappings for a remote task definition \(RTD\). You can start AI-assisted mapping either through a ServiceNow Otto conversation, or from the **Run Introspection** action on an existing draft RTD. The AI agent generates the RTD in draft state.

**Note:** AI-generated field mappings should be reviewed to ensure accuracy. The AI agent may not capture all business requirements or edge cases.

## Procedure

1.  Open ServiceNow Otto and describe the tables you want to connect.

    For example, map incident to incident.

    To run introspection again from an existing draft, open the RTD record and select **Run Introspection**. This action is available only while the RTD is in the draft state and doesn't already have generated field mappings.

2.  If the agent asks which company the consumer instance belongs to, reply with the company name.

    The agent confirms the steps it takes, such as validating table names, retrieving the provider schema, and retrieving the consumer schema.

    To use the local instance schema as a fallback, reply with **local**, **use local**, **no company** or **skip**.

3.  If the agent can't find AI or MCP support on the consumer instance, and asks for a table specification file, upload the file.

    You can also ask the agent to proceed with a standard RTD for all consumers.

4.  Review the completion message.

    The message includes the RTD name, the number of field rows written, and links to the integration spec and remote task definition.

    **Note:** If the message reports failed transforms for one or more fields, open the RTD's **Transforms** tab and complete those transform maps manually. To learn more, see [Create a transform in Service Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-create-transform.md).

5.  Open the RTD and review the generated fields on the **Inbound fields**, **Outbound fields**, and **Transforms** tabs.

    If necessary, you can modify the fields. To learn more, see [Create a remote task definition in Service Exchange for Providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-create-remote-tasks-defs.md).


## Result

The RTD remains in draft state until you publish it. When you're satisfied with the mappings, select **Publish** to publish the RTD.

**Related topics**  


[AI-assisted remote task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/ai-assisted-remote-task.md)

[Remote tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-remote-task-overview.md)

