---
title: Setup the theme for Business and Consumer Portals
description: Customize the theme of the Business and Consumer Portals to add font and theme style sheets.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup Business and Consumer Portal, Business and Consumer Portal, Set up self-service, Configure, Customer Service Management]
---

# Setup the theme for Business and Consumer Portals

Customize the theme of the Business and Consumer Portals to add font and theme style sheets.

## Before you begin

Role required: sp\_admin

## About this task

The default theme for the Business and Consumer Portals is the Coral Theme. You can use your own theme according to your branding.

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

    **Note:** Convert any font or theme size from rems to pixel in the CSS with a conversion factor of 10. For example, 10 rems should be changed to 100 pixel.

5.  Select **Update**.


