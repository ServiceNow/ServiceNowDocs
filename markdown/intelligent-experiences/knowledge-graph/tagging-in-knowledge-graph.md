---
title: Tagging in Knowledge Graph Designer
description: Use Knowledge graph tags to mark the key tables, that are important for answering natural language questions for specific use cases.
locale: en-US
release: zurich
product: Knowledge Graph
classification: knowledge-graph
topic_type: concept
last_updated: "2025-11-21"
reading_time_minutes: 3
breadcrumb: [Using Enterprise graph schema, Knowledge Graph, Enable AI experiences]
---

# Tagging in Knowledge Graph Designer

Use Knowledge graph tags to mark the key tables, that are important for answering natural language questions for specific use cases.

Use Knowledge Graph Designer to create and edit tags from the **Enterprise Graph Tags** section.

<table id="table_xct_jg3_4hc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enterprise Graph- regular mode

</td><td>

Provides hint to Enterprise Graph on which tables to prioritize when retrieving information, to improve the accuracy of results.It is recommended to only tag up to 30 tables for regular mode as hints to prioritize while searching.

</td></tr><tr><td>

Enterprise Graph \(Small\)

</td><td>

Provides a list of tables to run the search operation. Enterprise Graph \(Small\) will only search on the tables provided by tags.

 It is mandatory to add a tag when Enterprise Graph \(Small\) is used with any of the prebuilt integration with AI agent, Virtual Agent or Now Assist Panel.

 You can tag a maximum of 50 tables.

 Note that to enable querying on columns of table which are references to another table, also include referenced table in tags.

</td></tr></tbody>
</table>## Creating tags

Tags are created by kg\_admins using the Knowledge Graph Tags section and has to be linked to schema when selecting the Enterprise Graph or Enterprise Graph \(Small\) as the Knowledge Graph schema for your use case in Virtual Agent, Now Assist Panel or AI agent.

Knowledge graph ships the following prebuilt tags:

1.  VIRTUAL AGENT DEFAULT TAG: A prebuilt tag listing common to core, ITSM, and HR tables for integrating Enterprise Graph with the Virtual Agent on the employee portal. Admins can edit this tag to include additional tables relevant for answering Virtual Agent queries.
2.  NOW ASSIST PANEL DEFAULT TAG: A prebuilt tag listing common to core, ITSM and HR tables which can be leveraged as general tag on Now Assist panel. Admins can edit this tag to add additional important table for answering questions on Now Assist panel.

Follow these steps to create or edit tags:

-   Go to the Knowledge Graph Designer to view the existing tags and their associated tables. You can use an existing tag, edit one to fit your needs, or create a new tag for your particular use case.
-   Navigate to the admin center for consuming apps.
    -   For the Now Assist Virtual Agent or Now Assist Panel, go to your virtual agent’s setup, select Information Sources, and open the Knowledge Graph.
    -   For AI agent, proceed to its setup and open the Knowledge Graph tool for the AI agent.
-   Select Enterprise graph or Enterprise Graph \(Small\) as the KG schema and select the required tag from Tag drop down to link it to graph schema.

**Note:** In this release, the Enterprise Graph option is hidden by default for Now Assist Virtual Agent and Now Assist Panel, and only Enterprise Graph \(Small\) can be selected as schema option. To use Enterprise Graph, Admins can enable it as a schema option by setting the property `sn_kg.va.enable_global_graph_all_modes` to true. The role required is Admin.

## Recommended tables for different use cases

-   Now Assist Virtual Agent: For Now Assist Virtual Agent include the tables necessary to answer the expected user queries. For example if you want to deploy a new virtual agent on employee center portal, you should add a tag having tables relevant for answering employee questions.
-   Now Assist Panel: Now Assist Panel operates as a unified assistant across multiple workspaces, hence it is essential to tag tables as follows:
    -   An individual tag for each workspace that encompasses key tables relevant to that workspace. This ensures the Now Assist panel can deliver responses specific to queries related to the workspace tables when accessed within each workspace.
    -   Create a general tag that includes the most important tables required to answer users questions on Now Assist panel, allowing the Now Assist panel to provide relevant answers when used outside of any workspace.
    -   For more information on adding workspace tags in Now Assist Panel, see [Add a Knowledge Graph schema to a chat assistant](https://www.servicenow.com/docs/access?context=add-kg-schema-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).
-   AI agent: For an AI agent use case, include key tables relevant to the agent's purpose. For example, for asset manager agents User, Asset, and other crucial tables should be included in the tag. For more information, see [Add a Knowledge Graph to an AI agent](../../now-assist-ai-agents/task/add-knowledge-graph.md).


