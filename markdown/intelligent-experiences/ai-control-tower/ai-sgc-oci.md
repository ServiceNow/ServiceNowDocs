---
title: AI Service Graph Connector for OCI
description: The AI Service Graph Connector for OCI enables you to discover and import AI assets from your OCI environment into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/ai-sgc-oci.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# AI Service Graph Connector for OCI

The AI Service Graph Connector for OCI enables you to discover and import AI assets from your OCI environment into ServiceNow AI Control Tower.

The AI Service Graph Connector for OCI integrates with your OCI account to catalog AI systems, agents, models, and prompts. Usage data is automatically collected and populated into the AI Control Tower value dashboard, providing comprehensive visibility and governance of your AI operations.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

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


## OCI prerequisites

Create a Java KeyStore \(JKS\) certificate, configure OCI IAM policies, bind the policies to the OCI user, and configure the connection in your ServiceNow instance. For setup instructions and API details, see the [Service Graph Connector for OCI - Setup Instructions \[KB2898105\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2898105) article in the Now Support Knowledge Base.

After completing the OCI setup requirements, register the connector in your ServiceNow instance.

