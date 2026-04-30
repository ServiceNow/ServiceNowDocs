---
title: Update the scope of a release
description: Review and update the scope of the release by adding or removing product enhancements, planning items, and related tasks like incidents and problems.
locale: en-US
release: xanadu
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2024-11-04"
reading_time_minutes: 2
breadcrumb: [Manage releases for digital products and services, Using Digital Product Release, Digital Product Release, IT Service Management]
---

# Update the scope of a release

Review and update the scope of the release by adding or removing product enhancements, planning items, and related tasks like incidents and problems.

## Before you begin

Role required: sn\_dpr\_model.product\_manager or sn\_dpr\_model.release\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the releases icon \(![Releases icon.](../image/dpr-icon-release.png)\).

3.  Select a release from the list to open.

4.  Select **Release scope** to manage product enhancements, work items, planning items, and tasks in the release.

    **Note:** The tabs for task types that you see depend on the permissions required to view those task type records and the system property **sn\_dpr.release\_related\_record\_types**. For more information, see [Digital Product Release properties](../reference/digital-product-release-properties.md).

5.  Select the **Product enhancements and Work items** tab to manage product enhancements and work items in the release.

    -   [Add an enhancement to a product or service](dpr-create-product-enhancement.md)
    -   [Add a product enhancement from an epic](dpr-add-product-enhancement-from-epic.md)
    The product enhancements added to the release are listed in the Product enhancements and Work items tab.

6.  Select the **Planning Items** tab to view planning items associated with the product enhancements in the release.

    **Note:** The **Planning Items** tab is available only when the following conditions are met:

    -   You have one of the following roles required to view those items
        -   sn\_dpr\_model.product\_enhancement\_read
        -   sn\_dpr\_model.release\_admin
        -   sn\_dpr\_model.release\_user
        -   sn\_dpr\_model.product\_manager
        -   sn\_dpr\_model.release\_coordinator
    -   ServiceNow® Strategic Planning Workspace is installed with the Digital Product lens configured

        For more information about the lenses and portfolio plans, see [Lenses in Strategic Planning](https://www.servicenow.com/docs/access?context=lens-alignment-planner-workspace&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US) and [Portfolio plans in Strategic Planning](https://www.servicenow.com/docs/access?context=portfolio-plans-in-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

    1.  Select a planning item number to view its details.

    A list of the planning items associated with the product enhancements displays.

7.  Manage related tasks in the release.

    -   To add a related task, select **Add**.
        1.  Select the tab in which you would like to add a task.

            A list of the records of the selected task type displays.

        2.  Select one or more records from the list and then select **Add**.

            The selected task records are added to the release.

    -   To remove a related task, select it from the list and select **Remove**.

**Parent Topic:**[Manage releases for digital products and services](dpr-manage-releases.md)

