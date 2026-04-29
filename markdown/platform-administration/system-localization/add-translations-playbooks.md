---
title: Add translations for Playbooks
description: Make Playbooks available in multiple languages during runtime, to support worldwide business processes.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 1
breadcrumb: [Translating individual UI strings, Translating custom content, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Add translations for Playbooks

Make Playbooks available in multiple languages during runtime, to support worldwide business processes.

## Before you begin

-   Role required: admin or playbook.admin
-   To enable custom translations for playbooks, install the 27.1 app version or later.
-   Activate any playbooks that you want to translate.
-   To learn more about translating custom content in general, see [Translating custom content](../../localization/concept/translating-applications.md).

## About this task

UI Message records are used to translate the text in your playbooks to different languages at runtime, similar to the way system messages are translated on the platform. To learn more about the Message table \[sys\_ui\_message\] in general, see [Message table](../../localization/reference/r_MessageTable.md).

The playbook text that you can create translations for are:

-   Playbook Label
-   Stage Label
-   Activity Label
-   Activity Description
-   HTML and string Activity UI Layout properties

**Note:** Automation inputs such as text used to create emails or records are not translated. Only text that is shown at runtime within a Playbook Experience is translatable.

## Procedure

1.  Navigate to Workflow Studio, open playbook, activate playbook.

2.  Open the **All** menu.

3.  In the filter bar, type and enter **sys\_pd\_process\_definition.list**.

4.  Select the playbook that you want to add translations for.

5.  Open the **Translated Messages** tab.

    All of your playbook text is listed here.

6.  Open a piece of text that you want to translate.

7.  From the **Language** drop-down, select the language that you want to translate to.

8.  In the **Message** field, enter the translation.

9.  Right-click on the form header to open the context menu, and select **Save**.

    Your translation is saved.

10. Repeat steps 1-8 to add more translations.


## Result

When the playbook runs, the translated content appears for agents in their user session language.

![The message translated into Spanish.](../images/playbook-translation-runtime.png)

