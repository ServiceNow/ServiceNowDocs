---
title: Edit view config form
description: The Edit view config form contains information about EVAM view configurations defined for search application configurations in AI Search. Use this form when creating or modifying a view configuration.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [AI Search Admin console reference, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Edit view config form

The Edit view config form contains information about EVAM view configurations defined for search application configurations in AI Search. Use this form when creating or modifying a view configuration.

For details on creating or modifying a view configuration, see [Create or edit an EVAM view definition](../task/ais-admin-console-evam-configurations.md).

## Edit view config form

|Field|Description|
|-----|-----------|
|Name|Unique name for the EVAM view configuration.|
|Order|Order of appearance for a view configuration in the context of the search application configuration.|
|Table|Table to associate with the EVAM view configuration.|
|Condition|Conditions for when to use the EVAM view configuration.|
|View Template|Template to associate with the EVAM view configuration.|

<table id="table_h21_jhv_ddc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Component

</td><td>

Name of the component to be added to the EVAM view configuration.

</td></tr><tr><td>

Title label

</td><td>

Title of the EVAM view result card.

</td></tr><tr><td>

Type

</td><td>

Determines how title is handled within the EVAM view, select either Model Field or Static Value.-   **Static Value**

A fixed or constant value that you manually enter.

-   **Table Field**

Dynamically generated value based on a specific columns from the selected table.

-   **Custom Field**

Specific information that is returned as part of the search results. By default, there are four custom fields available:

    -   ai\_search\_teaser\_title
    -   ai\_search\_teaser\_text
    -   document\_index
    -   navigation\_url

**Note:** This field appears multiple times throughout the form. Choose its value according to the configuration of the preceding field.

</td></tr><tr><td>

Title font size

</td><td>

The font size for the title text in an EVAM view to control the visual appearance of the title.

</td></tr><tr><td>

Translatable

</td><td>

Option to translate the text based on the preferred language of a user​.**Note:** This field appears multiple times throughout the form.

</td></tr><tr><td>

Summary

</td><td>

Additional information to display in the result card after the title.

</td></tr><tr><td>

Summary font size

</td><td>

The font size for the text in an EVAM view result card to control the visual appearance of the information.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Text header label one|Unique title one for a specific EVAM view that communicates the purpose or content of the view.|
|Text header label two|Unique title two for a specific EVAM view that communicates the purpose or content of the view.|
|Text header label three|Unique title three for a specific EVAM view that communicates the purpose or content of the view.|

|Field|Description|
|-----|-----------|
|Image type|Determine the format or type of an image you want to display, such as icon, image, or avatar.|
|Image URL|Determine the web address \(URL\) of an image that you want to display within a particular component or element of your application.|
|Avatar URL|Determine the web address \(URL\) of an avatar image. Avatars are typically used to represent users, characters, or entities within an application.|
|Avatar name|Name given to the avatar.|
|Icon|Represents a visual symbol that displays in the EVAM view result card interface. /The icon to display next to the breakdown-related field on the form.|
|Icon size|Determines the size of the icon|
|Hide icon|An option to hide icon in the EVAM view result card interface.|

|Field|Description|
|-----|-----------|
|Aria label|An attribute that enhances web accessibility by supplying titles for screen readers.|
|Detail label type|Specifies how the details are displayed on the EVAM view result card, either inline or stacked.|
|Detail position|Specifies where the details are displayed on the EVAM view result card, either above the summary text or below.|
|Detail label separator|Specifies the character or string used to separate labels on the EVAM view result card.|
|Detail label|Describes each detail displayed on the EVAM view result card.|
|Detail value|Specifies the information that is displayed for each detail on the EVAM view result card.|
|Open in new tab|An option to display and enable the Open in New Tab icon on the EVAM view result card.|
|Is global|Indicates whether the view configuration is for a portal.|

