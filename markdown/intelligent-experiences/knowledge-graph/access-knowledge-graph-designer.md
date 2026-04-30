---
title: Access Knowledge Graph Schema
description: Use Knowledge Graph Designer to create, edit, and manage Knowledge Graph schema.
locale: en-US
release: yokohama
product: Knowledge Graph
classification: knowledge-graph
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring Knowledge Graph, Knowledge Graph, Enable AI experiences]
---

# Access Knowledge Graph Schema

Use Knowledge Graph Designer to create, edit, and manage Knowledge Graph schema.

## Before you begin

Role required: kg\_admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge Graph** &gt; **Knowledge Graph Designer**.

    The Knowledge Graph Designer landing page displays a list of all the Knowledge Graph schemas available for users.

    ServiceNow some provides prebuilt schema that are non-editable. Currently, the following prebuilt schemas are available:

    -   User graph schema: Used to provide logged in user's details to Virtual Agent for personalised response. The profile section is used by AI agents for additional user context.
    -   Natural Language Query Scheme: Helps the requester with personalized responses on people queries and Natural Language queries. Also supports people citation card. By default the user NLQ graph is connected which is used for people queries but you also have sample graph schema for other employee queries. For more details see [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2069778).
    ![Knowledge Graph Designer landing page.](../Images/knowledge-graph-landing-page.png)

    You can create a Knowledge Graph schema from the landing page.

    Knowledge Graph also supports Admin to create Knowledge Graph schema with WorkFlow Data Fabric tables. This helps accessing data from different system in real time without moving it.


