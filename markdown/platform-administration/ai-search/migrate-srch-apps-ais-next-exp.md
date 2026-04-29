---
title: Migrate Zing search application configurations to AI Search
description: Walk through a Guided Setup task to migrate your existing Zing search application configurations to AI Search application configurations.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring AI Search for Next Experience, AI Search for Next Experience, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Migrate Zing search application configurations to AI Search

Walk through a Guided Setup task to migrate your existing Zing search application configurations to AI Search application configurations.

## Before you begin

The AI Search for Next Experience ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install AI Search for Next Experience](install-ais-next-experience-app.md).

You must have already completed the **Prerequisites** Guided Setup tasks. For details on completing these tasks, see [Verify that your instance meets the prerequisites for AI Search for Next Experience](verify-ais-next-exp-prereqs.md).

Role required: ais\_admin

## About this task

The base system includes Zing search application configurations for global search and some workspaces. To use AI Search for Next Experience, you need AI Search configurations for these search applications.

You can create the new AI Search application configurations you need by migrating settings from your existing Zing search application configurations. The **Convert Zing search applications** Guided Setup task walks you through this procedure.

**Note:** When you migrate a Zing search application configuration, the system creates a new search application configuration for use with AI Search. This procedure doesn't delete or change your original Zing search application configuration.

Migration of a Zing search application configuration to AI Search includes these steps:

1.  The migration tool analyzes your selected Zing search application configuration and determines what record changes in ServiceNow AI Platform® tables are needed to replicate its settings in a new AI Search application configuration.
2.  You accept the proposed migration changes for review, and then commit them to make the required record changes in ServiceNow AI Platform tables.
3.  You index content and metadata from any new indexed sources that the migration job created.

For more information on AI Search application configurations, see [Search application configurations](../concept/defining-search-app-cfgs-ais.md). To learn more about indexing content and metadata from AI Search indexed sources, see [Indexed sources in AI Search](../concept/indexed-sources-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search for Next Experience** &gt; **Guided Setup for Zing to AI Search Migration**.

2.  In the **Convert Zing search applications** category, select **Get Started**.

3.  In the **Migrate settings for a Next Experience search application** task, open the Zing to AI Search Migration Job form by selecting **Configure**.

    A modal window shows a list of Zing search application configurations and their migration status. Custom search application names are only translated to your session language if you've created appropriate Message \[sys\_ui\_message\] table records for them. For details on translating message strings by creating Message table records, see [Translate a client script message](../../localization/task/t_TranslateAClientScriptMessage.md).

4.  Close the modal list of Zing search application configurations.

    **Note:** You can reopen the list of Zing search application configurations at any time by selecting the **View Search Application Migration Status** related link.

5.  For each Zing search application configuration with **Needs migration** status, migrate the search application configuration to AI Search.

    1.  In the **Search Application Configuration** field, use the Lookup using list icon ![](../image/icon-lookup-using-list.png) to select the Zing search application configuration that you want to migrate to AI Search.

        **Note:** Only Zing search application configurations with **Needs migration** status are available for selection. Application configurations with **Migrated** status already have corresponding AI Search application configurations.

    2.  To have the system send email notifications to users when indexing of content for the migration job starts and completes, add those users to the watch list.

        **Note:** The system automatically adds the current user to the watch list when a migration job is created or updated.

    3.  Select **Start Migration**.

        The migration tool converts the Zing search application configuration for use with AI Search, and the migration job's state changes from **Pending Conversion** to **Configuration Converted**.

    4.  Select **Accept All Changes**.

        The system displays proposed changes to system tables in the Changes to Review related list.

    5.  Select **Commit Changes**.

        The system commits the changes to system tables shown in the Changes to Review related list, and the migration job's state changes to **Configuration Committed**.

    6.  Select **Index Searchable Content**.

        AI Search indexes content and metadata for new indexed sources created by the migration job. When indexing completes, the job's state changes to **Indexing Complete** and the modal window with the list of Zing search application configurations reopens.

6.  When all Zing search application configurations in the modal list show **Migrated** status, close the browser tab and return to the **Convert Zing search applications** Guided Setup category tab, then select the Back icon ![](../image/icon-back.png) to return to the top-level **Guided Setup for Zing to AI Search Migration** page.


## What to do next

Now that you've got AI Search application configurations for global search and your workspaces, it's time to enable AI Search for Next Experience on your instance. For details on this procedure, see [Enable AI Search for Next Experience](enable-ais-next-exp-app.md).

**Parent Topic:**[Configuring AI Search for Next Experience](../concept/configuring-ais-next-experience.md)

