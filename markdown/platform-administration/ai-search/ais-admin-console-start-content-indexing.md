---
title: Index the content from an indexed source for searchability
description: Enable AI Search to index the records from your source tables to make the content searchable.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing the indexed sources from the AI Search Admin console, Using AI SearchAdmin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Index the content from an indexed source for searchability

Enable AI Search to index the records from your source tables to make the content searchable.

## Before you begin

Role required: admin or ais\_admin

## About this task

You can index the existing records in the source table and any child tables that you set up for indexing. Before starting the indexing process, you can also test the indexed source configuration to identify and resolve any issues early, instead of waiting for the full indexing process to complete.

If you add, change, or remove an indexed source attribute, or update the indexed values for fields on referenced tables, you must reindex the content from an internal source. You can do it manually by following the steps in the procedure again. For more information, see [Indexing content from AI Search indexed sources](../concept/indexing-content-ais.md).

You can also index the content from an indexed source for external documents. For more information, see [Indexing and searching external content in AI Search](../concept/external-content-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  On the **Shared Configurations** tab, select **Indexed Sources**.

3.  Select the indexed source that you want to index.

    The selected indexed source opens in the Configuration form view.

4.  Select **Start index job**.

5.  Start indexing.

    ![Start index job dialog box in the AI Search Admin console, where you can index search content either fully or for specific source tables. It also includes an option to test the indexed sources before beginning the actual indexing process.](../image/ais-start-indexing.png)

<table id="choicetable_wty_414_tdc"><thead><tr><th align="left" id="d153086e156">

Option

</th><th align="left" id="d153086e159">

Procedure

</th></tr></thead><tbody><tr><td id="d153086e165">

**Enable AI Search indexing content from internal indexed sources, including both parent table and its child tables**

</td><td>

1.  Select **Full index**.
2.  Select **Start**.


</td></tr><tr><td id="d153086e189">

**Enable AI Search indexing content from the source tables, including only the selected child tables**

</td><td>

1.  Select **Select source tables to index**.
2.  Select the source tables that are defined in the indexed source from the **Tables** field.
3.  Select **Start**.


</td></tr><tr><td id="d153086e221">

**Test the indexed source configuration**

</td><td>

1.  Select **Quick indexing test**.
2.  Select the tables that are defined in the indexed source from the **Tables** field.
3.  Enter the number of AI Search index records you want to test in the **Number of records** field.
4.  Select **Start**.


</td></tr></tbody>
</table>    The AI Search Indexed Source History page appears.

6.  To monitor the progress of the indexing task, refresh the AI Search Indexed Source History form page.

    When the task completes, the **Ingestion State** field of the indexed source shows its status as indexed.

7.  Return to the list of indexed sources by selecting the back icon ![](../../../use/using-forms/image/FormBackUI15.png).


## Result

AI Search indexes content from existing records in the indexed source. Indexing continues on a scheduled basis. You must repeat this task for the indexed sources If you want to reindex their content before the next scheduled indexing run, you must repeat this task for the indexed sources.

## What to do next

Define search sources to make searchable content from the indexed source available in user search experiences. For details on creating search sources, see [Create or edit an EVAM view definition](ais-admin-console-evam-configurations.md).

**Parent Topic:**[Managing the indexed sources from the AI Search Admin console](../concept/ais-managing-indexed-source.md)

