---
title: Create a release
description: Specify the details for your release, including the target instance that the changes will be deployed to and when the release should occur.
locale: en-US
release: zurich
product: ReleaseOps
classification: releaseops
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [ReleaseOps, deploy changes, update sets, pipeline, ATF, schedule a release, deployment request, deployment analyzer]
breadcrumb: [Use, ReleaseOps, Deploying applications, Building applications]
---

# Create a release

Specify the details for your release, including the target instance that the changes will be deployed to and when the release should occur.

## Before you begin

Role required: release\_admin

## Procedure

1.  On your production instance, navigate to **All** &gt; **ReleaseOps** &gt; **Releases**.

2.  Select **New**.

3.  On the new release form, select the **Destination environment** field, then select your target destination instance from the list.

    Typically, the target destination instance is your production instance. However, some organizations might have different target destination instances, depending on their pipeline. For more information about the pipeline environments, see [Pipelines in ReleaseOps](../concept/releaseops-pipeline-environments.md).

4.  Select the **Pipeline** field, then select the pipeline that you want the release to use.

5.  Enter a short description for the release in the **Short description** field.

6.  Enter a description for the release in the **Description** field.

7.  Set a freeze date for the release.

    A freeze date is the date by which all changes for the release must be submitted via deployment requests and ready for deployment. Any changes that aren’t ready for deployment are deferred at the time of the freeze date.

    1.  Select the Select freeze date and time icon \(![](../../../use/reporting/image/inline-data-vis-96px-calendar-days.png)\).

    2.  Select the Previous month icon \(![](../image/releaseops-previous-month-icon.png)\) or Next month icon \(![](../image/releaseops-next-month-icon.png)\) to locate the month and year for your intended freeze date.

    3.  Select your freeze date by selecting the date.

        ![Select the Select freeze date and time icon and choose your freeze date from the calendar pop-up to set your freeze date.](../image/releaseops-select-freeze-date.png)

    4.  Set the time for the freeze date by entering a time in the **Time** fields.

    5.  Select the Enter icon \(![](../../creator-studio/image/crs-save-check.png)\).

8.  Set a release date for the release.

    A release date is the date by which the changes that apply to the release are deployed to the target destination instance, typically the production instance.

    **Note:** If your release is associated with a change request, the **Release date** field is automatically populated by the scheduled date in the change request.

    1.  Select the Select release date and time icon \(![](../../../use/reporting/image/inline-data-vis-96px-calendar-days.png)\).

    2.  Select the Previous month icon \(![](../image/releaseops-previous-month-icon.png)\) or Next month icon \(![](../image/releaseops-next-month-icon.png)\) to locate the month and year for your intended release date.

    3.  Select the date for your release date by selecting the date.

    4.  Set the time for the release date by entering a time in the **Time** fields.

    5.  Select the Enter icon \(![](../../creator-studio/image/crs-save-check.png)\).

9.  Select **Activate release** to activate the release.

    Once a release is activated, you can select the release as an available option when creating deployment requests for scheduled releases.


**Parent Topic:**[Using ReleaseOps to manage deployments](../concept/using-releaseops-to-manage-deployments.md)

