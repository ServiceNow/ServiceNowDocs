---
title: Card template element attributes
description: Use this reference to determine which attributes to use for your card template elements.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Card actions in Mobile Card Builder, Mobile Card Builder, Mobile app building tools, Building mobile apps, Mobile Platform]
---

# Card template element attributes

Use this reference to determine which attributes to use for your card template elements.

Each card template element has one or more required attributes that you must create. The sections below show the required attributes for each card template element type.

**Note:** When using the Mobile Card Builder, the listed attributes do not need to be manually created, as the tool automatically creates the attributes in the background.

## Attributes for the Text type

|Name|Description|Configuration|
|----|-----------|-------------|
|TextValue|Used to display static text.|Use the **Translatable value** field to enter the text to display.|
|FieldLabel|Used to display the label of a table field.|Use the **Value** field to enter the name of a field. For example, `short_description`.|
|FieldValue|Used to display the value of a field in a record.|Use the **Value** field to enter the name of a field. For example, `short_description`.|
|FieldFunction|Used to display either a count of records, or the value by which records are grouped.| |

## Attributes for the Image type

|Name|Description|Configuration|
|----|-----------|-------------|
|ImageURL|Used to display a static image from the attachment\[sys\_attachment\] table on your instance.|Use the **Value** field to enter a SysID for a record in the attachment\[sys\_attachment\] table.|
|FieldValue|Used to display an image from a field in a record.|Use the **Value** field to enter the name of a field. For example, `avatar`.|

## Attributes for the Button and MenuButton types

|Name|Description|Configuration|
|----|-----------|-------------|
|Button|Used to select the function that runs when users tap a button.|Use the **Value** field to enter the SysID of a function from the Functions\[sys\_sg\_button\] table. For details on creating functions, see [Mobile functions](../concept/sg-studio-mobile-button-types.md).|
|TextValue|Used to display static text.|Use the **Value** field to enter the name of a field. For example, `short_description`.|
|FieldValue|Used to display the value of a field in a record.|Use the **Value** field to enter the name of a field. For example, `avatar`.|
|Icon|Used to display an icon.|Use the **Value** field to enter the SysID of an icon record from the Icon\[sys\_sg\_icon\] table.|

## Attributes for the Menu type

|Name|Description|Configuration|
|----|-----------|-------------|
|TextValue|Used to display static text.|Use the **Value** field to enter the name of a field. For example, `short_description`.|
|Icon|Used to display an icon.|Use the **Value** field to enter the SysID of an icon record from the Icon\[sys\_sg\_icon\] table.|

## Attributes for the HtmlText type

|Name|Description|Configuration|
|----|-----------|-------------|
|SearchExternalSource| | |
|HtmlReplaceMap| | |
|HtmlSanitizationAllowList| | |
|HtmlRemoveList| | |
|StringReplaceMap| | |
|RenderType| | |

## Property Attributes

Use property attributes to define additional properties for your card template slot. These properties are not associated with a specific attribute type.

|Name|Description|Configuration|
|----|-----------|-------------|
|BackgroundColor|Color of the background for the card template element.|Use the **Value** field to define the color. Colors must be in color hex code format, or the name of a color theme. For example `Primary` or `#8a8a8a`.|
|BorderColor|Color of the border for the card template element.|Use the **Value** field to define the color. Colors must be in color hex code format, or the name of a color theme. For example `Primary` or `#8a8a8a`.|
|TextColor|Color of the text or the card template element.|Use the **Value** field to define the color. Colors must be in color hex code format, or the name of a color theme. For example `Primary` or `#8a8a8a`.|

