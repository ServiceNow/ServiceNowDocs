---
title: Request translations in Localization Workspace: Languages
description: Add target languages to a translation request in Localization Workspace.
locale: en-US
release: yokohama
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2025-04-28"
reading_time_minutes: 1
breadcrumb: [Requesting translations in Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Request translations in Localization Workspace: Languages

Add target languages to a translation request in Localization Workspace.

## Before you begin

Ensure that you have installed the languages that you intend to add to your translation request.

Ensure that Localization Workspace is configured with the translation providers that you intend to use. See [Configure a translation provider](lw-configure-translation-provider.md).

Role required: localization\_requestor

## About this task

Your translation request can include multiple target languages for each document.

**Note:** In the Yokohama release, only requests from English into non-English target languages are supported. Requests from non-English source languages are not supported.

The following procedure covers step one of four steps in the Translation Request wizard.

## Procedure

1.  Navigate to **All** &gt; **Localization Workspace** &gt; **Home**.

2.  Select the **Request Translation** button to open the wizard.![The Translation Request modal, open to step one for languages.](../image/lw-request-translations-langs1.png)

    The **Translation Request** modal opens at the first step, **Languages**.

3.  In the **Short Description** field, enter a name that describes this translation request.

    The name becomes visible in the list on Localization Workspace's Home page.

4.  In the **Target Language** field, select a language from the list of languages activated on your instance.

5.  In the **Translation Provider** field, select a name from the list of providers available for the language you chose.

6.  Select the plus icon to add another language to your request, then repeat the previous two steps.

7.  Select **Save**.

8.  Select the **Next** button to advance to the Types step of translation request creation.


## What to do next

Advance to the next step in the wizard, **Types**.

