---
title: Verify that your instance meets the prerequisites for AI Search for Next Experience
description: Walk through Guided Setup tasks to confirm that your instance meets the requirements for AI Search for Next Experience.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring AI Search for Next Experience, AI Search for Next Experience, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Verify that your instance meets the prerequisites for AI Search for Next Experience

Walk through Guided Setup tasks to confirm that your instance meets the requirements for AI Search for Next Experience.

## Before you begin

The AI Search for Next Experience ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install AI Search for Next Experience](install-ais-next-experience-app.md).

Role required: ais\_admin

## About this task

The **Prerequisites** Guided Setup tasks walk you through verifying that your instance can use AI Search for Next Experience. Complete these tasks before you begin migrating your Zing search application configurations.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search for Next Experience** &gt; **Guided Setup for Zing to AI Search Migration**.

2.  Select **Get Started**.

3.  In the **Prerequisites** category, select **Get Started**.

4.  Confirm that AI Search is provisioned and enabled on your instance.

    1.  In the **Confirm that AI Search is enabled** task, select **Configure**.

        A modal window reports whether AI Search is provisioned and enabled on your instance.

    2.  If the window reports **AI Search is ready**, select **Close**, then select **Mark as Complete** for the **Confirm that AI Search is enabled** task.

    3.  If the window reports any other status, select **Close**, then repeat this task after AI Search is provisioned and enabled on your instance.

5.  Confirm that Next Experience is enabled on your instance.

    1.  In the **Confirm that Next Experience is Enabled** task, select **Configure**.

        A modal window reports whether Next Experience is enabled on your instance.

    2.  If the system reports **Next Experience is enabled**, select **Close**, then select **Mark as Complete** for the **Confirm that Next Experience is Enabled** task.

    3.  If the system reports any other enablement status, ask your administrator to enable Next Experience on your instance, then repeat this task after it's enabled.

        For details on enabling Next Experience, see [Enable Next Experience](https://www.servicenow.com/docs/access?context=next-experience-adoption-paths&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

6.  Index content and metadata for AI Search indexed sources used in global search.

    1.  In the **Index searchable content and metadata for global search sources** task, select **Configure**.

        The AI Search Indexed Sources list opens in a new browser tab.

    2.  Select all indexed sources marked with the alert triangle icon ![](../image/icon-alert-triangle.png), then index their content by selecting **Actions on selected rows…** &gt; **Index All Tables**.

        For more information on indexing tables from multiple indexed sources, see [Perform a full table index or reindex for multiple AI Search indexed sources](index-multiple-sources-ais.md).

    3.  When indexing is complete, close the browser tab and return to the **Prerequisites** Guided Setup category tab.

    4.  Select **Mark as Complete** for the **Index searchable content and metadata for global search sources** task.

7.  When all three **Prerequisites** tasks are marked as complete, select the Back icon ![](../image/icon-back.png) to return to the top-level **Guided Setup for Zing to AI Search Migration** page.


## What to do next

Now that you've satisfied the prerequisites, it's time to migrate your existing Zing search application configurations for use with AI Search. For details on this procedure, see [Migrate Zing search application configurations to AI Search](migrate-srch-apps-ais-next-exp.md).

**Parent Topic:**[Configuring AI Search for Next Experience](../concept/configuring-ais-next-experience.md)

