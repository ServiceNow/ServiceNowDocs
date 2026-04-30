---
title: List of Search Result EVAM card properties
description: You can customize the appearance of standard search results in your AI Search application by changing these properties in the application's Search Result EVAM \(Entity View Action Mapping\) cards.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Configure EVAM display settings for search results, Configure, AI Search, Search administration, Configure core features, Administer]
---

# List of Search Result EVAM card properties

You can customize the appearance of standard search results in your AI Search application by changing these properties in the application's Search Result EVAM \(Entity View Action Mapping\) cards.

To learn about configuring properties for Search Result EVAM cards, see [Configure EVAM display settings for search results in AI Search applications](../task/configure-search-result-card-opts.md).

**Note:** The following properties are only supported for EVAM cards with `component` property value `sn-search-result-evam-card`. Don't set these properties for EVAM cards with any other `component` value.

<table id="table_jkl_xcq_qdc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

avatarURL

</td><td>

Defines the URL for the image you want to show on the Search Result card when **imageType** is set to **avatar**. -   Type: string
-   Default value: \(no value\)

**Note:** To specify literal text for this property, include the property in the `staticValues` object and specify the text as its `key` value. To populate this property with the current search result's value from an AI Search indexed field, include the property in the `mappings` object with the field name as its value. For a list of AI Search indexed field names, see [AI Search index fields](index-fields-list-ais.md).

</td></tr><tr><td>

customIcon

</td><td>

Specifies the name of an image from the Images \[db\_image\] table that you want to show as a custom icon for the Search Result card. If specified, this property overrides the icon setting from the **icon** property.**Note:** This property only has an effect if **imageType** is set to **icon**. If **imageType** is set to any other value, the **customIcon** setting is ignored.

 Custom icon images should be either 24 × 24 pixels or 32 × 32 pixels in size.

 -   Type: string
-   Default value: \(no value\)

</td></tr><tr><td>

customIconSize

</td><td>

Specifies the size of the image specified as the **customIcon** property. The specified size should match the size of the custom icon image in the Images \[db\_image\] table. -   Type: string
-   Default value: 24px
-   Supported values:
    -   **24px**: Render the custom icon image as 24 × 24 pixels in size.
    -   **32px**: Render the custom icon image as 32 × 32 pixels in size.

</td></tr><tr><td>

detailLabelOne, detailLabelTwo, detailLabelThree, detailLabelFour, detailLabelFive, detailLabelSix, detailLabelSeven, detailLabelEight, detailLabelNine, and detailLabelTen

</td><td>

Defines label content for the Search Result card's detail label-value pairs. You can show up to 10 label-value pairs on the Search Result card. -   Type: string
-   Default value: \(no value\)

**Note:** To specify literal text for one of these properties, include the property in the `staticValues` object and specify the text as its `key` value. To populate one of these properties with the current search result's value from an AI Search indexed field, include the property in the `mappings` object with the field name as its value. For a list of AI Search indexed field names, see [AI Search index fields](index-fields-list-ais.md).

 To define value content for these label-value pairs, see **detailValueOne** through **detailValueTen**. **detailValueOne** sets the value for **detailLabelOne**, **detailValueTwo** sets the value for **detailLabelTwo**, and so on up through **detailValueTen** and **detailLabelTen**

 For additional configuration of how a search result's details are shown on the Search Results card, see **detailLabelType**, **detailLabelSeparator**, and **detailPosition**.

</td></tr><tr><td>

detailLabelSeparator

</td><td>

Defines the character used to separate inline label-value pairs. Only applies when **detailLabelType** is set to **inline**. -   Type: string
-   Default value: \(no value\)

**Note:** To specify literal text for this property, include the property in the `staticValues` object and specify the text as its `key` value. To populate this property with the current search result's value from an AI Search indexed field, include the property in the `mappings` object with the field name as its value. For a list of AI Search indexed field names, see [AI Search index fields](index-fields-list-ais.md).

</td></tr><tr><td>

detailLabelType

</td><td>

Defines how to render label-value pairs on the Search Result card. -   Type: choice list
-   Default value: inline
-   Supported values:
    -   **inline**: Render label-value pairs using the [Label-value](https://developer.servicenow.com/dev.do#!/reference/next-experience/paris/now-components/now-label-value-inline/overview) component, with each label appearing on the same line as its value string.
    -   **stacked**: Render label-value pairs using the [Label value stacked](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/now-components/now-label-value-stacked/overview) component, with each label appearing on a separate line from its value string.

</td></tr><tr><td>

detailPosition

</td><td>

Defines where search result detail label-value pairs are shown relative to the Search Result card's summary field.-   Type: choice list
-   Default value: below
-   Supported values:
    -   **above**: Search result details are shown above the summary field.
    -   **below**: Search result details are shown below the summary field.

</td></tr><tr><td>

detailValueOne, detailValueTwo, detailValueThree, detailValueFour, detailValueFive, detailValueSix, detailValueSeven, detailValueEight, detailValueNine, and detailValueTen

</td><td>

Defines value content for the Search Result card's detail label-value pairs. You can show up to 10 label-value pairs on the Search Result card. -   Type: string
-   Default value: \(no value\)

**Note:** To specify literal text for one of these properties, include the property in the `staticValues` object and specify the text as its `key` value. To populate one of these properties with the current search result's value from an AI Search indexed field, include the property in the `mappings` object with the field name as its value. For a list of AI Search indexed field names, see [AI Search index fields](index-fields-list-ais.md).

 To define label content for these label-value pairs, see **detailLabelOne** through **detailLabelTen**. **detailLabelOne** sets the label for **detailValueOne**, **detailLabelTwo** sets the label for **detailValueTwo**, and so on up through **detailLabelTen** and **detailValueTen**

 For additional configuration of how a search result's details are shown on the Search Results card, see **detailLabelType**, **detailLabelSeparator**, and **detailPosition**.

</td></tr><tr><td>

forceNewTab

</td><td>

Defines whether you want the search result to open in a new browser tab or the current browser tab when you select the link in the Search Result card. -   Type: true \| false
-   Default value: true
-   Supported values:
    -   **false**: Open the search result in the current browser tab when you select the link in the Search Result card.
    -   **true**: Open the search result in a new browser tab when you select the link in the Search Result card.

</td></tr><tr><td>

hideIcon

</td><td>

Defines whether you want to show or hide the icon on the Search Result card. -   Type: true \| false
-   Default value: false
-   Supported values:
    -   **false**: Show the configured icon on the Search Result card.
    -   **true**: Do not show an icon on the Search Result card.

</td></tr><tr><td>

icon

</td><td>

Defines the icon you want to show on the Search Result card when **imageType** is set to **icon**. This icon is also shown as a fallback when **imageType** is set to **image** but no **imageURL** value is provided. -   Type: string
-   Default value: \(no value\)

**Note:** To specify literal text for this property, include the property in the `staticValues` object and specify the text as its `key` value. To populate this property with the current search result's value from an AI Search indexed field, include the property in the `mappings` object with the field name as its value. For a list of AI Search indexed field names, see [AI Search index fields](index-fields-list-ais.md).

 For the set of available icon names, see the [Icon Gallery](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/now-components/now-icon/gallery) in the Next Experience reference section on the ServiceNow® Developer Site.

</td></tr><tr><td>

iconSize

</td><td>

Defines the size of the icon or avatar image shown on the Search Result card. -   Type: choice list
-   Default value: xl \(if **imageType** is set to **icon**\) or md \(if **imageType** is set to **avatar**\)
-   Supported values:
    -   **sm**: Show a small icon or avatar image on the Search Result card.
    -   **md**: Show a medium-sized icon or avatar image on the Search Result card.
    -   **lg**: Show a large icon or avatar image on the Search Result card.
    -   **xl**: Show an extra-large icon or avatar image on the Search Result card.

</td></tr><tr><td>

imageType

</td><td>

Defines the type of marker you want to show on the Search Result card. Supported values:

-   avatar
-   icon
-   image

</td></tr><tr><td>

imageURL

</td><td>

Defines the URL for the image you want to show on the Search Result card when **imageType** is set to **image**. -   Type: string
-   Default value: \(no value\)

**Note:** To specify literal text for this property, include the property in the `staticValues` object and specify the text as its `key` value. To populate this property with the current search result's value from an AI Search indexed field, include the property in the `mappings` object with the field name as its value. For a list of AI Search indexed field names, see [AI Search index fields](index-fields-list-ais.md).

</td></tr><tr><td>

summary

</td><td>

Defines the content of the Search Result card's summary field. -   Type: string
-   Default value: \(no value\)

**Note:** To specify literal text for this property, include the property in the `staticValues` object and specify the text as its `key` value. To populate this property with the current search result's value from an AI Search indexed field, include the property in the `mappings` object with the field name as its value. For a list of AI Search indexed field names, see [AI Search index fields](index-fields-list-ais.md).

</td></tr><tr><td>

summaryFontSize

</td><td>

Defines the font size for the Search Result card's summary field. -   Type: choice list
-   Default value: sm
-   Supported values:
    -   **sm**: Show the Search Result card's summary field in small font size.
    -   **md**: Show the Search Result card's summary field in medium font size.
    -   **lg**: Show the Search Result card's summary field in large font size.
    -   **xl**: Show the Search Result card's title summary in extra-large font size.

</td></tr><tr><td>

textHeaderLabelOne, textHeaderLabelTwo, and textHeaderLabelThree

</td><td>

Defines the content of the Search Result card's text header labels. If you specify multiple text header labels, they appear separated by a pipe `|` character. -   Type: string
-   Default value: \(no value\)

**Note:** To specify literal text for one of these properties, include the property in the `staticValues` object and specify the text as its `key` value. To populate one of these properties with the current search result's value from an AI Search indexed field, include the property in the `mappings` object with the field name as its value. For a list of AI Search indexed field names, see [AI Search index fields](index-fields-list-ais.md).

</td></tr><tr><td>

titleFontSize

</td><td>

Defines the font size for the Search Result card's title field. -   Type: choice list
-   Default value: lg
-   Supported values:
    -   **sm**: Show the Search Result card's title field in small font size.
    -   **md**: Show the Search Result card's title field in medium font size.
    -   **lg**: Show the Search Result card's title field in large font size.
    -   **xl**: Show the Search Result card's title field in extra-large font size.

</td></tr><tr><td>

titleLabel

</td><td>

Defines the content of the Search Result card's title field. -   Type: string
-   Default value: \(no value\)

**Note:** To specify literal text for this property, include the property in the `staticValues` object and specify the text as its `key` value. To populate this property with the current search result's value from an AI Search indexed field, include the property in the `mappings` object with the field name as its value. For a list of AI Search indexed field names, see [AI Search index fields](index-fields-list-ais.md).

</td></tr><tr><td>

useAttachmentViewer

</td><td>

Option to use Document Viewer to display grouped attachments shown on the Search Result card in collapsed format. To learn more about Document Viewer, see [Enable Document Viewer](https://www.servicenow.com/docs/access?context=enable-document-viewer&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US). For more information on grouped attachments and how they're shown on the Search Result card, see [Group attachment search results with their parent results](../task/group-attachment-srch-results-ais.md).

 -   Type: true \| false
-   Default value: false
-   Supported values:
    -   **true**: Use Document Viewer to display attachments selected from the Search Result card.

**Note:** If Document Viewer is not active on your instance, or not enabled for the search result's source table, selecting an attachment from the Search Result card shows a message indicating that the attachment can't be viewed.

    -   **false**: Download attachments selected from the Search Result card.

</td></tr></tbody>
</table>**Parent Topic:**[Configure EVAM display settings for search results in AI Search applications](../task/configure-search-result-card-opts.md)

