---
title: Translate announcement content
description: Translate announcement content manually or request translation through the Localization Framework.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/eslate-translate-announcement.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 2
keywords: [translation, localization, switch language, Employee Slate, announcements]
breadcrumb: [Employee communications, Working with EmployeeWorks capabilities, ServiceNow EmployeeWorks Web App, Unified Employee Experience, Employee Service Management]
---

# Translate announcement content

Translate announcement content manually or request translation through the Localization Framework.

## Before you begin

Create the announcement in its source language before you translate it. For more information, see [Create announcements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown).

Role required: content\_manager or content\_admin

## About this task

After you save an announcement, a language menu becomes available on the record. Use this menu to manually translate the content or to request translation through the Localization Framework.

-   **Switch language** creates a translated copy of the content that you edit manually.
-   **Manage translations** sends a translation request to the Localization Framework for one or more languages.

**Note:** Schedule fields aren't editable on a translated copy. The translated content uses the publishing schedule from the source announcement.

## Procedure

1.  Open the announcement and select the language menu.

2.  To translate content manually, select **Switch language** and select a target language.

    The system creates a language-specific copy of the content and prefills the image and link fields from the source. Schedule fields remain read-only and inherit the source schedule.

    -   Each language pack shows a **Translated** tag or an untranslated tag based on its current state.
    -   Edit the translatable text and image fields, then select **Save** to create the translated draft.
    -   The translated content has its own version history, independent of the source announcement.
    -   To translate the same source content into another language, return to the source language first and select **Switch language** again.
3.  To request translation through the Localization Framework instead, select **Manage translations**.

    A dialog box opens with **Untranslated**, **Requested**, and **Translated** tabs.

4.  From the **Untranslated** tab, select one or more languages and select **Request translations**.

    The system creates a localization task for each selected language and moves the language to the **Requested** tab.

    **Note:** The Localization Framework translates against the content version present when you submitted the request. If you update the source content afterward, cancel and resubmit the request so the translation reflects the update.

5.  To cancel a pending request, open it from the **Requested** tab and delete it.

    The localization task closes as incomplete, and you can request the translation again.


## Result

When the localization task completes, the system publishes the translated content and moves the language to the **Translated** tab.

**Note:** If a Localization Framework request for a language is still open, manually translating that language shows a warning. It doesn't block you from continuing with the manual translation.

**Related topics**  


[Create announcements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown)

