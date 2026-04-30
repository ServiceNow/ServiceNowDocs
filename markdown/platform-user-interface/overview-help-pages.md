---
title: Overview help pages
description: The overview help feature included with the base system displays slides with introductory information on new features offered in the ServiceNow platform. An administrator can hide the option from the help menu.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Overview help pages

The overview help feature included with the base system displays slides with introductory information on new features offered in the ServiceNow® platform. An administrator can hide the option from the help menu.

To learn about the latest features in your version, click the **What's New** link in the Core UI help sidebar.

![Overview help link](../image/WhatsNewLink.png "Overview help link")

The Overview Help Page \[sys\_ui\_overview\_help\] table contains the records for each panel that appears, including images, icons, descriptions, and condition statements that control display. By default, the instance displays panels describing notable features of the current release, but users can modify this page to display panels for customized features in their own instance and then define who can see these panels.

Users scroll through the panels by clicking the buttons provided or by clicking the directional arrows at the bottom of the page, depending on how the page was configured.

**Note:** Administrators can edit the default help page to modify, add, or delete existing panels from this page to match the features in your system.



## Hide the What's New option

Administrators can hide the What's New option using a system property.

To find the property, type `sys_properties.list` in the application navigator. Find the **glide.product.show\_what\_is\_new** property and change the value to **false**.

![Help panel open with the What's New option hidden](../image/WhatsNewHidden.png "What's New option hidden")

-   **[Create custom overview help](../task/create-custom-overview-help-pages.md)**  
You can edit existing overview help pages to display your own custom panels to selected users.
-   **[Example of adding a panel to an existing overview help page](../task/example-add-slide-to-existing-page.md)**  
This example adds panels to the existing overview help page that display only for users with specific roles and when a specific plugin is activated.

**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)

