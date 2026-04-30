---
title: Suggestion Reader Group form
description: The Suggestion Reader Group form contains information about auto-complete suggestion types defined for AI Search. Use this form when modifying settings for auto-complete suggestion types in AI Search applications.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Suggestion Reader Group form

The Suggestion Reader Group form contains information about auto-complete suggestion types defined for AI Search. Use this form when modifying settings for auto-complete suggestion types in AI Search applications.

For details on configuring auto-complete suggestions in AI Search applications, see [Auto-complete suggestions in AI Search applications](../concept/auto-complete-ais.md#).

<table id="table_ahj_2jm_4nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Suggestion Type

</td><td>

Application-specific name for the auto-complete suggestion type. This field is automatically set.

</td></tr><tr><td>

Section Header

</td><td>

Header displayed in the application search field for auto-complete suggestions of this type.

</td></tr><tr><td>

Application

</td><td>

Application scope for the auto-complete suggestion type. This field is automatically set.

</td></tr><tr><td>

Order

</td><td>

Order of appearance in the application search field for the section containing auto-complete suggestions of this type. The system uses this field to determine display order when a search application configuration includes multiple suggestion types with the same **Click-in Mode** setting.

</td></tr><tr><td>

Suggestion Limit

</td><td>

Maximum number of auto-complete suggestions of this type that the application should display in the search field.

</td></tr><tr><td>

Click-in Mode

</td><td>

Option to control the display of the section containing auto-complete suggestions of this type.-   If selected, auto-complete suggestions of this type are displayed when the user first selects the empty application search field.
-   If deselected, auto-complete suggestions of this type are displayed as the user enters search query terms into the application search field.

 **Note:** A search application configuration can't link to multiple search suggestion types that include the same reader and have the same click-in mode. If you try to link a second suggestion type with the same reader and click-in mode to a search application configuration, the system displays an error message.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

