---
title: AI Search on the TRM catalog
description: Use the Now Assist panel to search published Technology Reference Model \(TRM\) catalog records using natural language queries.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-17"
reading_time_minutes: 3
breadcrumb: [Working with the publishing center, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# AI Search on the TRM catalog

Use the Now Assist panel to search published Technology Reference Model \(TRM\) catalog records using natural language queries.

Installing the May 2026 EA Workspace update with Now Assist for EA automatically registers the TRM catalog as a searchable source in AI Search. You can then use the Now Assist panel to ask natural language questions about your published TRM catalog records and get answers with citations linked to the source knowledge articles.

For example, you can ask the Now Assist panel questions such as *List all published TRM products* and receive a summarized response with references to the relevant catalog records.

![An example showing how AI Search works for searching all published TRM catalogs](../../image/eaw-image/ai-search-trm-cat.png)

Sample queries:

-   What is the approved software for databases?
-   Which technologies are pending retirement?
-   What is the approval status of EC2?
-   List all published TRM products in the infrastructure category.
-   What is the lifecycle status of Oracle Database?

## How AI Search works with the TRM catalog

EA Workspace ships with an AI Search configuration record that registers the TRM catalog \[sn\_apm\_ws\_kb\_template\_trm\_product\] as an indexed source.

After you install the May 2026 update, the indexing behavior depends on when your TRM catalog records were published:

-   Records published after the update: Automatically indexed and searchable through the Now Assist panel. No additional configuration is required.
-   Records published before the update: Not automatically indexed. You must manually trigger indexing. See [Index previously published TRM catalog records for AI Search](../../task/eaw-task/index-archive-pub-trm-cat.md).

## Prerequisites

Before you can search TRM catalog records using AI Search, verify the following are configured on your instance:

-   AI Search is activated. Navigate to **All** and search for **AI Search Status**. The status page must display **AI Search is ready**. For instructions, see Activate AI search
-   Now Assist panel is enabled. Navigate to **Now Assist admin** &gt; **Now Assist Experiences** &gt; **Now Assist panel** and verify that the panel is turned on. For instructions, see Activate the Now Assist panel standard chat.
-   Install the Now Assist for EA plugin. For instructions, see [Configure Now Assist for Enterprise Architecture \(EA\)](../../../now-assist-ea/task/configure-now-assist-ea.md).
-   At least one TRM catalog is published to a knowledge base. AI Search returns results only for published records. See [Publish a TRM catalog to the knowledge base](../../task/eaw-task/publish-trm-cat-to-kb.md).

-   **[Index previously published TRM catalog records for AI Search](../../task/eaw-task/index-archive-pub-trm-cat.md)**  
Manually trigger indexing for TRM catalog records that were published before you installed the May 2026 EA Workspace update, so that they are searchable through the Now Assist panel.

**Parent Topic:**[Working with the publishing center](working-with-publishing-center.md)

**Related topics**  


[Index previously published TRM catalog records for AI Search](../../task/eaw-task/index-archive-pub-trm-cat.md)

[Publish a TRM catalog to the knowledge base](../../task/eaw-task/publish-trm-cat-to-kb.md)

[Access the published TRM catalog knowledge base](../../task/eaw-task/access-the-published-kb.md)

