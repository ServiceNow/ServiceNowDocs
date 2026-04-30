---
title: Configure Mega menu
description: The mega menu enables you to easily navigate to a topic and its child topic. The taxonomy you associate with the employee center portal record determines the mega menu and its menu items. By default, the topics and child topics you create in the taxonomy are displayed as mega menu items.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
keywords: [mega menu, servicenow mega menu, menu taxonomy]
breadcrumb: [Setup browse experience features, Configure, Employee Center, Employee Service Management]
---

# Configure Mega menu

The mega menu enables you to easily navigate to a topic and its child topic. The taxonomy you associate with the employee center portal record determines the mega menu and its menu items. By default, the topics and child topics you create in the taxonomy are displayed as mega menu items.

## Before you begin

Role required: admin

## About this task

Taxonomy topics become available to you after you install and activate the Employee Experience Taxonomy plugin \(sn\_ect\). The base system taxonomy—Employee—is installed when you install the Employee Experience Taxonomy plugin.

To modify the default taxonomy, clone the taxonomy first, and then create new parent topics and their child topics. The root topics are shown in the mega menu. The child topics up to two levels are listed under the mega menu and displayed when you click the mega menu. Click **Browse** &lt;topic\_name&gt;&lt;topic\_name&gt; to open the parent topic. For example, click the **Browse all** to open the IT parent topic. The following figure shows the IT menu items.

**Note:** Only the active topics that have connected content are shown in the mega menu.

For more information on the EC information architecture and configuring the portal navigation, see [Advanced Portal Navigation](../concept/adv-portal-navigation-overview.md).

![Mega menu with its options and the Browse all button at the bottom.](../images/mega-menu-browse-all.jpg "Mega menu on the Employee Center home page")

**Note:** You can customise the primary and background color from CSS variables.

In Employee Center, the default Employee taxonomy includes IT, HR, Workplace, Legal, and Procurement mega menus. The mega menu displays three levels of topics \(root topic, child topic 1, and child topic 2\). For example, **IT &gt; Hardware &gt; Printers**.

-   Simple list: If a root topic has only one level of child topic 1, that is, if the child topic 1 does not have child topic 2, the child topic 1 is displayed as a simple list under the root topic menu.
-   Single column: If child topic 2 \(2nd level topics\) has upto 10 under child topic 1, UI is displayed as single column.
-   Two columns: If child topic 2 exceeds 10 under child topic 1, UI is displayed as two columns.
-   Two columns with topic page: If child topic 2 has more than 20 under child topic 1, UI displays only 20 child topic 2s as two columns. For remaining topics, navigate to Topic Page of child topic 1 and verify in Sub-Topics widget.

**Note:** As changes are saved in session cache, the user has to re-login to reflect any topic changes on the mega menu.

## Procedure

1.  Do one of the following:

    -   Clone the taxonomy for employee content. For more information, see [Clone taxonomy for employee content](clone-taxonomy-content.md).
    -   Manually create a taxonomy. For more information, see [Create taxonomy](create-taxonomy-content.md).
2.  Create a root topic and associate it with the cloned or new taxonomy.

    For more information, see [Create and associate topics](create-topics-for-taxonomy.md).

3.  Create a child topic and associate it with the parent topic.

    For more information, see [Create a child topic](create-child-topics-for-parent.md). Repeat this step to create as many child topics as needed.

4.  Associate connected content to the topics.

    For more information, see [Associate connected content to a topic](associate-content-to-topics.md).

    **Note:** You can view topics on the mega menu only if you have access to at least one connected content.

5.  [Enable user criteria for topics](enable-user-criteria-topics.md) to set up topic-level visibility settings.


## What to do next

You can also add non-taxonomy menu items to the primary navigation bar. For more information, see [Add menu items to primary navigation](add-menu-items.md).

**Note:** When the mega menu is empty, check if the demo data for the Employee Experience taxonomy app is installed. Select the Load demo data check-box to include the demo data along with your install or repair.

