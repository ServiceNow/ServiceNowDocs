---
title: Configure favorite content type on Mobile
description: Configure the favorites option on Mobile to help employees personalize the content and easily access the content.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Cross-channel favorites, Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Configure favorite content type on Mobile

Configure the favorites option on Mobile to help employees personalize the content and easily access the content.

## Before you begin

Role required: portal admin and sp\_admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile UI** &gt; **Mobile**.

2.  Edit the mobile UI rules to suit your needs.

    See [Mobile UI Rules](https://www.servicenow.com/docs/access?context=create-mobile-ui-rule&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US) and configure the following field values.

    |Field|Description|
    |-----|-----------|
    |Condition|For the **Condition** field, specify `text_02=sysId`, where sysId indicates the the sys\_id of the new **Favorite Content Type** record. This rule applies only to the favorite items that belong to this content type.|
    |Parent|My favorites \(without image\)|
    |Parent Table|Mobile View|
    |Trigger|OnLoad|

    |Field|Description|
    |-----|-----------|
    |Target|text\_01|
    |Operation|Set UI Style|
    |Value|Example JSON`{ "TextDecorator":{ "Type": "Font", "FontName": "now-mobile-icons", "Value": "f15c", "FontColor": "#333E3F" } }`|

    When the content configuration associated with this content type can have images to render on the favorite card, create another record with the parent value as **My favorites \(with image\)**

3.  Create a function and function instance to suit your needs.

    See [Create a function and function instances](../../../administer/mobile-employee/task/add-quick-action.md#) and configure the following field values.

    |Field|Description|
    |-----|-----------|
    |Table|Favorite \(App Use\) \[sn\_ex\_sp\_st\_favorite\].|
    |Conditions|Add appropriate conditions so that this function only applies on desired content types.|
    |Parent|Set the table name to **sys\_sg\_master\_item** and document to My favorites \(without image\).|


## Result

The content type display is configured for Mobile.

**Related topics**  


[Now Mobile app](../../../administer/mobile-employee/concept/mobile-employee-experience.md)

[Mobile plugins](https://www.servicenow.com/docs/access?context=sg-mobile-plugins&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)

