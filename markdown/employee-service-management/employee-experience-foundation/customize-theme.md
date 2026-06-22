---
title: Customize Employee Center portal theme
description: A theme is a collection of one or more style sheets \(CSS files\) that define a consistent look for a set of pages. Customize the default portal theme to apply your own theme to suit your branding and improve the visual design of the portal pages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/employee-experience-foundation/customize-theme.html
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Portal configuration, Configure your Employee Center portal, Configure, Employee Center, Employee Service Management]
---

# Customize Employee Center portal theme

A theme is a collection of one or more style sheets \(CSS files\) that define a consistent look for a set of pages. Customize the default portal theme to apply your own theme to suit your branding and improve the visual design of the portal pages.

## Before you begin

Role required: admin

## About this task

Employee Center application ships a default **EC theme** that has the best visual design experience. The EC theme provides a consistent experience across all portal pages.

\[Omitted image "ec-theme.jpg"\] Alt text: Portal pages with EC theme applied

## Procedure

1.  Navigate to **Service Portal** &gt; **Themes**.

2.  Search for `EC Theme` to use the default theme.

    **Note:**

    -   Use the default theme for better visual and usability experience. However, you can select other themes to suit your needs.
    -   Remove the customized portal theme before an upgrade to see any default theme that might be released with a future version of Employee Center.
3.  Customize the theme content to suit your requirement.

    1.  Navigate to **Service Portal** &gt; **Themes**.

    2.  Select **EC Theme** to open the page.

    3.  Edit the **CSS variables** field to customize the text and the background colors of your portal.

        For a description of the field values to create a portal theme, see [Create a portal theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-user-interface/service-portal/c_CustomCSS.md).

4.  Navigate to **Service Portal** &gt; **Portals** &gt; **Employee Center**, click **Try it** to preview Employee Center.

5.  Select **Update**.


**Parent Topic:**[Portal configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/employee-experience-foundation/portal-config.md)

**Related topics**  


[Configure portal branding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-user-interface/service-portal/c_BrandingEditor.md)

