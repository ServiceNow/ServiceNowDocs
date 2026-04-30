---
title: Prepare to upgrade with Upgrade Plan
description: Prepare your instance upgrade with Upgrade Plan by determining all the applications and plugins are ready to be implemented in the upgrade.
locale: en-US
release: yokohama
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Upgrade Plans tool in Upgrade Console, Upgrade Console tools, Using Upgrade Console, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Prepare to upgrade with Upgrade Plan

Prepare your instance upgrade with Upgrade Plan by determining all the applications and plugins are ready to be implemented in the upgrade.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to Upgrade Plan using one of the following ways.

    |Option|Navigation|
    |------|----------|
    |Using left navigation|Navigate to **All** &gt; **Admin Center** &gt; **Upgrade Management** &gt; **Upgrade Plan**.|
    |Using Admin tab option|Navigate to **Admin** &gt; **Upgrade Management** &gt; **Upgrade Plan**.|

    The upgrade plan that is installed shows up on the list.

2.  Select the upgrade plan.

    The upgrade plan form view shows up with all its configurations.

3.  To ensure that all the applications and plugins are ready to be implemented in the upgrade, select **Refresh** in the context menu of the Upgrade Plan.

    If there are errors for any of the items, then fix them and follow the Reprocess step.

    **Note:** All the applications and plugins under the Upgrade Plan Items related list must be in the **Ready** state to proceed with the upgrade. The application or plugin in the **Already Installed** state, error or its latest version won't be considered during the upgrade process.

    The upgrade plan is now ready to be implemented.

4.  Apply an existing upgrade plan to an instance anytime, without being limited to during upgrades only.

    You can now also export the upgrade plan in a batch install format by using the **Export** button. See [CI/CD - POST /sn\_cicd/app/batch/install](https://www.servicenow.com/docs/access?context=cicd-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) for more information.

5.  Select **Reinstall** to reinstall the failed items in an upgrade plan, after the upgrade completes.

    You can also review the upgrade plan history to know the reasons of failure.

    **Note:** You are required to use this option only if you have failed items in an upgrade plan.

6.  Click **Reprocess** to reprocess the upgrade plan after the upgrade plan item errors have been resolved.

    **Note:** This step is applicable only if you have any error items in the upgrade plan.


-   **[Preview Upgrade Plan](um-preview-upgrade-plan.md)**  
Preview your upgrade plan before being implemented in the upgrades. Once the upgrade plan is installed, it auto generates the preview of the upgrade plan.

**Parent Topic:**[Upgrade Plans tool in Upgrade Console](../concept/um-upgrade-plans-tool.md)

**Related topics**  


[Building your Upgrade Plan](um-building-upgrade-plan.md)

[Refreshing your Upgrade Plan](um-refreshing-upgrade-plan.md)

[Installing your Upgrade Plan](um-installing-upgrade-plan.md)

[Apply Upgrade Plan on your upgrade](um-apply-upgrade-plan.md)

