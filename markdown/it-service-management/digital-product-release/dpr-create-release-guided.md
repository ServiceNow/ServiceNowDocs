---
title: Create a release with a wizard
description: Create a release for one or more products or services with the help of a wizard. The wizard guides you through the entire release creation process.
locale: en-US
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 6
breadcrumb: [Use, Digital Product Release, IT Service Management]
---

# Create a release with a wizard

Create a release for one or more products or services with the help of a wizard. The wizard guides you through the entire release creation process.

## Before you begin

-   [Define release scope using product enhancements](dpr-manage-digital-product.md)
-   [Complete the release planning](dpr-plan-feature-version.md) by moving enhancements into different releases

Role required: sn\_dpr\_model.product\_manager

## About this task

Releases can follow a timeline-oriented and stage-oriented release process. For more information, see [Release for a product or service](../concept/dpr-product-release.md).

**Note:** When you edit releases that are in the Draft state, they open in the wizard where you can finish creating them.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the releases icon \(![Releases icon.](../image/dpr-icon-release.png)\).

3.  Select **Create release**.

4.  In the **Release details** step, provide basic information about the release, including the release name, owner, and a brief description.

5.  Select **Release validates a new product version** to determine whether the release validates a version.

    The versions and templates in the next step are determined by this field.

    -   If this option is selected, the **Versions** list only shows only versions that are not validated by other releases. If this option is cleared, the list shows all product versions, regardless of whether they are already validated or not.
    -   Templates with the validate version setting on are only available to select.
6.  In the **Version details** step, select a product or service from the **Primary product or service** and select an existing version or enter a new version number.

    The existing versions listed for a product or service are based on the **Release validates a new product version** field.

    **Note:** If a new version number was entered, it’s automatically created and associated with the release.

    Any Included products associated with the selected product or service are listed.

    You can add more related products or remove any listed related products and their versions.

    -   To add more products, perform the following steps:
        1.  Select **+ Add product**.
        2.  Select one or more related products from the list as needed.
        3.  Select **Add**.
        4.  If any of the selected products also have their own Included products, you can choose to include or exclude them from being added to the release.
            -   To add the selected products and their Included products, select **Yes, add Included products also**.
            -   To add only the selected products without Included products, select **No, add selected products**.
    -   To remove an existing Included product from the list, select the remove included product icon \(![Remove included product icon.](../image/dpr-icon-release-remove.png)\) against the product.

        **Note:** The number of Included products that can be added to a release depends on the system property **sn\_dpr.multi\_product.included\_products\_limit**. A release admin can update the value of this property to increase or decrease the limit.

7.  In the **Release template** step, select a release template to apply to the release.

    The templates listed are based on the **Release validates a new product version** field. If it’s selected, the templates with the validate version setting on are only available to choose.

    A release structure is generated based on the selected release template. For more information about a release template, see [Create a release template](dpr-create-release-template.md#).

8.  In the **Release target** step, select a release readiness target to determine when the release should be ready.

    **Note:** Release readiness target and Release target are used interchangeably. Both terms refer to the same concept - release readiness target date.

    A release target is needed for timeline-oriented releases, while it's not required for stage-oriented releases.

    1.  Select a release calendar.

    2.  Select a release target date on the calendar.

        -   If release targets are available on the selected date, select a target to apply to the release.
        -   If release targets are unavailable on the selected date, a new target is created and applied to the release.
9.  Save or update the release.

    -   Save a new release by selecting **Create release**.
    -   Update the changes to an existing draft release by selecting **Update release**.

## Result

-   One or more releases are created depending on the number of products or services selected:

    -   If you selected a single product or service, one release is created. The release is opened in the Release Overview page.
    -   If you selected a primary product or service and added included products, the releases are created based on the value set in the **sn\_dpr.multi\_product.create\_independent\_releases** system property:
        -   When the property is set to false, a main release is created for the primary product or service and individual releases for each included product are created and added to the main release as dependent releases. The release is opened in the Release Dashboard page.
        -   When the property is set to true, a release bundle is created which contains all the individual releases created for the primary product or service and each included product. The release bundle is opened in the Release bundle's Overview page.
    In either case, the releases are created in the Pending state.

-   If you have selected a timeline-oriented release template, then the following options might apply as defined in the template:
    -   If available, the schedule from the template is applied to the release. The actual working days for the phase and release are calculated by considering the holidays and weekends in the schedule. When considering the holidays for calculating phase or release durations, a release is not created if:

        -   The start date of the release or its phase falls in the past.
        -   The duration exceeds the max duration defined in the system property.
        In that case, you have to select another schedule or adjust the holidays. For more information, see [Holiday schedules in a release](../concept/dpr-release-holiday-schedule.md).

    -   Any key dates from the template are added to the release. The date of each key date is calculated using the number of days from the start or end of the phase specified in the release template.

        **Note:** If the release has a holiday schedule and a key date from the template falls on a holiday, the last workday before or after the holiday is considered as the revised key date.

-   Any artifacts associated with the product or release are added to the release. For more information, see [View and manage data from external tools](dpr-manage-product-ext-tool.md).

    You can add or remove artifacts from a release as needed. For more information, see [Manage artifacts in a release](dpr-work-release-artifact.md).


**Parent Topic:**[Using Digital Product Release](../concept/dpr-using-digital-product-release.md)

