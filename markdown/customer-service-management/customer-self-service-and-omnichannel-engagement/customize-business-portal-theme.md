---
title: Setup the theme for Business Portal
description: Customize the theme of the business portal to add font and theme style sheets.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setup the Business Portal, Configure Business Portal, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Setup the theme for Business Portal

Customize the theme of the business portal to add font and theme style sheets.

## Before you begin

Role required: admin

## About this task

The default theme for the business portal is the Coral Theme. You can use your own theme according to your branding.

You must customize your theme to add font or theme size-related style sheets.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Themes**.

2.  Search and select the required theme.

3.  Add font and theme style sheets.

    1.  On the theme record, select the **CSS Includes** in the related list.

    2.  Select **Edit**.

    3.  Add the following style sheets from the Collection list to the CSS Includes list:

        ![Edit css includes](../image/edit_css_include_list.png "Edit CSS includes list")

        -   portal-polaris-set-base-font
        -   portal-polaris-rem-px-theme
        -   portal-polaris-kb-rem-px-theme
    4.  Select **Save**.

4.  Hover over the style sheet and select the preview icon \(![Preview icon](../image/preview-record.png)\) then select **Open Record** to set the order of added style sheets.

    1.  Set the order of portal-polaris-set-base-font as the lowest.

    2.  Set the order of portal-polaris-rem-px-theme as second highest.

    3.  Set the order of portal-polaris-kb-rem-px-theme as the highest.

    **Note:** Convert any font or theme size from REMs to pixels in the CSS with a conversion factor of 10. For example, 10 REMs should be changed to 100 pixels.

5.  Select **Update**.


