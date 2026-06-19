---
title: Metadata app file categories in the ServiceNow Studio Navigator
description: Use ServiceNow Studio to access and work with all metadata types that the ServiceNow AI Platform supports, from automations and integrations to user interface files.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/sn-studio-working-with-metadata.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-05-28"
reading_time_minutes: 2
breadcrumb: [Use, ServiceNow Studio, Developing your application, Building applications]
---

# Metadata app file categories in the ServiceNow Studio Navigator

Use ServiceNow Studio to access and work with all metadata types that the ServiceNow AI Platform supports, from automations and integrations to user interface files.

## How do I access metadata in the Navigator panel?

The **File Categories** section of the Navigator panel displays all metadata types accessible to the current user, arranged by taxonomy category. Expanding each metadata file category shows its subcategories. For example, expanding the **Automation** category displays all automation metadata sub-types, such as actions, flows, and playbooks.

**Note:** For a complete list of each category's file types, see [ServiceNow Studio Navigator panel taxonomy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-file-navigator-taxonomy.md).

\[Omitted image "sn-studio-file-nav-expanded.png"\] Alt text: Expanded AI section of the File Categories section of the Navigator

Selecting a sub-type of an expanded file category displays all metadata of that type. For example, selecting **Flow** under the **Automation** file category displays a list of all accessible flows. Select one to open it in Workflow Studio in a tab in ServiceNow Studio.

**Note:** The source table for each sub-category of metadata file type appears when you select the category. Select **Open list** to see a complete list of all the files of that type.

\[Omitted image "sn-studio-file-category-table-name.png"\] Alt text: The base table for the app file type appears at the top of the list

For more information on using the Navigator panel to find app files by metadata category, see [Find an app or app file using the Navigator panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/qs-find-app-app-file-using-navigator-panel.md).

## How does metadata relate to platform tables?

Metadata lives as application files in their corresponding tables on the ServiceNow AI Platform. The main metadata table is sys\_metadata, but specific types of metadata extend the sys\_metadata table. For example, flows and sub-flows use the extended sys\_hub\_flow table.

For a list of available metadata and corresponding tables that extend sys\_metadata, see [ServiceNow Studio Navigator panel taxonomy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-file-navigator-taxonomy.md).

## What metadata is available by category?

Each file category contains different metadata types for automations, data, integrations, mobile app builder, UI, and other categories. For a list of each file type, its primary table, primary builder experience, and more, see [ServiceNow Studio Navigator panel taxonomy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-file-navigator-taxonomy.md).

**Note:** Group or ungroup the metadata categories in the File Categories menu by selecting the more options icon \[Omitted image "sn-studio-more-options-icon.png"\] Alt text: more options icon and selecting or deselecting **Show parent categories**.

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
-   UI Builder
-   User interface

</td></tr><tr><td>

Other

</td><td>

-   Natural Language Understanding \(NLU\)
-   Reporting
-   Security

</td></tr></tbody>
</table>