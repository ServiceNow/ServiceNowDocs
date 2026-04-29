---
title: Add a new Unified Navigation workspace search configuration to AI Search for Next Experience
description: Enable Unified Navigation search for newly installed workspaces in AI Search for Next Experience.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring AI Search for Next Experience, AI Search for Next Experience, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Add a new Unified Navigation workspace search configuration to AI Search for Next Experience

Enable Unified Navigation search for newly installed workspaces in AI Search for Next Experience.

## Before you begin

The AI Search for Next Experience ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install AI Search for Next Experience](install-ais-next-experience-app.md).

You must have already enabled AI Search for Next Experience on your instance. For details on this procedure, see [Enable AI Search for Next Experience](enable-ais-next-exp-app.md).

Role required: ais\_admin

## About this task

When a new workspace application that includes a search application configuration is installed on your instance, you can enable search for the workspace in AI Search for Next Experience by following this procedure.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search for Next Experience** &gt; **Guided Setup for Zing to AI Search Migration**.

2.  In the **Post-Migration Actions** category, select **Get Started**.

3.  In the **When a new Next Experience workspace has been added to your instance** task, open the Zing to AI Search Migration Job form by selecting the **migration tool** link.

    A modal window shows a list of Zing search application configurations and their migration status.

4.  If the new workspace's search application configuration shows **Migrated** status, reindex its associated content and publish its search profiles and dictionaries.

    1.  Repeat the **Index searchable content and metadata for global search sources** task in the **Prerequisites** Guided Setup category.

        For details on this procedure, see [Verify that your instance meets the prerequisites for AI Search for Next Experience](verify-ais-next-exp-prereqs.md).

    2.  Publish all search profiles and dictionaries provided by the new workspace.

        To learn how to publish search profiles, see [Publish an AI Search search profile](publish-search-profile-ais.md). For details on publishing stop word and synonym dictionaries, see [Create stop words](create-stop-word-ais.md) and [Create synonyms](create-synonym-ais.md).

5.  If the new workspace's search application configuration shows **Needs migration** status, migrate it for use with AI Search.

    1.  Close the modal window.

        **Note:** You can reopen the list of Zing search application configurations at any time by selecting the **View Search Application Migration Status** related link.

    2.  In the **Search Application Configuration** field, use the Lookup using list icon ![](../image/icon-lookup-using-list.png) to select the new Zing search application configuration.

        **Note:** Only Zing search application configurations with **Needs migration** status are available for selection. Application configurations with **Migrated** status already have corresponding AI Search application configurations.

    3.  To have the system send email notifications to users when indexing of content for the migration job starts and completes, add those users to the watch list.

        **Note:** The system automatically adds the current user to the watch list when a migration job is created or updated.

    4.  Select **Start Migration**.

        The migration tool converts the Zing search application configuration for use with AI Search, and the migration job's state changes from **Pending Conversion** to **Configuration Converted**.

    5.  Select **Accept All Changes**.

        The system displays proposed changes to system tables in the Changes to Review related list.

    6.  Select **Commit Changes**.

        The system commits the changes to system tables shown in the Changes to Review related list, and the migration job's state changes to **Configuration Committed**.

    7.  Select **Index Searchable Content**.

        AI Search indexes content and metadata for new indexed sources created by the migration job. When indexing completes, the job's state changes to **Indexing Complete** and the modal window with the list of Zing search application configurations reopens.

6.  Refresh the list of search application configurations included in AI Search for Next Experience.

    1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search for Next Experience** &gt; **Guided Setup for Zing to AI Search Migration**.

    2.  In the **Complete migration to AI Search** category, select **Edit**.

    3.  In the **Activate AI Search for all Next Experience search applications** task, select **Configure**.

        A modal window reports whether AI Search for Next Experience is enabled on your instance.

    4.  Select **Refresh AI Search for Next Experience**.


## Result

AI Search for Next Experience updates to include the new workspace application's search application configurations. The system uses AI Search as the search engine for workspace searches from the Unified Navigation search field.

## What to do next

Notify all users of your instance that they need to log out and back in before they can use the new workspace search in AI Search for Next Experience.

**Parent Topic:**[Configuring AI Search for Next Experience](../concept/configuring-ais-next-experience.md)

