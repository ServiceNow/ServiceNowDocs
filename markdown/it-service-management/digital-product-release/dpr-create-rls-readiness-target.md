---
title: Create a release readiness target
description: Create release readiness targets to define the dates by which the releases must be ready for deployment. These targets help you to track and manage capacity and conflicts while ensuring a smooth delivery of your products.
locale: en-US
release: yokohama
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 1
breadcrumb: [Configure, Digital Product Release, IT Service Management]
---

# Create a release readiness target

Create release readiness targets to define the dates by which the releases must be ready for deployment. These targets help you to track and manage capacity and conflicts while ensuring a smooth delivery of your products.

## Before you begin

Role required: sn\_dpr\_model.release\_calendar\_admin orsn\_dpr\_model.release\_admin

## About this task

-   The release readiness target dates indicate when the products should be ready. They aren’t the actual deployment dates.
-   You can set either a single or recurring release readiness target on a release calendar.

**Note:** Release readiness target and Release target are used interchangeably. Both terms refer to the same concept - release readiness target date.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the release calendar icon \(![Release calendar icon.](../image/dpr-icon-rls-target.png)\).

3.  Select a calendar on which you want to create release readiness targets.

4.  Create a release readiness target or update an existing one.

    -   To create a release readiness target, select **Create release target**.
    -   To modify an existing release readiness target, open the release readiness target from the calendar or list.
5.  In the dialog box, fill in the fields.

    For more information on release readiness target field descriptions, see [Release readiness target form](../reference/create-release-readiness-target-form.md).

6.  Select **Next**.

7.  If your target dates conflict with scheduled events, you will see a list of those dates, and you can choose to create or not create targets on those dates.

    -   To create release targets for conflicting dates, select the check box under the **Opt-in** column next to the dates.
    -   If you don't want to create release targets for those dates, clear **Opt-in**.
    **Note:** By default, the **Opt-in** check boxes for all conflicting dates are clear, which means that the target dates will not be created for those dates.

8.  Select **Create**.


## Result

Release readiness targets are created and displayed on the selected calendar. Release targets that overlap with dates in the exclusion scheduleare created only for the dates for which you selected to opt in to.

