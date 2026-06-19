---
title: Create a Knowledge Graph schema
description: Create customized Knowledge Graph schema that will be used by Virtual Agent, AI Agents and Now Assist Panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/knowledge-graph/creating-a-new-knowledge-graph-schema.html
release: australia
product: Knowledge Graph
classification: knowledge-graph
topic_type: task
last_updated: "2026-03-12"
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

    \[Omitted image "add-nodes.png"\] Alt text: Add nodes.

    You can search and select the Workflow Data Fabric tables, if integrated.

    The Knowledge Graph schema​ is created and displayed on the Knowledge Graph canvas.

6.  In the navigation pane, add the following details:

    \[Omitted image "kg-canvas.png"\] Alt text: Knowledge Graph canvas.

7.  In the Node details section, you can add or edit the following fields.

    -   Add node synonym
    -   Node description
    \[Omitted image "edit-node-details.png"\] Alt text: Node details.

8.  In the **Table filters** section, view and add filters to set rules that control which records are shown in query results.

    To add table filters, provide the following information:

    -   Field
    -   Operator
    -   Value
    -   Add Condition set: optional field to add an alternative filter condition.
    -   Apply filters to child tables: optional check box to add the same filter conditions for the child table of the selected table in the graph.
    \[Omitted image "table-filters.png"\] Alt text: Table filters

9.  In the Columns that can be queried section, search for and select the desired columns and select **Save**.

    \[Omitted image "columns-that-can-be-queried.png"\] Alt text: Columns that can be queried.

10. Add, delete, or edit edges in the Related nodes section and select **Save**.

    \[Omitted image "related-nodes.png"\] Alt text: Related nodes.


