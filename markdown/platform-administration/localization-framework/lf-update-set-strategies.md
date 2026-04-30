---
title: Localization Framework Properties: Update Set Strategies
description: Use update sets to migrate your translations to another instance. Configure properties for update sets according to your business requirements.
locale: en-US
release: zurich
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Localization Framework settings, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer]
---

# Localization Framework Properties: Update Set Strategies

Use update sets to migrate your translations to another instance. Configure properties for update sets according to your business requirements.

Update sets enable you to transfer your artifact translations to other instances. For background information on update sets, see [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

For localization tasks, the default has been to create a dedicated update set per task in the scope of the artifact. In the Zurich release, you can specify your update set strategy to control whether translations are bundled into one update set, or distributed into granular update sets.

The settings for update set strategies vary according to the type of translation, defined as follows:

-   **localization tasks**

    Part of workflows that often include approval processes. These are based on tasks.

-   **adhoc**

    Edited and published directly by the localization editor, from the artifact record \(such as a catalog item\). The **Edit translation** button is visible to the editor, and it opens a UI page for translation. Adhoc translations are processed in the user context.


<table id="table_r15_kxt_d1c"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Save translation in update set created for each localization task

</td><td>

The system will create a dedicated update set for each task, using the task name.This strategy is most appropriate when there are a limited number of tasks.

</td></tr><tr><td>

Save translations in 'LF: Translations' update set

</td><td>

Granular update sets are not created. Instead, the system creates or reuses one update set named 'LF: Translations', and saves all tasks to it.This strategy can be more convenient when there are many localization tasks.

</td></tr></tbody>
</table><table id="table_swb_5yt_d1c"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Save translations in user preferred update set

</td><td>

The translations are written to the update set that the user has specified for a scope, because the processing happens in the user's context.When artifacts are in an application scope, their translations are saved to the user's preferred update set for that scope.

</td></tr><tr><td>

Save translations in 'LF: Translations' update set

</td><td>

The system creates or reuses one update set named 'LF: Translations', and all adhoc translations are written to it.

</td></tr></tbody>
</table>To set these properties, navigate to **Localization Framework** &gt; **Properties**. Choose the appropriate strategy and select **Save**.

**Parent Topic:**[Localization Framework settings](localization-settings.md)

