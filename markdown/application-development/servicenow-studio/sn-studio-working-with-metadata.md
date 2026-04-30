---
title: Working with metadata app file categories in the ServiceNow Studio Navigator
description: ServiceNow Studio enables you to work with all types of metadata that the ServiceNow AI Platform supports, from automations and integrations to user interface files.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, ServiceNow Studio, Developing your application, Building applications]
---

# Working with metadata app file categories in the ServiceNow Studio Navigator

ServiceNow Studio enables you to work with all types of metadata that the ServiceNow AI Platform supports, from automations and integrations to user interface files.

## Accessing metadata for your ServiceNow Studio apps

The **File Categories** section of the Navigator panel enables you to quickly view all types of metadata that you have access to, arranged by taxonomy category. Expanding each metadata file category shows its subcategories. For example, expanding the **Automation** category provides access to view all of the sub-types of automation metadata, such as actions, flows, and playbooks.

**Note:** To see a complete list of each category's file types and information about each file, see [ServiceNow Studio Navigator panel taxonomy](../reference/servicenow-studio-file-navigator-taxonomy.md).

![Expanded AI section of the File Categories section of the Navigator](../image/sn-studio-file-nav-expanded.png "Metadata sections in the File Categories section of the Navigator")

When you select a sub-type of an expanded file category, ServiceNow Studio displays all of the metadata of that type, which you can select to view. For example, selecting **Flow** under the **Automation** file category displays a list of all flows that you have access to. Select one to open it in Workflow Studio in an integrated tab in ServiceNow Studio.

**Note:** The source table for each sub-category of metadata file type appears when you select the category. Select **Open list** to see a complete list of all the files of that type.

![The base table for the app file type appears at the top of the list](../image/sn-studio-file-category-table-name.png "Table for app files")

For more information on using the Navigator panel to find app files by their metadata category, see [Find an app or app file using the Navigator panel](../task/qs-find-app-app-file-using-navigator-panel.md).

## Metadata table and its extended tables

Metadata lives as application files in their corresponding tables on the ServiceNow AI Platform. The main metadata table is sys\_metadata, but specific types of metadata extend the sys\_metadata table. For example, flows and sub-flows use the extended sys\_hub\_flow table.

See [ServiceNow Studio Navigator panel taxonomy](../reference/servicenow-studio-file-navigator-taxonomy.md) for a list of available metadata and corresponding tables that extend sys\_metadata.

## Metadata by category

Each file category has different types of metadata available for automations, data, integration, mobile app builder, UI, and other categories. For a list of each type of file, its primary table, primary builder experience, and more, see [ServiceNow Studio Navigator panel taxonomy](../reference/servicenow-studio-file-navigator-taxonomy.md).

**Note:** You can group or ungroup the metadata categories in the File Categories menu by selecting the more options icon \(![more options icon](../image/sn-studio-more-options-icon.png)\) and selecting or deselecting **Show parent categories**.

<table id="table_j5p_nzv_zcc"><thead><tr><th>

Category

</th><th>

Metadata sections

</th></tr></thead><tbody><tr><td>

AI

</td><td>

-   Agentic Workflow
-   AI Agent
-   Skill

</td></tr><tr><td>

Automation

</td><td>

-   Automation
-   Schedules

</td></tr><tr><td>

Data

</td><td>

-   Client development
-   Data
-   MID Server
-   Server development

</td></tr><tr><td>

Integrations

</td><td>

-   Inbound integration
-   Outbound integration
-   Properties

</td></tr><tr><td>

Mobile

</td><td>

-   Mobile App Builder
-   Mobile Card Builder

</td></tr><tr><td>

UI

</td><td>

-   Content
-   User interface

</td></tr><tr><td>

Other

</td><td>

-   Natural Language Understanding \(NLU\)
-   Reporting
-   Security

</td></tr></tbody>
</table>