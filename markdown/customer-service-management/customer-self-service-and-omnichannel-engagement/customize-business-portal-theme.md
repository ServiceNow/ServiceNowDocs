---
title: Setup the theme for Business Portal
description: Customize the theme of the business portal to add font and theme style sheets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/customer-self-service-and-omnichannel-engagement/customize-business-portal-theme.html
release: zurich
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setup the Business Portal, Configure Business Portal, Set up self-service, Configure, Customer Service Management]
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

        \[Omitted image "edit\_css\_include\_list.png"\] Alt text: Edit css includes

        -   portal-polaris-set-base-font
        -   portal-polaris-rem-px-theme
        -   portal-polaris-kb-rem-px-theme
    4.  Select **Save**.

4.  Hover over the style sheet and select the preview icon \(\[Omitted image "preview-record.png"\] Alt text: Preview icon\) then select **Open Record** to set the order of added style sheets.

    1.  Set the order of portal-polaris-set-base-font as the lowest.

    2.  Set the order of portal-polaris-rem-px-theme as second highest.

    3.  Set the order of portal-polaris-kb-rem-px-theme as the highest.

    **Note:** Convert any font or theme size from rems to pixel in the CSS with a conversion factor of 10. For example, 10 rems should be changed to 100 pixel.

5.  Select **Update**.


