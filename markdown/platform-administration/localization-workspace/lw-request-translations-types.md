---
title: Request translations in Localization Workspace: Types
description: Add content types to a translation request in Localization Workspace. Your translation request can include multiple types of documents.
locale: en-US
release: yokohama
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2025-04-28"
reading_time_minutes: 1
breadcrumb: [Requesting translations in Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Request translations in Localization Workspace: Types

Add content types to a translation request in Localization Workspace. Your translation request can include multiple types of documents.

## Before you begin

Ensure that Restricted Caller Access privileges are set to allow Localization Workspace to access the tables where your content is stored. See .

Ensure that artifacts in Localization Framework are fully configured. See [Artifact configurations](../../localization-framework/concept/framework-configuration.md).

Complete the first step in the Translation Request wizard, then proceed to this step. See [Request translations in Localization Workspace: Languages](lw-request-translations-langs.md).

Role required: localization\_requestor

## About this task

When you indicate which content types to include in your request, Localization Workspace retrieves all untranslated or partially translated documents and displays them to you. Then you can select or deselect specific documents from the list.

The following procedure covers step two of four steps in the Translation Request wizard.

## Procedure

1.  Complete the first step in the Translation request wizard \(Languages\), then proceed to **Types**.![The Types step in the Translation Request wizard in Localization Workspace, with the Knowledge type highlighted.](../image/lw-request-translations-types1.png)

2.  Choose the content types you want to translate by selecting the appropriate check boxes.

    **Note:** Content types that are not selectable may require Restricted Caller Access privileges to allow Localization Workspace to retrieve documents from those tables. Ask your administrator to enable access. See .

3.  Select **Save**.

4.  Select the **Next** button to advance to the Scope step of translation request creation.


## What to do next

Advance to the next step in the wizard, **Scope**, where you can select specific documents for inclusion.

