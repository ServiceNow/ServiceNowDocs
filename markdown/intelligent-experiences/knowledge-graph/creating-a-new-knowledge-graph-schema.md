---
title: Create a Knowledge Graph schema
description: Create customized Knowledge Graph schema that will be used by Virtual Agent, AI Agents and Now Assist Panel.
locale: en-US
release: yokohama
product: Knowledge Graph
classification: knowledge-graph
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Knowledge Graph Designer, Knowledge Graph, Enable AI experiences]
---

# Create a Knowledge Graph schema

Create customized Knowledge Graph schema that will be used by Virtual Agent, AI Agents and Now Assist Panel.

## Before you begin

Role required: kg\_admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge Graph** &gt; **Knowledge Graph Designer**.

    The UI displays a list of all the Knowledge Graph schemas on the landing page.

2.  Start creating a Knowledge Graph schema by selecting **Create New**.

    **Note:** You can create Knowledge Graph schema using ServiceNow tables or the external Workflow Data Fabric tables.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Display Name|Display name for the Knowledge Graph schema.|
    |Name|Optional name for the Knowledge Graph schema.|
    |Scope|Scope used when creating the Knowledge Graph schema. This field is a read-only.|
    |Description|Knowledge Graph schema overview to provide additional information to users.|

4.  Select **Create**.

    The Add nodes to the Knowledge graph schema window is displayed.

5.  Enter or search for the nodes that you want to add to the Knowledge Graph schema and select **Add**.

    ![Add nodes.](../Images/add-nodes.png)

    You can search and select the Workflow Data Fabric tables, if integrated.

    The Knowledge Graph schema​ is created and displayed on the Knowledge Graph canvas.

6.  In the navigation pane, add the following details:

    ![Knowledge Graph canvas.](../Images/kg-canvas.png)

7.  In the Node details section, you can add or edit the following fields.

    -   Add node synonym
    -   Node description
    ![Node details.](../Images/edit-node-details.png)

8.  In the Columns that can be queried section, search for and select the desired columns and select **Save**.

    ![Columns that can be queried.](../Images/columns-that-can-be-queried.png)

9.  Add, delete, or edit edges in the Related nodes section and select **Save**.

    ![Related nodes.](../Images/related-nodes.png)


