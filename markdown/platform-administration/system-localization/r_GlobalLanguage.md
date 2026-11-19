---
title: Set the default language for an instance
description: Change the language that appears by default for an instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/system-localization/r\_GlobalLanguage.html
release: zurich
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring System Localization, System Localization, Translation and localization, Configure core features, Administer]
---

# Set the default language for an instance

Change the language that appears by default for an instance.

## Before you begin

Activate the languages that your users need. For more information, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/system-localization/t_ActivateALanguage.md) for supported languages or [Translating to an unsupported language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/system-localization/self-localize.md) for custom translations.

Role required: admin

## About this task

This property defines the language that users with a role see if a language is not specified in their user record. Users without a role see the default guest language, as described in [User specific language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/system-localization/r_UserSpecificLanguage.md).

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **System Localization**.

2.  In the **Default language for the system \(two character values\)** field, enter a two-character language code.

    You can set the default language to any language that is active on the instance. The following language codes and languages are examples of possible values.

    \[Omitted image "DefaultLanguage.png"\] Alt text: List of two-character values for default language.

3.  Select **Save**.


