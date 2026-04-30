---
title: Create a Knowledge Graph schema
description: Use the Knowledge Graph to create Knowledge Graph schemas.
locale: en-US
release: xanadu
product: Knowledge Graph
classification: knowledge-graph
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Knowledge Graph Designer, Knowledge Graph, Now Assist, Enable AI experiences]
---

# Create a Knowledge Graph schema

Use the Knowledge Graph to create Knowledge Graph schemas.

## Before you begin

Role required: kg\_admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge Graph** &gt; **Knowledge Graph Designer**.

    The UI displays a list of all the Knowledge Graph schemas on the landing page.

2.  Start creating a Knowledge Graph schema by selecting **Create New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Display Name|Display name for the Knowledge Graph schema.|
    |Name|Optional name for the Knowledge Graph schema.|
    |Scope|Scope used when creating the Knowledge Graph schema. This field is a read-only.|
    |Description|Knowledge Graph schema overview to provide additional information to users.|
    |Mark as Default|Check box used to assign the Knowledge Graph schema as a fallback schema. The default schema is used if the system fails to reach the assigned schema.|

4.  Use the schema as a fallback option by selecting **Mark as Default**.

    **Note:**

    -   If the specified Knowledge Graph schema isn't available, the system uses the fallback schema.
    -   If you select this option, the system overrides the existing selection.
5.  Select **Create**.

    The Add nodes to the Knowledge graph schema window is displayed.

6.  Enter or search for the nodes that you want to add to the Knowledge Graph schema and select **Add**.

    ![Add nodes.](../Images/add-nodes.png)

    The Knowledge Graph schema​ is created and displayed on the Knowledge Graph canvas.

7.  In the navigation pane, add the following details:

    ![Knowledge Graph canvas.](../Images/kg-canvas.png)

8.  In the Node details section, you can edit the following fields.

    -   Node type
    -   Node Description
    ![Node details.](../Images/edit-node-details.png)

9.  In the Columns that can be queried section, search for and select the desired columns and select **Save**.

    ![Columns that can be queried.](../Images/columns-that-can-be-queried.png)

10. Add, delete, or edit edges in the Related nodes section and select **Save**.

    ![Related nodes.](../Images/related-nodes.png)


