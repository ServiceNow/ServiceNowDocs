---
title: Portal configuration
description: Configure the default Employee Center portal to incorporate specific widget experiences into your home page.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure your Employee Center portal, Configure, Employee Center, Employee Service Management]
---

# Portal configuration

Configure the default Employee Center portal to incorporate specific widget experiences into your home page.

## Before you begin

Role required: admin

## About this task

Employee Center application provides best in class portal home pages with all the relevant widgets that provide an employee-centric portal experience. The application has two default home pages.

-   Employee Center: ec\_home.
-   Employee Center Pro: ec\_pro\_home.

**Note:** Employee Center Pro portal home page is made available only when you install the Employee Center Pro \(com.snc.employee\_center\_pro\) application from the ServiceNow Store and is licensed separately.

To use the latest out-of-the-box homepage:

-   For upgrade customers, the default homepage associated with the Employee Center portal record remains the same as before the upgrade.​ Edit the portal homepage record manually for using the new portal homepage.
-   New EC and EC Pro customers see the new homepages associated with the portal by default.

**Note:** New home page is not displayed when you have a customized home page.

Modify the default Employee Center or Employee Center Pro portal pages to suit your needs.

For standard sizes of the images and icons, see [Standard banner and icon sizes](../reference/ec-portal-images-size.md) for optimal portal performance.

## Procedure

1.  Navigate to one of the following portals.

    1.  For Employee Center, navigate to **All** &gt; **Employee Center** &gt; **Administration** &gt; **Portal configuration**

    2.  For Employee Center Pro Kiosk, navigate to **All** &gt; **Service Portals** &gt; **Portals** &gt; **Employee Center Pro Kiosk**.

2.  Edit the portal to suit your needs.

    For more information on the portal form fields and description, see [Create a portal](https://www.servicenow.com/docs/access?context=create-a-portal&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

3.  Map the **Taxonomy** that you created or use the default taxonomy.

    For more information on taxonomy, see [Unified Taxonomy for Employee Center](../concept/config-taxonomy.md).


-   **[Customize Employee Center portal theme](customize-theme.md)**  
A theme is a collection of one or more style sheets \(CSS files\) that define a consistent look for a set of pages. Customize the default portal theme to apply your own theme to suit your branding and improve the visual design of the portal pages.
-   **[Enable support for right-to-left languages](../concept/ec-direction-right-to-left-languages.md)**  
When the session language is a right-to-left language, the direction of the portal user interface is mirrored to display from right to left.
-   **[Update the Employee Center home page theme](config-ec-home-theme.md)**  
Enable the gradient background theme along with other UI changes on the Employee Center home page as an existing customer.
-   **[Update the Employee Center Pro home page theme](config-ec-pro-home-theme.md)**  
Enable the gradient background theme along with other UI changes on the Employee Center Pro home page as an existing customer.

**Parent Topic:**[Configure your Employee Center portal](../concept/configure-ec-portal.md)

**Related topics**  


[Customize the Employee Center with widgets](../concept/emp-center-topic-inst-options.md)

[Employee live chat overview](../concept/employee-center-chat-configuration.md)

[Footer configuration](../concept/emp-center-footer-config.md)

