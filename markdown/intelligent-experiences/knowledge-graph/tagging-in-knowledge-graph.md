---
title: Tagging in Knowledge Graph Designer
description: Use Knowledge Graph tags to mark tables that are important for answering natural language questions for specific use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/knowledge-graph/tagging-in-knowledge-graph.html
release: zurich
product: Knowledge Graph
classification: knowledge-graph
topic_type: concept
last_updated: "2025-11-21"
reading_time_minutes: 3
breadcrumb: [Using Enterprise graph schema, Knowledge Graph, Enable AI experiences]
---

# Tagging in Knowledge Graph Designer

Use Knowledge Graph tags to mark tables that are important for answering natural language questions for specific use cases.

Use Knowledge Graph Designer to create and edit tags from the **Enterprise Graph Tags** section.

<table id="table_xct_jg3_4hc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enterprise Graph \(regular mode\)

</td><td>

Provides hint to Enterprise Graph on which tables to prioritize when retrieving information, to improve the accuracy of results.Tag up to 30 tables for regular mode to help prioritize search results.

</td></tr><tr><td>

Enterprise Graph \(Small\)

</td><td>

Provides a list of tables to run the search operation. Enterprise Graph \(Small\) will only search on the tables provided by tags.

 A tag is required when Enterprise Graph \(Small\) is used with any of the prebuilt integrations with AI agent, Virtual Agent, or Now Assist Panel.

 You can tag a maximum of 50 tables.

 To enable querying on columns of a table that reference another table, also include the referenced table in tags.

</td></tr></tbody>
</table>## Creating tags

Tags are created by kg\_admins using Knowledge Graph Tags section.

Tags must be linked to a schema when selecting the Enterprise Graph or Enterprise Graph \(Small\) as the Knowledge Graph schema for your use case in Virtual Agent, ServiceNow Otto panel or AI agent.

Knowledge Graph includes the following prebuilt tags:

-   Virtual Agent DEFAULT TAG: A prebuilt tag listing common to core, ITSM, and HR tables for integrating Enterprise Graph with the Virtual Agent on the employee portal. Admins can edit this tag to include additional tables relevant for answering Virtual Agent queries.
-   ServiceNow Otto PANEL DEFAULT TAG: A prebuilt tag listing common to core, ITSM and HR tables which can be leveraged as general tag on ServiceNow Otto panel. Admins can edit this tag to add additional important table for answering questions on ServiceNow Otto panel.

To create or edit tags:

-   In Knowledge Graph Designer lists the existing tags and their associated tables. Use an existing tag, edit one to fit your needs, or create a tag for your use case.
-   Navigate to the admin center for consuming apps.
    -   For the Now Assist Virtual Agent or Now Assist Panel, go to your virtual agent's setup, select Information Sources, and open Knowledge Graph.
    -   For AI agent, proceed to its setup and open the Knowledge Graph tool for the AI agent.
-   Select Enterprise Graph or Enterprise Graph \(Small\) as the Knowledge Graph schema, and select the required tag from the Tag drop-down list to link it to a graph schema.

**Warning:** By default, the Enterprise Graph option is hidden for Virtual agent and Otto panel, and only Enterprise Graph \(Small\) is available as a schema option. To use Enterprise Graph, set the `sn_kg.va.enable_global_graph_all_modes` property to `true`. Role required: admin.

## Recommended tables for different use cases

-   ServiceNow Otto Virtual Agent: For Virtual Agent include the tables necessary to answer the expected user queries. For example, if you are deploying a new virtual agent on the employee center portal, add a tag that includes tables relevant to answering employee questions.
-   ServiceNow Otto panel: ServiceNow Otto panel operates as a unified assistant across multiple workspaces. Tag tables as follows:
    -   An individual tag for each workspace that encompasses key tables relevant to that workspace. This ensures the Now Assist panel can deliver responses specific to queries related to the workspace tables when accessed within each workspace.
    -   Create a general tag that includes the most important tables required to answer users questions on ServiceNow Otto panel, so the ServiceNow Otto panel can provide relevant answers when used outside a workspace.
    -   For more information on adding workspace tags in ServiceNow Otto panel, see [Add a Knowledge Graph schema to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/add-kg-schema-assistant.md).
-   AI agent: For an AI agent use case, include key tables relevant to the agent's purpose. For example, for asset manager agents User, Asset, and other crucial tables should be included in the tag. For more information, see [Add a Knowledge Graph to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/add-knowledge-graph.md).


