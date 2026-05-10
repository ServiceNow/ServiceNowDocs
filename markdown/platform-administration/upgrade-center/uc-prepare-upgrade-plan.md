---
title: Prepare to upgrade with Upgrade Plan
description: Prepare your instance upgrade with Upgrade Plan by determining all the applications and plugins are ready to be implemented in the upgrade.
locale: en-US
release: australia
product: Upgrade Center
classification: upgrade-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Preparing your upgrade plan, Using Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Prepare to upgrade with Upgrade Plan

Prepare your instance upgrade with Upgrade Plan by determining all the applications and plugins are ready to be implemented in the upgrade.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Upgrade Plan**.

    The upgrade plan that is installed shows up on the list.

2.  Select the upgrade plan.

    The upgrade plan form view shows up with all its configurations.

3.  To ensure that all the applications and plugins are ready to be implemented in the upgrade, select **Refresh** in the context menu of the Upgrade Plan.

    If there are errors for any of the items, then fix them and follow the Reprocess step.

    **Note:** All the applications and plugins under the Upgrade Plan Items related list must be in the **Ready** state to proceed with the upgrade. The application or plugin in the **Already Installed** state, error or its latest version won't be considered during the upgrade process.

    The upgrade plan is now ready to be implemented.

4.  Apply an existing upgrade plan to an instance anytime, without being limited to during upgrades only.

    You can now also export the upgrade plan in a batch install format by using the **Export** button. See [CI/CD - POST /sn\_cicd/app/batch/install](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/cicd-api.md) for more information.

5.  Select **Reinstall** to reinstall the failed items in an upgrade plan, after the upgrade completes.

    You can also review the upgrade plan history to know the reasons of failure.

    **Note:** You are required to use this option only if you have failed items in an upgrade plan.

6.  Click **Reprocess** to reprocess the upgrade plan after the upgrade plan item errors have been resolved.

    **Note:** This step is applicable only if you have any error items in the upgrade plan.


-   **[Preview Upgrade Plan](uc-preview-upgrade-plan.md)**  
Preview your upgrade plan before being implemented in the upgrades. Once the upgrade plan is installed, it auto generates the preview of the upgrade plan.

**Parent Topic:**[Preparing your upgrade plan](../concept/uc-prepare-up.md)

**Related topics**  


[Building your Upgrade Plan](uc-building-upgrade-plan.md)

[Refreshing your Upgrade Plan](uc-refreshing-upgrade-plan.md)

[Installing your Upgrade Plan](uc-installing-upgrade-plan.md)

[Apply Upgrade Plan on your upgrade](uc-apply-upgrade-plan.md)

