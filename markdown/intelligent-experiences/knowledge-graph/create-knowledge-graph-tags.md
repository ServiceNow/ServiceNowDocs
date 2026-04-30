---
title: Create Knowledge Graph tag
description: Create Knowledge Graph tags for Now Assist Virtual Agent, AI agent or Now Assist panel Enterprise Graph using Knowledge Graph Designer to improve accuracy of natural language queries.
locale: en-US
release: zurich
product: Knowledge Graph
classification: knowledge-graph
topic_type: task
last_updated: "2025-11-21"
reading_time_minutes: 3
breadcrumb: [Tagging in Knowledge Graph Designer, Using Enterprise graph schema, Knowledge Graph, Enable AI experiences]
---

# Create Knowledge Graph tag

Create Knowledge Graph tags for Now Assist Virtual Agent, AI agent or Now Assist panel Enterprise Graph using Knowledge Graph Designer to improve accuracy of natural language queries.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge Graph Designer** &gt; **Enterprise Graph Tags** &gt; **New tag**.

    You are navigated to the Create New Tag record page.

    ![Tag Module navigation](../Images/kg-tags.png)

2.  On the Create New Tag record page, add the following information:

    ![Tag Module](../Images/kg-tagging-module.png)

    -   Tag name: Name for the tag.
    -   Description
    -   Scope: The default selection in Global. Read-only field.
    -   Select Tables: The tables or nodes that you want to add to the tag.
3.  Select **Next** to go to Configure tables page.

    The details that are added to the Configure tables page will help to further improve the accuracy of the natural language queries.

    The selected tables will be displayed on the left pane of the Configure tables page.

    ![New tag configure tables page](../Images/kg-new-tag-table-config.png)

4.  Select a table from the left pane to add the following: , column and edge configurations, data filters and hidden columns.

    -   Tables configurations: Synonyms and AI instructions
    -   Column and edge configurations: Synonyms and AI instructions
    -   Data filters
    -   Hidden columns
    AI Instructions injects business context directly into the Knowledge Graph natural language query engine, shaping how the system interprets and traverses data. Instructions can be configured at three levels:

    -   Node \(entity/table\)
    -   Property \(column/attribute\)
    -   Edge \(relationship\)
    Each instruction can optionally be marked as **Always Include**, ensuring critical business logic applies unconditionally across all queries. For example, excluding retired assets or closed tickets by default unless explicitly requested.

    For best results, write instructions as generalized, context-driven guidance rather than hard-coded references to specific table values. See [Improving Natural Language Queries with Tag configuration](../concept/ai-instructiona-and-examples.md) to see detailed examples.

5.  Add alternative names in the **Table synonyms** field and select **Add**.

    -   Use the commonly used table names as synonyms to help AI recognize it in natural language queries.
    -   Example: you can add Tickets as a synonym for the Incident table.
    -   You can add up to five synonyms only.
6.  To delete a synonym, select ![](../../document-intelligence/image/icon-docintel-delete-grid-line.png) icon next to the synonym.

7.  Add AI Instructions in the Table Configurations section and select **Add**.

    **Note:** Add up to 5 table specific business context in the **AI Instructions** field.

8.  Select **Always include** to allow adding an instruction as a default business logic.

    For example, always include instruction to skip retired assets from the results unless user explicitly request for it.

9.  Select **Add Column** and choose the columns and edges that you want to add synonyms to.

    -   Add commonly used column and edge names as synonyms to help the AI match user terms to this field.
    -   Example: you can add Opened On as a synonym for Created Date.
    -   You can add up to five synonyms only.
    The selected columns and edges are added to the **Column / Edge configurations** section.

10. To delete a column from the section, select ![delete icon](../../../common/image/icon-delete-trashcan.png) next to the column.

11. Add AI Instructions in the **Column/Edge Configurations** section and select **Add**.

    **Note:** Add up to 5 instructions per entity in the **AI Instructions** field.

12. Select **Add filter** option to add data filters for managing which records appear in the query results and add the following details:

    -   Field
    -   Operator
    -   Value
    Examples:

    -   To exclude inactive users from search results, apply `Active = True` filter.
    -   To include only active incidents in response, add a data filter to consider `state in (in progress, on hold)`.
13. Select **Apply filters to child tables** check box if you want to add the same filter conditions for the child table of the selected table in the tag.

    If enabled, these filters will also apply to child tables that inherit data from this table.

14. Select irrelevant or insensitive columns from the **Hidden column** drop-down to exclude them from queries.

    Hidden columns cannot be queried and do not appear in the result.

    For example, add `Employee number` as hidden columns for `sys_user` table to hide the employee number from query results.

15. Select **Create tag** and repeat the same process for each of the selected columns.


