---
title: Building your Upgrade Plan
description: Build your upgrade plan to experience a seamless and an accelerated upgrade by packaging the applications in an upgrade plan.
locale: en-US
release: australia
product: Upgrade Center
classification: upgrade-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Preparing your upgrade plan, Using Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Building your Upgrade Plan

Build your upgrade plan to experience a seamless and an accelerated upgrade by packaging the applications in an upgrade plan.

## Before you begin

**Note:** Ensure that you have upgraded your instance to the latest available version to build the upgrade plan. It is recommended to build an Upgrade Plan for each instance upgrade. The target version of the Upgrade Plan must be exactly the same as the instance version \(including patches and hot fixes\). You can’t use the previously created Upgrade Plan for the new instance upgrade.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Upgrade Center** &gt; **Administration** &gt; **Properties** &gt; **Upgrade Plan Properties**.

    **Note:** It is recommended to set up your dev instance as a builder instance.

2.  Navigate to **All** &gt; **Upgrade Center** &gt; **Upgrade Plan**.

    **Note:** If you are on the Upgrade Monitor page, click **Manage Upgrade Plan**.

    The Upgrade Plan list view shows up.

3.  Click **Build** to start the upgrade plan build.

    Upgrade Plan takes up only the app installations by default and publish it on to the app repository. See Upgrade Plan background operations section in [Upgrade Plan overview](../concept/uc-upgrade-plan.md) for more information.

    **Note:** Ensure all the applications in the instance are in ready state to be published on to the app repository.

    You are allowed to have only one Upgrade Plan at any point of time.

    A final confirmation message shows up to start building the upgrade plan. If any application has changes in-progress, the Upgrade Plan must be built only after the changes are done. Warning message shows up to complete the review of the remaining skipped records, provided you have enabled the GLIDE\_UPGRADE\_PLAN\_INCLUDE\_SKIPS property.

4.  Click **Build Upgrade Plan**.

    The upgrade plan starts to build.

5.  Click **Go to Upgrade Plan** once the build is done.

    **Note:** Click **View Details** if you want to view the execution details of the Upgrade Plan. If you see a warning, it is recommended to review the execution details to know the errors.

    The upgrade plan opens and a list of upgrade plan items shows up.

6.  Click **New** if you want to manually add any upgrade plan items.

    **Note:** The applications or plugins that you want to add manually to the upgrade plan must be already installed and active on the instance.

    If you want to skip any of the upgrade plan items from being a part of the Upgrade Plan, set the selected upgrade plan item to false.

7.  Click **Refresh** to capture all the recent changes to the Upgrade Plan.

    **Note:** This step is applicable only if you have any update on the existing application or plugin in the Upgrade Plan. If the upgrade plan has already been published, you are required to republish it after every refresh.

8.  Click **Publish** to publish the Upgrade Plan.

    See Upgrade Plan background operations section in [Upgrade Plan overview](../concept/uc-upgrade-plan.md) for more information.

    **Note:** Install all the required applications and plugins before publishing the upgrade plan. If you have set the GLIDE\_UPGRADE\_PLAN\_INCLUDE\_SKIPS property to true, you will have to resolve all the skipped records before publishing the upgrade plan. If you want to delete the Upgrade Plan, click **Delete**. The **Delete** option is available only for the Upgrade Plans that are not yet published.

    ![Upgrade plans screen.](../image/uc-publish-plan.png)

    The upgrade plan is now ready to be installed in the consumer instance.


**Parent Topic:**[Preparing your upgrade plan](../concept/uc-prepare-up.md)

**Related topics**  


[Refreshing your Upgrade Plan](uc-refreshing-upgrade-plan.md)

[Installing your Upgrade Plan](uc-installing-upgrade-plan.md)

[Prepare to upgrade with Upgrade Plan](uc-prepare-upgrade-plan.md)

[Apply Upgrade Plan on your upgrade](uc-apply-upgrade-plan.md)

