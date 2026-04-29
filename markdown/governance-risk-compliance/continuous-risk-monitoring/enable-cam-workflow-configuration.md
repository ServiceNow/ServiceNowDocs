---
title: Enable CAM workflow configuration
description: Enable the CAM workflow configuration to use custom workflows and frameworks in CAM. This feature enables you to configure workflows beyond the default National Institute of Standards and Technology \(NIST\) framework and adapt CAM to your organization's specific requirements.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CAM workflow configuration, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Enable CAM workflow configuration

Enable the CAM workflow configuration to use custom workflows and frameworks in CAM. This feature enables you to configure workflows beyond the default National Institute of Standards and Technology \(NIST\) framework and adapt CAM to your organization's specific requirements.

## Before you begin

Role required: sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization and Monitoring** &gt; **Administration** &gt; **Properties**.

2.  In the **CAM System Properties** page, select **Enable CAM workflow configuration**.

3.  In the **Enable CAM Workflow Configuration** pop-up, read the impact listed under **Turning this property on will update your CAM experience**.

    The impacts to the CAM experience when you enable the CAM workflow configuration.

    -   Your current homepage widgets and layout will change.
    -   Existing package flows may not work until data-migration is done.
    -   Any custom workflow changes will need to be managed separately.
    -   New boundaries and packages will not be affected.
    -   Once enabled, this property cannot be turned off.
4.  Select **I will run the data migration script to complete the setup** option to confirm you’ll migrate existing data after enabling the workflow configuration.

    The Confirm button is enabled only after you select this checkbox. If you select Cancel or do not select the checkbox, the property remains disabled.

5.  Select **Confirm** to enable the property.

6.  Select **Save** to save the system properties.


## What to do next

To proceed with data migration, select **Script for migrating data to cam workflow configurator** link under the **Enable CAM workflow configuration** option.

This link is available at all times, even after the property is enabled, so you can run migration when required.

See [Run migration scheduled job](run-migration-scheduled-job.md) from Step 4 for detailed migration steps.

