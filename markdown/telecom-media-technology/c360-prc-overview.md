---
title: Party Relationship Center
description: The Party Relationship Center \(PRC\) provides a single, unified view of all entities connected to a party, including billing accounts, sold products, related parties, and active cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/c360-prc-overview.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [party relationship centre, PRC, node map, customer hierarchy, relationship graph]
breadcrumb: [Explore, Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Party Relationship Center

The Party Relationship Center \(PRC\) provides a single, unified view of all entities connected to a party, including billing accounts, sold products, related parties, and active cases.

**Note:** To view the party relationship center, you must have the `sn_genai_platform` plugin installed.

An interactive graph of all entities connected to a party is displayed in the CRM Workspace. It is fully configurable and administrators can controlAdministrators can control which entities appear in the graph, what information is displayed on each node, and how relationships are visualized. A contextual side panel shows detailed information about any selected entity and eliminates the need to navigate across multiple screens or applications.

Log in as a user with the sn\_telecom\_c360.user or the sn\_telecom\_c360.admin role and select the Party Relationship Center icon on the [Telecommunications Customer 360 home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/c360-home-page.md). The map is displayed when a graph configuration exists for the selected consumer or account.

Each node in the map displays a header, subheader, highlighted value, and contextual side panel properties. You can configure these values per node type. The node map supports horizontal and vertical orientation. Selecting any node opens a contextual side panel that displays the configured properties for that entity. You can also navigate directly to a node's underlying record by selecting the open-record button in the side panel.

Use the **Search** option to filter the node map by typing a value that matches the header or subheader configured for a node type. Matching nodes are highlighted in the graph.

For consumers, the map displays the consumer and up to five levels of related entities. Products can link directly to the consumer or through a billing account. For accounts, the map displays the parent account and up to five levels of related entities for each child account.

**Related topics**  


[Configure the Party Relationship Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/c360-configure-prc.md)

