---
title: Configure Employee Center Pro Kiosk
description: Configure and use the default Kiosk for better deskless experience.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Employee Center Pro Kiosk, Employee Center Integrations, Unified Employee Experience, Employee Service Management]
---

# Configure Employee Center Pro Kiosk

Configure and use the default Kiosk for better deskless experience.

## Before you begin

Role required: sn\_hr\_sp.esc\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Portals** &gt; **Portals** &gt; **Employee Center Pro Kiosk**.

2.  Edit the portal to suit your needs.

    For more information on the portal form fields and description, see [Create a portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/create-a-portal.md).

3.  Navigate to **All** &gt; **Service Portal** &gt; **Themes**.

    1.  Search and select `Employee Center Pro Kiosk Coral Theme` to use the default theme.

        **Note:** Use the default theme for better visual and usability experience. However, you can customize the theme to suit your needs.

    2.  Click **Update**.

4.  Navigate to **All** &gt; **Service Portal** &gt; **Headers &amp; Footers** to check and use the following default header configuration.

    -   Header: `eck_header`
    -   Header name: `Employee Center Pro Kiosk Header`
5.  Navigate to **All** &gt; **Employee Center** &gt; **Employee Center footer** to check and use the following default footer configuration:

    -   Footer: `employee-center-footer`
    -   Footer name: Employee Center Footer
6.  On the theme page, Edit **CSS variables** information to customize other settings such as primary and background colors.

    For more information on the theme fields and description, see [Create a portal theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/c_CustomCSS.md).

7.  Verify and use the following default configuration:

    -   Theme: `Employee Center Pro Kiosk Coral Theme`
    -   Main menu: `EC Pro Kiosk Menu`
    -   Homepage: `eck_home`
    -   Login page: `eck_login_page`
    -   Topic template: `eck_taxonomy_topic`
8.  Mark the **Enable AI Search** option to **Active** to use AI search.

    **Note:** For Employee Center Pro Kiosk, the default option is active.

9.  Enable Favorites
10. Navigate to **All** &gt; **Service Portal** &gt; **Portals**, and mark the **Enable favorites** option to **true** to enable My favorites.

    **Note:** By default, the favorites are disabled on the header. You can enable the favorites with the following steps:

    1.  On the portal page, next to the **Main menu** field, click preview this record, and open the **EC Pro Kiosk Menu** record.

    2.  Edit the **Additional options, JSON format** field.

        ```
        "enable_requests":{ "displayValue":"true", "value":true
        "enable_favorites":{ "displayValue":"true", "value":true
        ```

    The **My Favorites** option appears on the header.

11. Select **Support right-to-left languages** for supporting the right-to-left language display on the UI.

12. Click **Update**.

13. Navigate to **All** &gt; **Service Portal** &gt; **Portals** &gt; **Employee Center Pro Kiosk**, click **Try it** to preview the kiosk.


## Result

Your employees can now use the configured Kiosk portal. Kiosk app displays the portal, theme, header, footer, and others based on your configuration.

-   **[Schedule in Employee Center Pro Kiosk](../concept/shift-time-kiosk-ec.md)**  
The schedule details in Employee Center Pro Kiosk is a one-stop destination to check the shift scheduling details for the deskless workers.
-   **[Time off balances in Employee Center Pro Kiosk](../concept/kiosk-timeoff-ec.md)**  
The time off balances details in the Employee Center Pro Kiosk is the source of truth for the time off or leave details of the deskless workers.

**Parent Topic:**[Employee Center Pro Kiosk](../concept/deskless-kiosk-overview.md)

