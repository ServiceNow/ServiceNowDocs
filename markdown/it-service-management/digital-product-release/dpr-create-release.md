---
title: Create a release for a product or service
description: Create a product or service release when all planned product enhancements and product features are ready.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use, Digital Product Release, IT Service Management]
---

# Create a release for a productor service

Create a product or service release when all planned product enhancements andproduct features are ready.

## Before you begin

-   [Define release scope using product enhancements](dpr-manage-digital-product.md)
-   [Complete the release planning](dpr-plan-feature-version.md) by moving enhancements into different releases

Role required: sn\_dpr\_model.product\_manager

## About this task

Releases can follow a timeline-oriented and stage-oriented release process. For more information, see [Release for a product or service](../concept/dpr-product-release.md).

For creating a release for multiple products using the wizard, see [Create a release with a wizard](dpr-create-release-guided.md).

**Note:** Release readiness target and Release target are used interchangeably. Both terms refer to the same concept - release readiness target date.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Create a release for a product version from the Release planning page or the Releases list view.

<table id="choicetable_mxj_fsr_lyb"><thead><tr><th align="left" id="d98486e151">

Option

</th><th align="left" id="d98486e154">

Steps

</th></tr></thead><tbody><tr><td id="d98486e160">

**From the Release planning page of a product**

</td><td>

1.  Select the products and services icon \(![Products and services icon.](../image/dpr-icon-products.png)\).
2.  Select a product or service from the list to open.
3.  Select **Release planning**.
4.  Select the sub menu icon \(![Sub menu icon.](../image/dpr-icon-menu.png)\) on a version lane and select the **Create release** menu option.


</td></tr><tr><td id="d98486e211">

**From the Releases list view**

</td><td>

1.  Select the releases icon \(![Releases icon.](../image/dpr-icon-release.png)\).
2.  Select the more actions icon next to the **Create release** button and then select **Quick create**.


</td></tr></tbody>
</table>3.  In the dialog box, fill in the fields.

    For more information on release field descriptions, see [Release form](../reference/create-release-form.md).

4.  Select **Confirm**.


## Result

-   A release is created in the Draft or Pending state based on the following conditions:
    -   If all fields on the form are filled, the release is created in the Pending state and opens in the Release Dashboard page.
    -   If either the **Release template** or **Release readiness target** fields, or both, are empty, the release is created in the Draft state.

        You can finish creating the release later from the Release Planning page or from the Releases list.

-   If you have selected a timeline-oriented release template, then the following options might apply as defined in the template:
    -   If available, the schedule from the template is applied to the release. The actual working days for the phase and release are calculated by considering the holidays and weekends in the schedule. When considering the holidays for calculating phase or release durations, a release is not created if:

        -   The start date of the release or its phase falls in the past.
        -   The duration exceeds the max duration defined in the system property.
        In that case, you have to select another schedule or adjust the holidays. For more information, see [Holiday schedules in a release](../concept/dpr-release-holiday-schedule.md).

    -   Any key dates from the template are added to the release. The date of each key date is calculated using the number of days from the start or end of the phase specified in the release template.

        **Note:** If the release has a holiday schedule and a key date from the template falls on a holiday, the last workday before or after the holiday is considered as the revised key date.

-   If an out-of-band release is created on a date that already has a release target, it uses that release target. However, if there’s no release target for that date, one is created, when the system property **sn\_dpr.out\_of\_band\_release\_allowed** is set to true. The release admin for this new release target is the same as the one for the selected release calendar.
-   Any artifacts associated with the product or release are added to the release. For more information, see [View and manage data from external tools](dpr-manage-product-ext-tool.md).

    You can add or remove artifacts from a release as needed. For more information, see [Manage artifacts in a release](dpr-work-release-artifact.md).


**Parent Topic:**[Using Digital Product Release](../concept/dpr-using-digital-product-release.md)

