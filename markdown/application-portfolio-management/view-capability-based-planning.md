---
title: Use capability map for planning
description: Capability-based planning helps you to understand your business capabilities, and the business applications that support them, to achieve your business goals.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Using Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Use capability map for planning

Capability-based planning helps you to understand your business capabilities, and the business applications that support them, to achieve your business goals.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy capability ratings module has been deprecated from Enterprise Architecture \(formerly Application Portfolio Management\). However, if you’re an existing user of Enterprise Architecture \(formerly Application Portfolio Management\), you can still use the legacy capability ratings module. If you’re a new activation user, the legacy capability ratings module isn’t available.

You can leverage the same features by using the Enterprise Architecture Workspace. To learn more, see [Exploring a business portfolio](../concept/manage-business-portfolio.md).

Role required: sn\_apm.apm\_analyst

## About this task

Capability map is a pictorial representation of the capability-based planning displaying capabilities in a hierarchy. The hierarchical structure helps you to easily drill down to the lowest level and identify major and minor gaps. With this map, you get a complete view of all the capabilities, the applications associated with each of the capabilities, and the indicator scores of each business application in association with the capability.

The capabilities are color-coded which enables you to identify, in a glimpse, those capabilities that have major, medium, and minor gaps. Since you have visibility of the business applications that support the capabilities, you can create goals, demands, or programs to improve the performance of the applications.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Capability Ratings** &gt; **Capability Map**.

    The left pane lists all parent capabilities in the hierarchy. By default, the first business capability in the hierarchy at level 0 expands to display its immediate child capabilities at level 1. For subsequent business capabilities and child capabilities, click the icon to expand and view its sub-capabilities at each level. This view is similar across Business Capability, Technology Risk, and also in Manage Capability Hierarchy views.

    The left pane also displays the total count of sub-capabilities below each parent capability, the total number of business applications directly related to each capability, and their capability score. Similarly, on expanding a parent capability, you can see the number of subcapabilities, the total count of business applications that are directly related to the sub-capability at that level.

    The right pane displays the overall capability summary of the business capabilities in your enterprise with the following details. It shows the overall capability risk summary if you toggle to the technology risk view.

    -   **Capabilities**

        Total number of business capabilities that are displayed in the list on the left pane. The total number of capabilities is displayed for both **Business Capability** and **Technology Risk** views.

    -   **Leaf Capabilities**

        Total number of capabilities at the leaf level \(that has no child capabilities of its own\) in all the hierarchies of the business capabilities listed in the left pane.

    -   **Assessed**

        Total number of assessed business capabilities.

    -   **Not Assessed**

        Total number of capabilities that haven’t been assessed.

    -   **Major Gap**

        Total number of capabilities whose scores falls within the range of 1-4.

        The Technology Risk view displays the number of capabilities that use applications whose technologies are at a greater risk.

    -   **Medium Gap**

        Total number of capabilities whose scores falls within the range of 4-7.

        For the Technology Risk view, it displays the number of capabilities that use applications whose technologies are at a medium risk.

    -   **No Gap**

        Total number of capabilities whose scores falls within the range of 7-10.

        For Technology Risk view, it displays the number of capabilities that use applications whose technologies have no risk at all.

2.  By default the overall summary of capabilities is displayed.

    Use one of the following choices to configure the view, and the details that you want to see in the capability map:

    -   **Business Capability** view: Selecting **Business Capability** enables the scores view. It displays the capabilities and applications associated with it.

        With this view, you have the following search option:

        **Fiscal period**: Select a fiscal period to view the capability scores generated for that fiscal period. If the capability isn’t assessed for the fiscal period, then is it displays as **Not Assessed**. Conversely, you must also select a fiscal period to view the capability details, otherwise the system alerts you with an error message.

    -   **Technology Risk** view: Select the **Technology Risk** view to know the capabilities that are at risk due to their end of life or expired technologies. It displays the overall summary of business capabilities and the technology risk of each business application. It also shows the capabilities that are impacted as a result of the technology risk. The technology risk on the capability is derived from the technology risk on a business application.
    -   **Enter Search Capabilities**

        Use the **Enter Search Capabilities** field to enter a text and search a business capability that you’re looking for.

    -   **Legend \(\)**

        Lists the categories in color legends and the corresponding description. Also lists icons used in the map.

    -   **Create**

        Select the list to [create a demand](create-an-idea.md), a goal, or a program for the capability that you have currently selected.

        Similarly, toggle over to the technology risk view to raise a demand, create a goal, or a program for the underlying technology of an application if the technology is at risk.

        **Note:** The Program option is available only when you activate the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin.

    -   **Manage Capability Hierarchy**

        Enables you to create a level-0 capability, add a child capability, edit an existing capability, and also to delete a leaf-level capability in the capability map. You can manage all the [business capability relationship](manage-relationships-in-capability-map.md) in the UI without having to navigate to the Business Capability form to do these functions.

3.  Expand each business capability to view the capability details and technology risk details.

    For more information, see [View business capability details in capability map](capability-details-map.md) and [View technology risk details in capability map](technology-risk-map.md).


-   **[View business capability details in capability map](capability-details-map.md)**  
Use the capability map to assess capabilities on dimensions such as people, process, and technologies and plan investments accordingly. View the current trend of your business applications and plan to potentiate them by creating goals, demands, and programs and track their progress in the map.
-   **[View technology risk details in capability map](technology-risk-map.md)**  
Use the technology risk view of the capability map to know the risk profiles of the technologies that support the business capability.
-   **[Manage capability hierarchy in the capability map](manage-relationships-in-capability-map.md)**  
Create a root-level capability, add a child capability to a parent, edit a capability, and delete a leaf capability, and manage the relationships between the capabilities in the capability map.

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/using-apm.md)

