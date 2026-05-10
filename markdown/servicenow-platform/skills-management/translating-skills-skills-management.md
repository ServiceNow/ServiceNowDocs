---
title: Translate text in Skills Management
description: Translate skills and descriptions when you add new skills in Skills Management.
locale: en-US
release: australia
product: Skills Management
classification: skills-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Skills Management, Skills Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Translate text in Skills Management

Translate skills and descriptions when you add new skills in Skills Management.

## Before you begin

Role required: skill\_admin

Activate the relevant translation plugins. For more information, see [Localization Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-framework/localization-framework-landing.md).

## About this task

Translate skill names and the description using the following fields that support the translated text data type in the Skill \[cmn\_skill\] table:

-   **Display Skill Name**

    Auto-populates the corresponding value in the **Name** field.

-   **Description**

## Procedure

1.  [Add a skill](t_CreateASkill.md).

2.  For the newly added skills, load the translation to the Translated text \[sys\_translated.text\] table.

3.  Set the session language based on the language plugin that you've installed.

    **Note:** Every time you add new skills, you must load the translation to the Translated text table and set the session language.

    The text in the **Display Skill Name** and **Description** fields are translated.

    For more information on translating custom content, see [Translating custom content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/translating-applications.md).


