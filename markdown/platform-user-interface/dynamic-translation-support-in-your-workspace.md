---
title: Dynamic Translation support in your Workspace
description: Dynamic Translation support in Workspace enables on-demand translation of text in comments and work notes, in the Activity stream, and on forms.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working on records in your Workspace, Use, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Dynamic Translation support in your Workspace

Dynamic Translation support in Workspace enables on-demand translation of text in comments and work notes, in the Activity stream, and on forms.

## Configuring Dynamic Translation

To enable and configure Dynamic Translation for Activity stream, do the following.

1.  Activate the Dynamic Translation \(com.glide.dynamic\_translation\) plugin. For more information see [Activate Dynamic Translation](https://www.servicenow.com/docs/access?context=activate-dynamic-translation&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
2.  Configure Dynamic Translation for the translation service provider. For more information, see [Integration with other translation services](https://www.servicenow.com/docs/access?context=integration-with-other-translation-services&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Translation button in the Activity Stream

The **Translate** icon appears in the Activity stream for comments and work notes, next to text that is in a language other than your own.![Translate button in activity stream.](../image/translate-button-in-activity-stream.png).

The translation result displays below the original text. If the translation isn’t configured properly, an error message displays. ![The translation result displays.](../image/tanslate-button-result-in-activity-stream.png)

## Translation button on forms

Dynamic Translation can also be configured for forms in Workspace. ![The translate button appears on the form fields](../image/translate-button-on-forms.png)

To configure Dynamic Translation for form fields, do the following.

1.  Navigate to a record that needs translation enabled.
2.  Right-click a form field that needs translation and select **Configure Dictionary**.
3.  In the **Attributes** related list, select **New**.
4.  On the form, fill in the fields as follows.
    -   In the **Attribute** field, search for **Dynamic Translation Enabled**.
    -   In the **Value** field, enter `true`.
5.  Select **Submit**.

