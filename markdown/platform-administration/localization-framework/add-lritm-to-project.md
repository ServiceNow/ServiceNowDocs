---
title: Add localization requested items to a project
description: Add multiple localization requested items \(LRITMs\) to a localization project so fulfillers can translate the items in bulk.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/localization-framework/add-lritm-to-project.html
release: zurich
product: Localization Framework
classification: localization-framework
topic_type: task
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [Create translation projects, Localization Framework, Translation and localization, Configure core features, Administer]
---

# Add localization requested items to a project

Add multiple localization requested items \(LRITMs\) to a localization project so fulfillers can translate the items in bulk.

## Before you begin

-   Confirm that your localization project \[sn\_lf\_project\] is in the Draft state.
-   Check the availability of your localization requested items by confirming that they are in the Open state. You can check by navigating to the table Localization Requested Items \[sn\_lf\_requested\_item\]. Also, any items currently attached to another project might not be available for this procedure.
-   Role required: localization\_manager.

## Procedure

1.  Navigate to **All** &gt; **Localization Framework** &gt; **My Projects** \[sn\_lf\_project\].

2.  Open the localization project to which you want to add requested items.

3.  On the Localization Project record, select the **Localization Requested Items** tab from the related list.

4.  Select **Edit**.

    **Note:** The Edit button is visible only when a project is in the **Draft** state.

5.  Adjust the filter conditions for retrieving localization requested items, then select **Run filter**.

    \[Omitted image "add-lritm-to-project1.png"\] Alt text: The Edit Members window is open, showing both the Collection list of available items and the Localization Requested Items list. One item has been selected.

6.  Search for and select localization requested items under **Collection**.

7.  Add the selected items to **Localization Requested Items List** using the right arrow icon.

8.  Select **Save**.

9.  On return to the Localization Project form, select **Start Project** in the form header.

    \[Omitted image "add-lritm-to-project2.png"\] Alt text: On the Localization Project form, the Start Project button is highlighted.

    The state of the project is changed to **In progress** and one or more Localization tasks are created based on settings and requested items.

    After you start the project, you can't add more items to it.


