---
title: Add a Knowledge Graph schema to a chat assistant
description: Create Knowledge Graph schemas to represent semantic relationships in your data. Schemas improve assistant responses by providing additional context about users and your organization.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Add a Knowledge Graph schema to a chat assistant

Create Knowledge Graph schemas to represent semantic relationships in your data. Schemas improve assistant responses by providing additional context about users and your organization.

## Before you begin

See [Assign search sources to a chat assistant](add-info-sources-assistant.md).

Role required: virtual\_agent\_admin or admin

## About this task

Knowledge Graph transforms search into an intelligent, predictive, and efficient experience, increasing accuracy, and improving productivity.

**Note:** Knowledge Graph is not applicable to the Now Assist panel - Developer assistant.

For more information about Knowledge Graph, see Leverage Knowledge Graph prebuilt integration with Now Assist Virtual Agent and Now Assist Panel.

**Note:** By default, search personalization is available with AI Search in the assistant, and delivers personalized, context-aware search experiences powered by Knowledge Graph. To disable the integration with Knowledge Graph for personalization, open support ticket.

An empty Knowledge Graph page is shown if the Knowledge Graph app isn’t installed on the instance. Selecting **Go to Knowledge Graph** links to the ServiceNow Store’s Knowledge Graph page.

## Procedure

1.  If Knowledge Graph is turned on, select the Knowledge Graph schema to apply to the assistant.

    ![Choose your Knowledge Graph](../image/NAinVA-kg-122025.png "Choose your Knowledge Graph")

    **Note:** During a platform upgrade, if you previously created an assistant and assigned a Knowledge Graph schema to the assistant, you may need to reassign the schema to the assistant as it may show as **None**.

    Slot filling schema \(optional\): Slot filling automatically fills the user input with information from your organization's Knowledge Graph. The drop-down list consists of Knowledge Graph schemas that are available on the instance. There's no default schema for slot filling. If you select Enterprise Graph, you have the option to add tags.

    Natural language query schema \(optional\): Natural language query enables users to perform data query via plain text during the chat. The drop-down list consists of Knowledge Graph schemas that are available on the instance. The default schema for Natural Language Query is User Graph \(now\_user\_graph\_nlq\). If you select Enterprise Graph, you have the option to add tags.

    Enterprise Graph is a predefined graph schema that represents all tables. Use tags to annotate tables in the global schema for higher accuracy responses to questions on a specific subject matter. Selecting the button next to the Enterprise Graph selection directs you to the Knowledge Graph console where you can edit the specific Knowledge Graph.

    **Note:** For Now Assist panel - Platform \(default\) assistant, if Enterprise Graph and Enterprise Graph \(Small\) are selected within the NLQ schema, tags can be selected for specific workspaces that are active on the instance.

    For more information about Knowledge Graph tags, see Tagging in Knowledge Graph Designer.

    ![Fields to add workspace tags.](../image/NAinVA-kg-workspace-tags2-122025.png "Select workspace tags")

2.  Select**Manage tags** to open the tag list from the Knowledge Graph as a new browser tab.

    ![Manage tags.](../image/NAinVA-kg-tags-122025.png "Manage")

3.  Select **Manage Knowledge Graph** to open a new browser tab that directs you to the Knowledge Graph app.


## What to do next

See [Add assets to a chat assistant](add-assets.md).

