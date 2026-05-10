---
title: Request translations in Localization Workspace: Languages
description: Add target languages to a translation request in Localization Workspace.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Requesting translations in Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Request translations in Localization Workspace: Languages

Add target languages to a translation request in Localization Workspace.

## Before you begin

-   Ensure that the languages you intend to add to your translation request have been installed on your instance.
-   Ensure that the language providers that you intend to use have been configured. See [Configure a language provider](lw-configure-translation-provider.md).
-   Role required: localization\_requestor.

## About this task

Your translation request can bundle multiple target languages and multiple content types. Each language in the request can include different target documents.

**Note:** In the Australia release, only requests from English into non-English target languages are supported. Requests from non-English source languages are not supported.

The following procedure covers step one of four steps in the Translation Request wizard.

## Procedure

1.  Navigate to **All** &gt; **Localization Workspace** &gt; **Home**.

2.  Select **Request Translation** to open the wizard.![The Translation request wizard window, open to step one for language selection. In this example, selecting a language group has auto-populated three language rows.](../image/lw-request-translations-langs1.png)

    The **Translation request** wizard opens at the first step, **Languages**.

3.  In the **Short Description** field, enter a name for the translation request.

    The Short Description is displayed in the **My Requests** list on the Home screen, so you can find and monitor your request later. For information see [Localization Workspace Home and translation job status](../concept/lw-status-synchronization.md).

4.  Select target languages or language groups according to the following guidance.

<table id="choicetable_ff5_wjv_khc"><tbody><tr><td id="d292827e157">

**Language**

</td><td>

To select an individual language:1.  In the **Target language** field, select an available language from the drop-down list.
2.  In the **Translation provider** field, select a name from the list of providers available for the language you chose.
 You can add more than one language to a request.

</td></tr><tr><td id="d292827e181">

**Groups**

</td><td>

When you select a check box for a language group, the Target language and Translation provider fields auto-populate.-   You can add more than one language group to a translation request.
-   After you add a language group to request, you can manually delete individual languages from it. Deletion in the wizard applies only to this request; the definition of the language group doesn't change.
-   You can include a mix of language groups and individual languages in one request.
-   If a language is included multiple times in one request, Localization Workspace clears the value of the Translation provider field. You must then manually select the desired Translation provider for that language.


</td></tr></tbody>
</table>5.  Add another language by selecting the plus icon ![](../../../reuse/icons/product-icons/plus-outline-24.svg), or add another language group by selecting its check box.

6.  Select **Save**.

    A saved translation request has a status of `Draft` in the **My Requests** list on the Home screen.

7.  Select the **Next** button to proceed to the Types step of translation request creation.


## What to do next

Advance to the next step in the wizard, **Types**, to select content for translation.

