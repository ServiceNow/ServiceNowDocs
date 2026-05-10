---
title: Index previously published TRM catalog records for AI Search
description: Manually trigger indexing for TRM catalog records that were published before you installed the May 2026 EA Workspace update, so that they are searchable through the Now Assist panel.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-17"
reading_time_minutes: 1
breadcrumb: [AI Search on the TRM catalog, Working with the publishing center, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Index previously published TRM catalog records for AI Search

Manually trigger indexing for TRM catalog records that were published before you installed the May 2026 EA Workspace update, so that they are searchable through the Now Assist panel.

## Before you begin

Role required: admin

Your instance must meet the following prerequisites:

-   Activate AI Search. Navigate to **All** and search for **AI Search Status**. The status page must display **AI Search is ready**. For instructions, see [Activate AI search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/configure-ui-builder-agent.md)
-   Enable the Now Assist panel. Navigate to **Now Assist Admin** &gt; **Now Assist Experiences** &gt; **Now Assist panel** and confirm the panel is turned on. For instructions, see [Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).
-   Install the Now Assist for EA plugin. For instructions, see [Configure Now Assist for Enterprise Architecture \(EA\)](../../../now-assist-ea/task/configure-now-assist-ea.md).
-   Install the EA Workspace May 2026 update from the ServiceNow Store.

## About this task

Installing the May 2026 EA Workspace update registers the TRM catalog as an indexed source in AI Search. TRM catalog records published after this update are automatically indexed. However, records published before the update are not indexed automatically and do not appear in the Now Assist panel search results until you complete this task.

## Procedure

1.  Navigate to **All** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Select the Knowledge Table record.

3.  In the **Child Tables** tab, confirm that the TRM Product \[sn\_apm\_ws\_kb\_template\_trm\_product\] table is listed and its **Active** column shows **true**.

4.  Select the **Index Selected Table/s** button.

    ![Adding a Technology Reference Model child table to the indexed source](../../image/eaw-image/index-trm-table.png)

    The **Generate Text Index - Single Table** dialog opens.

5.  Select the **sn\_apm\_ws\_kb\_template\_trm\_product** option from the list, then select **Index**.


## Result

Previously published TRM catalog records are indexed and searchable through the Now Assist panel.

**Parent Topic:**[AI Search on the TRM catalog](../../concept/eaw-concept/ai-search-trm-cat.md)

**Related topics**  


[AI Search on the TRM catalog](../../concept/eaw-concept/ai-search-trm-cat.md)

