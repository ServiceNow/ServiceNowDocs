---
title: Request translations in Localization Workspace: Types
description: Add content types to a translation request in Localization Workspace. Your translation request can include multiple types of documents from tables across your instance.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Requesting translations in Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Request translations in Localization Workspace: Types

Add content types to a translation request in Localization Workspace. Your translation request can include multiple types of documents from tables across your instance.

## Before you begin

-   Content types correspond to tables. For details about making your content available to Localization Workspace, see [Types of Localizable content in Localization Workspace](../reference/lw-localizable-content.md).
-   Complete the first step in the Translation Request wizard, then proceed to this step. See [Request translations in Localization Workspace: Languages](lw-request-translations-langs.md).
-   Role required: localization\_requestor

## About this task

When you choose content types to include in your request, Localization Workspace retrieves all untranslated or partially translated documents from the tables. Then in the next step of the wizard \(Scope\), the retrieved list is displayed so that you can select or deselect specific documents.

A document may be considered partially translated when its original is updated after it was translated. In such cases it may be possible to synchronize the translated versions to the English original by translating only the new portion of the text.

The following procedure covers step number two in the Translation Request wizard.

## Procedure

1.  Complete the first step in the Translation request wizard \(Languages\), then proceed to **Types**.![The Types step in the Translation Request wizard in Localization Workspace, with the Knowledge type highlighted. There are four steps in the wizard. Types is step number two.](../image/lw-request-translations-types1.png)

2.  Choose the content types you want to translate by selecting the appropriate check boxes.

    **Note:** Content types that are not selectable may require table or role permissions. Ask your administrator to enable access. For more information see [Types of Localizable content in Localization Workspace](../reference/lw-localizable-content.md).

3.  Select **Save**.

    A saved translation request has a status of `Draft` in the **My Requests** list on the Home screen.

4.  Select the **Next** button to advance to the Scope step of translation request creation.


## What to do next

Advance to the third step in the wizard, **Scope**, where you can select specific documents for inclusion.

