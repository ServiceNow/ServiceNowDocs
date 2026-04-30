---
title: Configuring AI search in Recommended Actions
description: As an admin, configure AI search in Recommended Actions to enable agents to perform an AI search to find relevant resources.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Configuring AI search in Recommended Actions

As an admin, configure AI search in Recommended Actions to enable agents to perform an AI search to find relevant resources.

You can configure AI search in Recommended Actions by performing these procedures.

<table id="table_jm3_lm4_15b"><thead><tr><th>

Step

</th><th>

Action

</th></tr></thead><tbody><tr><td>

[Enable the AI search tab in UI builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/vancouver/now-components/sn-next-best-action-list-connected/uib-setup)

</td><td>

Deselect the **Hide Search** button in UI Builder to display the AI search tab in the contextual side panel of your workspace.

</td></tr><tr><td>

[Create a context and select a search application configuration](../task/ra-csm-contexts-create.md)

</td><td>

-   Create a context so that agents can see recommendations for records from a specific table, such as the Case table.
-   Select a search application configuration to specify AI search as the search engine. This configuration includes search sources and genius result configurations.

</td></tr><tr><td>

[Map AI search results with guidance inputs in Recommended Actions](../task/ra-create-search-result-mapping-for-ai-search.md)

</td><td>

Map AI search results with guidance inputs to enable the AI search results to be displayed with appropriate actions.

</td></tr><tr><td>

[Automatically map AI search results with guidance inputs](ra-configuring-ai-search-automatically.md)

</td><td>

Automatically create AI search results for a search configuration application in Recommended Actions.

</td></tr></tbody>
</table>## Configuring genius results

In the search profile of your selected search application configuration, link the following Genius Result configurations to display actionable top results. For more information, see [Link a Genius Result configuration to a search profile](https://www.servicenow.com/docs/access?context=link-gr-search-profile-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

<table id="table_jry_4cb_1zb"><thead><tr><th>

Genius Result configuration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog item

</td><td>

Displays top search results from the Catalog Item \[sc\_cat\_item\] table. Each answer card shows a single CI record.

</td></tr><tr><td>

People

</td><td>

Displays top search results from the User \[sys\_user\] table. Each answer card shows a single user record.

</td></tr><tr><td>

Q&amp;A

</td><td>

Displays top search results extracted from HTML fields of records on the Knowledge \[kb\_knowledge\] table and tables that extend it. Each answer card shows a topic snippet and an answer snippet extracted from a single knowledge article.

</td></tr><tr><td>

Now Assist Q&amp;A

</td><td>

Displays the top search results extracted from the HTML fields of the records on the Knowledge \[kb\_knowledge\] table and the tables that extend it. Each answer card shows an answer snippet extracted by Now LLM from a knowledge article. For reference, the answer card also includes a link the user can select to view the source knowledge article.**Note:** Now Assist in the AI Search application \(com.ais\_assist\) is required to link the Now Assist Q&amp;A Genius Result configuration to your search profile. For more information, see [Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>## Customizing Recommended Actions UIB component for AI search

Customize the Recommended Actions UIB component to align with your organization's requirements:

-   Modify titles for the main heading, Recommended Actions tab, and Search tab.
-   Modify the order of the **Recommended Actions** and **Search** tabs.
-   Hide or show Recommended Actions and Search tabs.

For more information, see [Recommended Actions UIB setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/vancouver/now-components/sn-next-best-action-list-connected/uib-setup).

Explore advanced customization options, such as adjusting the number of results to view on a page, identifying genius results to add to the search profile, and configuring search sources. For more information, see [Configuring AI Search](https://www.servicenow.com/docs/access?context=configuring-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

