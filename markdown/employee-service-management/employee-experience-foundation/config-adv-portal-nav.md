---
title: Configure advanced portal navigation order
description: Advanced Portal Navigation \(APN\) helps you design and configure an intuitive navigation for better information architecture and discovery. You can reorder topics and non-topic menu items based on employee needs.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Advanced Portal Navigation, Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Configure advanced portal navigation order

Advanced Portal Navigation \(APN\) helps you design and configure an intuitive navigation for better information architecture and discovery. You can reorder topics and non-topic menu items based on employee needs.

## Before you begin

Role required: Admin

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Advanced Portal Navigation**.

2.  Click **New** or view the list of the available portals.

3.  On the Advanced Portal Navigation page, specify **Employee Center** and click **Save**.

    The following active navigation items associated with the portal and taxonomy are fetched and displayed as a related list.

    |Field|Description|
    |-----|-----------|
    |Topic|Topic name fetched from taxonomy.|
    |Menu item|Menu items are fetched from the service portal menu.|
    |Order|Enter a number to indicate where this item appears on the menu relative to other menu items.|
    |Source|Source of the item is usually a taxonomy topic or a service portal menu item.|
    |Taxonomy|Associated active taxonomy of the root topics.|
    |Parent Menu|Parent from where menu items are fetched.|

    **Note:** Use this table to manage the display order of all items in the primary navigation. Order changes made in the taxonomy or SP menu do not reflect on the primary navigation.

4.  Specify the order of navigation menu items based on your needs.

    **Note:** Use increments of 100 when determining the order. This method makes it easier to edit. For example, you numbered your links 1, 2, 3, 4, 5 and wanted to place a new content after 2. You would have to renumber 3, 4, and 5. If you use 100, 200, and 300 and wanted to place content from 100 through 200, you can use any number from 101 through 199. You can use negative numbers such as -100.

5.  Click **Update** for changes to reflect.

    Order and Active status settings persist from this table.

6.  Set the Advanced portal navigation record status value to **Active** to manage the display order and navigation preferences.


## Result

Advanced portal navigation record is saved. You can save multiple records however only one **Advanced portal navigation** record can be **Active**. When you set the status to **Active**, you can control the display order of Employee Center navigation menu items from the table itself. This replaces the existing menu order.

## What to do next

To include any future changes in the service portal menu or root topics in the active taxonomy, you can

1.  Click **Sync menu changes**. The following confirmation message appears.

    `Changes show in the navigation menu right away, placed at the end. You can make edits or change the order of items after the sync is complete. Do you want to sync now?`

2.  Click **Yes** to confirm the updates instantly.

When sync happens, the new items appear in the end. Update the order manually to change the display order.

