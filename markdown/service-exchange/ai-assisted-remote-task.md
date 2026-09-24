---
title: AI-assisted remote task
description: Set up remote task definition \(RTD\) between a provider and consumer instance by using AI agent. An AI agent inspects tables on the instances and automatically generates field mappings for remote task definitions in Service Exchange, reducing manual setup work for cross-instance integrations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/ai-assisted-remote-task.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 3
keywords: [AI agent, remote task definition, field mapping, Service Bridge]
breadcrumb: [Remote tasks, Explore, Service Exchange]
---

# AI-assisted remote task

Set up remote task definition \(RTD\) between a provider and consumer instance by using AI agent. An AI agent inspects tables on the instances and automatically generates field mappings for remote task definitions in Service Exchange, reducing manual setup work for cross-instance integrations.

Setting up a RTD between a provider and a consumer instance normally requires an administrator to manually map fields between the two tables. Introspection uses Integration mapping agent to fetch table metadata from both instances. The agent uses that metadata to generate the outbound and inbound field mappings, transform maps, and a draft RTD.

## Key benefits

Introspection provides the following benefits:

-   Reduces the manual effort of researching table schemas on both the provider and consumer instance.
-   Generates field mappings, choice mappings, and reference field resolutions from the actual schema of both tables instead of guesswork.
-   Creates the resulting RTD in draft state so an you can review the AI-generated mappings before publishing.

## How it works

The following describes the general flow when a provider administrator starts an AI-assisted RTD through ServiceNow Otto:

1.  The administrator describes the tables to connect, for example by asking the agent to map one table to another.
2.  If a specific consumer company or connection is not part of the request, the agent asks which company the consumer instance belongs to. If more than one connection matches, the agent lists the matching connections and asks the administrator to select one. The administrator can also indicate that no specific company applies, in which case the local instance schema is used as a fallback for both sides of the mapping.
3.  The agent looks for an active connection to the consumer instance. When one exists and the target table is on the consumer's allowed tables list, the agent fetches the table metadata over that connection. If the target table isn't on the consumer's allowed list, the agent tells the administrator the table isn't shared and offers the list of tables that are. If no connection is available, or the target table still isn't available on the remote instance, the agent asks the administrator to confirm falling back to the local instance before it proceeds.
4.  Throughout the conversation, the agent shows its response first, followed by a collapsed summary of the provider and consumer table structures, each one clearly labeled by side, and confirms which side is the provider and which is the consumer before continuing.
5.  The agent retrieves enriched field metadata for both tables, including field types, choice values, and audit signals. The agent uses this information to generate field mappings, choice mappings, and reference field resolutions.
6.  The agent excludes custom fields that exist only on the provider instance \(fields with a **u\_** or **x\_** prefix\) from the generated mappings. The consumer instance may not have equivalent fields.
7.  The agent stores the generated field mappings as an integration spec and uses it to create a draft RTD. The integration spec and RTD reference each other so multiple versions of a spec can exist over time.
8.  The agent reports the outcome, including the RTD name, the number of field rows written, and links to both the integration spec and the RTD.

**Note:**

Transform maps for choice fields might not generate automatically. If the completion message reports failed transforms, manually review and complete the affected transform maps.

For more information on the detailed steps about generating RTD, see [Create a remote task definition with AI assistance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/create-remote-task-definition-ai-assistance.md).

**Related topics**  


[Remote tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-remote-task-overview.md)

