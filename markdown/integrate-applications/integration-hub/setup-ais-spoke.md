---
title: Set up the AI Search spoke
description: Configure the AI Search spoke to index content from a third-party application.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [AI Search Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the AI Search spoke

Configure the AI Search spoke to index content from a third-party application.

## Before you begin

-   Request an Integration Hub subscription
-   Activate the AI Search spoke
-   Role required: admin

## Procedure

1.  Create an external content schema table.

    To learn more about external content schema tables, see [Indexing and searching external content in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/external-content-ais.md).

    1.  Navigate to **AI Search** &gt; **Create Schema**.

    2.  In the field, provide the name of your schema table.

        For example, `My application schema table`.

    3.  Select **Submit**.

2.  Create an indexed source for content from your third-party application.

    To learn more about indexed sources, see [Indexed sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/indexed-sources-ais.md).

    1.  Navigate to **AI Search** &gt; **Indexed Sources**.

    2.  Select **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the indexed source. For example, `My application indexed source`.|
        |Source|External content schema table that you created for the third-party application. For example, `My application schema table`.|
        |Active|Option to enable the indexed source.|

    4.  Select **Submit**.

        **Note:** Ensure that the **Type** of the indexed source is **external**.

        You can now use the AI Search spoke actions.

3.  Add the third-party application's domain URL to the list of trusted domains.

    1.  Navigate to **AI Search Spoke** &gt; **Trusted Domains**.

    2.  Select **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the trusted domain record. For example, `My sample application's trusted domain`.|
        |Domain|URL of the trusted domain. For example, `https://example.com`.|

4.  Create a search source for your new indexed source.

    To learn more about search sources, see [Search sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/search-sources-ais.md).

    1.  Navigate to **AI Search** &gt; **Search Experience** &gt; **Search Sources**.

    2.  Select **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the search source. For example, `My application search source`.|
        |Application|Application scope. Select **AI Search Spoke**.|
        |Indexed Source|Indexed source that you created for the third-party application. For example, `My application indexed source`.|
        |Conditions|Filter conditions that records must satisfy to be searchable.|

    4.  Select **Submit**.

5.  Create a search profile that includes your new search source.

    For more information about configuring and publishing search profiles, see [Search profiles in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/defining-search-profiles-ais.md).

    1.  Navigate to **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

    2.  Select **New**.

    3.  Fill in a **Label** value to identify the search profile.

        For example, `My application search profile`.

    4.  Right-click the form header and select **Save**.

    5.  In the **Search Sources** tab, select **Link Existing**.

    6.  In **Search Source**, select the search source that you created for the third-party application.

        For example, **My application search source**.

    7.  Select **Submit**.

    8.  Select **Publish**.


## Result

You can now use the AI Search spoke actions to indexed content from the third-party application. To view the indexed content, you can use the Search Preview UI from the Advanced AI Search Management Tools application.

For details on the Search Preview UI, see [Search Preview UI for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/ai-search-preview.md). To learn more about the Advanced AI Search Management Tools application, see [Analytics and Reporting Solution for Advanced AI Search Management Tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/adv-ais-mgmt-tools-content-pack.md).

