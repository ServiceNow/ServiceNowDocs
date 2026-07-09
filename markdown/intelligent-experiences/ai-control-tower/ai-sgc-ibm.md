---
title: AI Service Graph Connector for IBM
description: The AI Service Graph Connector for IBM enables you to discover and import AI assets from your IBM environment into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/ai-sgc-ibm.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for IBM

The AI Service Graph Connector for IBM enables you to discover and import AI assets from your IBM environment into ServiceNow AI Control Tower.

The AI Service Graph Connector for IBM integrates with your IBM account to catalog AI systems, agents, models, and prompts. Usage data is automatically collected and populated into the AI Control Tower value dashboard, providing comprehensive visibility and governance of your AI operations.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported ServiceNow versions

-   Zurich \(Patch 8\)
-   Australia \(Patch 1\)

## User roles

You must have one of the following roles:

-   sn\_ai\_disc.discovery\_admin
-   sn\_cmdb\_int\_util.sgc\_admin

## ServiceNow prerequisites

Complete the following setup steps when configuring the connector for the first time.

**Note:** Updating data source access and clearing cache are prerequisites that must be completed only once, when setting up a new instance for the first time.

Update data source access

The connector requires write permissions to the Data Source table to create data sources.

To enable data source creation:

1.  Select **Global** from the application picker.
2.  Navigate to **Application Access**.
3.  Select the **Can create**, **Can update**, and **Can delete** check boxes.
4.  Select **Update**.
5.  Switch to the connector application scope.

Clear cache

Clear the cached data for the Data Source and Tables.

To clear the cache:

1.  Navigate to **System Definition** &gt; **Background Scripts**.
2.  Enter the following script in the **Run Script** text box:

    ```
    GlideTableManager.invalidateTable('sys_data_source');
    GlideCacheManager.flushTable('sys_data_source');
    GlideTableManager.invalidateTable('sys_db_object');
    GlideCacheManager.flushTable('sys_db_object');
    
    ```

3.  Select **Run Script**.

    **Note:** The script might take several minutes to complete. After completion, switch to the connector application scope.


## IBM prerequisites

Generate an IBM Cloud API Key and configure access for the connector before creating a connection. For setup instructions and API details, see the [AI Service Graph Connector for IBM — Setup Instructions \[KB2901071\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2901071) article in the Now Support Knowledge Base.

After completing the IBM setup requirements, register the connector in your ServiceNow instance.

