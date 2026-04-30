---
title: EC Information architecture
description: You can now use the out-of-the-box enhanced information architecture for improving content discovery and visibility.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Advanced Portal Navigation, Setup browse experience features, Configure, Employee Center, Employee Service Management]
---

# EC Information architecture

You can now use the out-of-the-box enhanced information architecture for improving content discovery and visibility.

Using the advanced portal navigation, you can design the primary navigation menu and configure the navigation setup based on employee needs and content priorities. Organize your content into menus or modal windows.

![Standard and expanded layouts](../images/ec-ic-architecture-megamenu.png "Out-of-the-box mega menu architecture options")

This image is for illustration purpose only for the out-of-the-box \(OOTB\) mega menu.

-   OOTB EC Pro mega menu layout is expanded.
-   OOTB EC mega menu layout is standard.

    **Note:** You can use a layout of your choice and configure more levels in your taxonomy based on business needs.


## Useful tips and information

Use some of the following guidance and tips.

-   For **Standard view**, you can have a maximum of three levels.
-   For **Expanded view**, you can have a maximum of four levels \(one menu item in the hierarchy and topics up to three levels\). In this example, `Help center > Technology Resources > Hardware > Computers`, you have
    -   One navigation menu item `Help center` and
    -   Three levels of topics `Technology Resources > Hardware > Computers`
-   Add topics up to three levels from the root-level. For example, when you add topics under Human Resources, you can only traverse from `Human Resources > Subtopic 1 > Subtopics 2`.
-   Topics from one hierarchy cannot be mixed with topics of another hierarchy. For example,
    -   For `Human Resources > Pay and Time > Compensation`, you cannot add Hardware as a child of HR.
    -   For `Technology Resources > Hardware > Computers`, you cannot add Pay and Time as a child of Technology Resources or Hardware or Computers.
    -   Pay and Time can be a sibling of Technology Resources or Hardware or Computers.
-   Level 3 in the expanded view and level 2 in the standard view are dynamically adjusted as per available space.
-   For the root item without any child items or any active associated quick link, the Browse button is not displayed.
-   The browse button is displayed in the hamburger view for topics and the browse button is not displayed in the hamburger view for SP menu items.

    **Note:** You can configure the browse button however the button text is not displayed in the hamburger view. The Browse button display text in the hamburger view is **Browse all**.

-   A quick links related list is available on the root-level for the standard view.
-   A quick links related list is not available on the root-level for the expanded view.
-   Quick links are fetched when you create portal records.

    **Note:** When you use a sync hierarchy, the quick links are not fetched.

-   Only three levels of topics and two levels of SP menu items associated with portal taxonomy are fetched.
-   Visibility of a topic in the Mega menu is based on connected content.​ To avoid display issues, ensure it is active at the source \(topic or SP menu item\) level and at navigation item level in Advanced portal navigation.​
-   When you disable the 'Browse' button in the mega menu from &lt;APN config page/record name&gt;, the browse button is disabled only in the desktop version. Mobile version still displays the Browse button as responsive version of the navigation does not currently support the buttons.

**Related topics**  


[Configure advanced portal navigation](../task/config-adv-portal-nav-as-menu.md)

[config-simplified-nav-as-menu]

