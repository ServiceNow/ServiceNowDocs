---
title: Configure mobile campaign components
description: Configure components to display the image, video, and text cards in a campaign for your users to view and interact with on mobile devices.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Displaying campaigns, Configuring the Mobile Platform, Mobile Platform]
---

# Configure mobile campaign components

Configure components to display the image, video, and text cards in a campaign for your users to view and interact with on mobile devices.

## Before you begin

To configure components to display a campaign on mobile devices, ensure that you have established the following items:

-   Developed content for your campaign. For more information, see [Campaigns for Content Experiences](https://www.servicenow.com/docs/access?context=ecpro-campaigns&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) and [Configure mobile content](https://www.servicenow.com/docs/access?context=ecpro-content-delivery-mobile&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

-   Defined the appearance criteria for at least one card type. For more information, see [Create appearance templates for cards for a mobile campaign](mobile-campaign-card-type.md) and [Configure the details for the appearance of cards for a mobile campaign](../reference/mobile-campaign-card-config.md).

-   Have the Employee Center Pro Content Publishing plugin \[com.sn\_content\_delivery\] installed. For more information, see [Activate Content Publishing](https://www.servicenow.com/docs/access?context=activate-content-delivery-plugin&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).


Role required: admin

## Procedure

1.  Create a data item to collect the data for the campaign content.

    1.  In the web-based UI, enter `sys_sg_data_item.list` in the filter navigator to open a list of data items.

    2.  Click **New** to create a data item.

    3.  On the form, fill in the fields.

<table id="table_wh2_nk3_fmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A title for the data item. You can have multiple data items with the same name.

</td></tr><tr><td>

Description

</td><td>

Optional additional details.

</td></tr><tr><td>

Condition Type

</td><td>

Select the method to use when building conditions to retrieve data from your data item. The available options are: -   **Declarative**

Create conditions for the data item using the condition builder.

-   **Scripted**

Use a script to determine the conditions of your data item. A text window to enter a script appears below this field when you select this option.

-   **Append Encoded Query**

This condition is only used when creating data items for chart screens. Don't choose this **Condition Type** for campaigns.

</td></tr><tr><td>

Table

</td><td>

`sn_cd_content_mobile`, the Employee Center table, which contains the content of the cards.

</td></tr><tr><td>

Query Condition

</td><td>

Condition that filters content data retrieved from the Employee Center table. For example, if a field called month exists in the table, you could set the condition **\[month\]\[is\]\[September\]** to indicate you want to pull content only when the month equals September.

</td></tr><tr><td>

Group by

</td><td>

Select the field used to group the records in your list.

</td></tr></tbody>
</table>    4.  Click **Submit**.

2.  Create an item configuration for each item view you use.

    1.  In the web-based UI, enter `sys_sg_master_item.list` in the filter navigator.

    2.  Click **New** to create an item configuration.

    3.  On the form, fill in the fields.

<table id="table_wyx_xgz_fmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A title for the list item configuration.**Note:** Include the card type in the name.

</td></tr><tr><td>

Card

</td><td>

The card you want to use for the list item. Search for an existing card or select **New** to configure one.

</td></tr><tr><td>

Table

</td><td>

`sn_cd_content_mobile`, the Employee Center table, which contains the content of the cards.

</td></tr><tr><td>

Condition

</td><td>

Condition that filters display-related data retrieved from the HR Service Content Delivery table. Use a declarative condition to create conditions for the item configuration using the condition builder.

 For example, you could specify to display all image records related to the condition September, which you defined in the data item condition. You then set the condition **\[Content type\]\[is\]\[Image\]** and as a result all images tagged as September are displayed in the mobile campaign.

</td></tr><tr><td>

Embedded screen

</td><td>

Not applicable for mobile campaigns.

</td></tr></tbody>
</table>3.  Create a list stream, which connects the data item with the item configuration.

    1.  In the web-based UI, enter `sys_sg_item_stream.list` in the filter navigator.

    2.  Click **New** to create an list stream.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|A title for the list stream.|
        |Data item|The data item you created.|

    4.  In the List Stream M2M item configuration section, click **Insert a new row**.

    5.  Insert the item configuration you created.

    6.  Click **Save**.

    7.  Click **Submit**.

4.  Create a list stream container.

    1.  In the web-based UI, enter `sys_sg_item_stream_container.list` in the filter navigator.

    2.  Click **New**.

    3.  In the **Name** field, enter a title for the list stream container.

    4.  Right-click on the form header \(![Form header menu button](../image/context-menu-icon.png)\) and select **Save**.

    5.  In the Stream Container M2M streams section, click **New**.

    6.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Stream|The stream that you want to add to the stream container.|
        |Stream container|The stream container that contains the stream.|
        |Order|A number that indicates where to place the stream container. Lower-numbered items display before higher-numbered items.|

    7.  Click **Submit**.

    8.  Click **Update**.

5.  Create a screen launcher content UI section to contain the campaign.

    1.  In the web-based UI, enter `sys_sg_content_section.list` in the filter navigator.

    2.  Click **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Title|Title for the content UI section. This title is not displayed in the mobile UI.|
        |Active|Option for enabling the display of the campaign in your mobile instance.|

    4.  Click **Submit**.


## What to do next

Add the content UI section to a screen launcher. For more information, see [Configure a content UI section](configure-content-ui-section.md).

