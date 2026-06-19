---
title: Localization Framework Properties: Update Set Strategies
description: Use update sets to migrate your translations to another instance. Configure properties for update sets according to your business requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/localization-framework/lf-update-set-strategies.html
release: australia
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [Localization Framework settings, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Localization Framework Properties: Update Set Strategies

Use update sets to migrate your translations to another instance. Configure properties for update sets according to your business requirements.

Update sets enable you to transfer your artifact translations to other instances. For background information on update sets, see System update sets.

For localization tasks, previously the default was to create a dedicated update set per task in the scope of the artifact. Alternatively, with sys properties you can specify your update set strategy: bundle translations into one update set, or distribute into granular update sets.

The settings for update set strategies vary according to the type of translation, defined as follows:

-   **localization tasks**

    Part of workflows that often include approval processes. These are based on tasks.

    Property name: com.glide.sn\_lf.update\_set.strategy.request\_translations.

-   **adhoc**

    Edited and published directly by the localization editor, from the artifact record \(such as a catalog item\). The **Edit translation** button is visible to the editor, and it opens a UI page for translation. Adhoc translations are processed in the user context.

    Property name: com.glide.sn\_lf.update\_set.strategy.edit\_translations.


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

**Parent Topic:**[Localization Framework settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-framework/localization-settings.md)

