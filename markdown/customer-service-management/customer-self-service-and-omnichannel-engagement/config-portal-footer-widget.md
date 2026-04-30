---
title: Configure the Portal Polaris Footer widget
description: Configure the Portal Polaris Footer widget to display your company’s corporate office address, email address, and more on the portal page.
locale: en-US
release: zurich
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Portal Polaris Footer widget, Set up Configurable Portal widgets, Set up self-service, Configure, Customer Service Management]
---

# Configure the Portal Polaris Footer widget

Configure the Portal Polaris Footer widget to display your company’s corporate office address, email address, and more on the portal page.

## Before you begin

The Portal Next Experience theme application should have been activated.

Role required: sp\_admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

2.  On the Service Portal page, in the **Title** column, enter `*customer support`.

3.  Select **Customer Support**.

4.  On the Customer Support form, in the **Quick start config** field, paste the following JSON code and update it.

    ```
     
     [{
      
    "footer": { 
           "org_info": [ 
              "<line #1>", 
              "<line #2>", 
              "<line #3>" 
           ], 
           "copyright": "<copyright text>", 
           "logo_img_name": "<image name from db_image table>", 
           "sitemap_links_menu_sys_id": "<enter the sys_id>", 
           "footer_links_menu_sys_id": "<enter the sys_id>", 
           "social_links_menu_sys_id": "<enter the sys_id>" 
         }
    }]
    ```

    For more information about the parameters, see [Portal Footer widget JSON parameters](../reference/portal-footer-widget-json.md).

5.  Select a theme for your portal.

    Note that the predefined La Jolla theme, used as an example, is active by default.

    1.  In the Theme field, select the Lookup using list icon \(![Lookup using list icon](../image/lookup-list.jpg)\)

    2.  On the Themes page, in the **Name** column, search for and select the `La Jolla` theme.

    The La Jolla theme is set as your portal theme.

6.  Select the Portal Footer as the footer for your portal theme.

    1.  In the **Theme** field, select the Preview this record icon \(![Preview this record icon.](../image/preview-record-icon.jpg)\).

    2.  On the Theme form, select **Open Record**.

    3.  On the La Jolla form, in the **Footer** field, select the Lookup using list icon \(![Lookup using list icon](../image/lookup-list.jpg)\).

    4.  On the Header \| Footers window, in the **Name** column, search for and select `Portal Footer`.

    5.  Select **Update**.


## What to do next

Configure links to appear in the Portal Footer widget:

-   To add pages or sections of your website in a sitemap, see [Configure sitemap links for the Portal Polaris Footer widget](portal-footer-widget-conf-sitemap-links.md)
-   To add the social media accounts of your organization, see [Configure social media links in the Portal Polaris Footer widget](portal-footer-widget-social-links.md)
-   To include a link to a site on a portal page, see [Add related links in the Portal Polaris Footer widget](portal-footer-widget-conf-footer-links.md).

