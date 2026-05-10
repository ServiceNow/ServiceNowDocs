---
title: Create a knowledge graph schema
description: Use the Knowledge Graph \(KG\) to create Knowledge Graph schema.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Generate product inventory summary, Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Create a knowledge graph schema

Use the Knowledge Graph \(KG\) to create Knowledge Graph schema.

## Before you begin

Role required: sn\_sprb\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge Graph** &gt; **Knowledge Graph Designer**.

    The UI displays a list of all the Knowledge Graph schema on the landing page.

2.  Start creating a Knowledge Graph schema by selecting **Create New**.

    This is an out of the box.

3.  On the form, fill in the fields.

    ![knowledge graph schema.](../image/create-knowledge-graph-schema.png)

    |Field|Description|
    |-----|-----------|
    |Display Name|Display name for the Knowledge Graph schema.|
    |Name|Optional name for the Knowledge Graph schema.|
    |Scope|Scope used when creating the Knowledge Graph schema. This field is a read only.|
    |Description|Knowledge Graph schema overview to provide additional information to users.|
    |Contribute to KG Global Graph|All the changes to the nodes and edges in the graph are added to the KG Global graph.|

4.  Select **Create**.

    The Add nodes to the Knowledge graph schema window is displayed.

5.  Enter or search for the nodes that you want to add to the Knowledge Graph schema and select **Add**.

    The Knowledge Graph schema​ is created and displayed on the Knowledge Graph canvas.

6.  In the navigation pane, add the following details:

    -   Node details
    -   Columns that can be queried
    -   Related nodes
    ![service summary graph.](../image/now-assist-tmt-service-summary-graph.png)

7.  In the Node details section, you can edit the following fields.

    -   Node type
    -   Node Description
    ![service summary graph.](../image/summary-graph-node-details.png)

    To manage the nodes in the Knowledge Graph schema, see [Manage nodes in a Knowledge Graph schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph/add-or-delete-nodes-from-a-knowledge-graph-schema.md).

8.  In the Columns that can be queried section, search for and select the desired columns and select **Save**.

9.  Add, delete, or edit edges in the Related nodes section and select **Save**.

    To edit the Knowledge Graph, you must copy the Knowledge Graph and adjust the settings according to your requirements.

    To edit the Knowledge Graph schema, see [Edit a Knowledge Graph schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph/editing-a-knowledge-graph-schema.md).


**Parent Topic:**[Generate service summary for a product inventory using Now Assist for Telecommunications, Media and Technology \(TMT\)](now-assist-tmt-summarize-knowledge-graph.md)

