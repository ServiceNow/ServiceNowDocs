---
title: Virtual Agent Designer integration with Localization Framework
description: The integration of Virtual Agent Designer with Localization Framework enables you to translate Virtual Agent topics using the translation modes supported by Localization Framework with or without a localization task.
locale: en-US
release: zurich
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer]
---

# Virtual Agent Designer integration with Localization Framework

The integration of Virtual Agent Designer with Localization Framework enables you to translate Virtual Agent topics using the translation modes supported by Localization Framework with or without a localization task.

## Localizing Virtual Agent topics

The integration of Virtual Agent Designer with Localization Framework enables you to do the following tasks.

-   Select multiple languages from the available languages in the instance to configure settings with the Virtual Agent artifact. To configure localization settings, see [Localization Framework settings](localization-settings.md).
-   Translate the content directly from the Virtual Agent Designer using the edit option.
-   Read, edit, machine translate, export, and import the content of the Virtual Agent topic from the Virtual Agent Designer if the Virtual Agent artifact is configured in the localization settings.

    **Note:**

    -   **Note:** You need the localization\_editor role to edit the translated content from the comparison UI of the Virtual Agent Designer directly. For more information about the localization\_editor role, see [Localization Framework Roles](../reference/roles-localization-framework.md#).

    -   Activate the Dynamic Translation plugin \(com.glide.dynamic\_translation\) to use machine translation in Localization Framework.
-   Request translations from Virtual Agent Designer.

    **Note:** Requesting translations creates localization tasks. You need the localization\_requester role to request translations.

-   Approve and publish the translated content.
-   Monitor the overall localization health of the Virtual Agent topics from the [Localization Insights dashboard](../../../use/dashboards/application-content-packs/localization-insights-dashboard.md).

For more information about localizing the Virtual Agent topics in the Virtual Agent Designer, see [Virtual Agent Localization](https://www.servicenow.com/docs/access?context=localize-va-topic&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

**Parent Topic:**[Explore Localization Framework](exploring-localization-framework.md)

