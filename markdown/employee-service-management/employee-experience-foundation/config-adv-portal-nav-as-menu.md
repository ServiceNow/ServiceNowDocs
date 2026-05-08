---
title: Configure advanced portal navigation
description: Advanced Portal Navigation \(APN\) helps you design and configure an intuitive navigation for better information architecture and topic discovery.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Advanced Portal Navigation, Setup Employee Center browse experience features, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Configure advanced portal navigation

Advanced Portal Navigation \(APN\) helps you design and configure an intuitive navigation for better information architecture and topic discovery.

## Before you begin

Before you start, ensure you understand the useful information available in [EC Information architecture](../concept/ec-information-architecture.md).

Role required: Admin and SP Admin

## About this task

Using the advanced portal navigation, you can enable single-click sync across all APN hierarchy levels, replacing level-by-level sync. You can design the primary navigation menu and configure the navigation setup as per employee needs and content priorities. Here is an overview of the navigation workflow:

![APN sync hierarchy workflows](../images/apn-architecture-workflow.png "APN architecture")

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Advanced Portal Navigation**.

2.  Click **Take a tour** to understand the APN process.

    Understand more about APN process and configuration from the explainer tour.

3.  Click **New** to create a new record or view the list of the available APN record.

4.  Select **Active** to replace the current Employee Center with the new navigation menu.

    **Note:** Only one Advanced portal navigation record \[sn\_ex\_sp\_portal\_extensible\_navigation\] can be active per portal. When you have one active record, you must first deactivate the other one first.

5.  Click **Submit** or **Save**.

    A pop-up appears with the following message.

    ```
    To help you get started, we can bring over your existing navigation menu items and you can edit from there. 
    You can also skip this and start from scratch. Do you want to bring over your current menu now?
    ```

6.  On the **Start with current navigation menu**, select one of the following options.

    -   **Skip**: When you click skip, the existing associated navigation menu items and topics are not fetched and you can start building your hierarchy afresh.
    -   **Yes**: When you click yes, the existing associated navigation menu items, topics, and associated quick links are fetched instantly and you can refine the hierarchy.
    The **Menu items** related list appears.

    **Note:** An empty list appears when you click the skip option.

7.  Use one of the options to create new or fetch the existing hierarchy.

    1.  Click **New** to create or add from the available list.

    2.  Click **Sync hierarchy** to fetch existing items.

        Topics and menu items which are in the **Active** state are synced. Confirm sync popup appears with info on email notification.

        **Note:** Quick links are not fetched. Add quick links manually.

    ![How to activate Advanced Portal Navigation record and menu items](../images/apn-menu-items-list.png "APN Menu items and sync hierarchy")

8.  On the **Navigation menu item** related list, fill in the form.

    **Note:** The following fields are available in the base system starting with [Employee Center](https://store.servicenow.com/sn_appstore_store.do#!/store/application/4249e63a28d54d61bb6fbf61fd86cccb/31.0.3) version 31.

<table id="table_uww_v2g_5qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

Source of the item is usually a taxonomy topic or a service portal menu item.

</td></tr><tr><td>

Application

</td><td>

Application in scope for this activity.

</td></tr><tr><td>

Topic

</td><td>

Topic name fetched from taxonomy. Depending on the level, you can select the children topics from the available list.**Note:** Ensure that the topic or menu item is already associated in the parent navigation.

Only active topics and menu items are available for creating navigation.

</td></tr><tr><td>

Menu path

</td><td>

Path for the menu item. When you open an available APN menu item, the menu path appears. Path indicates the parent-child association, for example **/Help center/Technology services**.

</td></tr><tr><td>

Menu item

</td><td>

Menu item fetched from the service portal menu.

</td></tr><tr><td>

Order

</td><td>

Enter a number to indicate where this item appears on the menu relative to other menu items.

</td></tr><tr><td>

Active

</td><td>

Status of the record. Only Active records are synced.

</td></tr><tr><td>

Render as

</td><td>

Indicates the rendering type that you want.-   **Menu**: Select this option to display as a menu.
-   **Modal window**: Select this option to display as a modal window. Use widget and widget parameters to customize experience.


</td></tr><tr><td>

Submenu display type

</td><td>

Indicates the rendering type that you want to display in the menu. This field appears only when **Menu** is selected at the root-level hierarchy.-   **Expanded**: Select this option to display in the expanded view.
-   **Standard**: Select this option to display in the standard view. Out-of-the-box is Standard.
For more information, see [EC Information architecture](../concept/ec-information-architecture.md).

</td></tr><tr><td>

Widget

</td><td>

Select this option to use the available widgets to customize experience. This field appears only when **Modal window** is selected.

</td></tr><tr><td>

Widget parameters

</td><td>

The modal window renders the widget content based on the name-value pair of widget parameters. This field appears only when **Modal window** is selected.

</td></tr><tr><td>

Browse button

</td><td>

Select this option to show the browse menu option. For the root-level hierarchy, select the Browse button and specify the display text. When you select this option with empty text, the default display is **Browse all**.**Note:** For standard view, the browse option is available on the root-level and for the expanded view root-level and first-level only.

</td></tr><tr><td>

Browse button display text

</td><td>

Select this option to show the browse option on the menu. -   When you select taxonomy as source, the Browse button display text is automatically generated based on the topic. For example, when you select HR Systems as Topic, the display text shows **Browse HR systems**.
-   When you edit a menu item or sync, manually specify the Browse button display text, for example, `Browse <your text>`.
-   When you do not specify any display text, the button displays **Browse all**.


</td></tr></tbody>
</table>    **Note:** Use this table to manage all items in the primary navigation. Hierarchy changes made in the taxonomy or SP menu do not reflect on the primary navigation.

9.  Track the sync status from the following fields:

    -   **Sync status** indicates the status of the sync such as **Never synced**, **In progress**, and **Completed**.

        **Note:** An email notification is sent with the sync results indicating the addition of new items, if any.

        When Sync is in progress, you can't perform actions such as Update or Delete from the APN or Menu items records.

    -   **Last synced** indicates the time of the last sync.
    **Note:** To display the Sync status, ensure you deactivate the **Hide sync status** UI policy from **All** &gt; **System UI** &gt; **UI Policies**. For more information, see Using UI policies

10. Notify the sync status through email.

    On completion, you receive information on the sync status update with the count of changes.

    **Note:** If you face issues with the sync, contact your administrator.

    ![APN Sync status email notification](../images/apn-sync-status-email.png "APN sync status email")

11. Click **Update** for changes to reflect.


## Result

Advanced portal navigation record is saved and your employees can view the new mega menu design.

## What to do next

All active navigation items associated with the portal and taxonomy are fetched and displayed in the related list.

-   While creating the record or for subsequent syncs, all the fetched navigation menu items are in the **Active** state by default.
-   To include any future changes in the service portal menu or root topics in the active taxonomy, you can use **Sync hierarchy** to bring any new topics or menu items.
-   Newly synced items are **active** by default with the existing order. When the order is not available for topic, the order is 999999.
-   You can make edits, if necessary, after the sync is complete.
-   All taxonomy updates across all APN hierarchy levels are in sync with a single-click.​

**Note:** For successful sync, ensure that the SP Menu Items are associated with the portal for which the Advanced Portal navigation record is configured.

For more information, see [EC Information architecture](../concept/ec-information-architecture.md).

