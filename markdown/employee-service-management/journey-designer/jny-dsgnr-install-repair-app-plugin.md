---
title: Add or repair demo data for applications and plugins
description: If the demo data wasn’t added during the initial installation, administrators can add demo data to a plugin using Repair install.
locale: en-US
release: zurich
product: Journey Designer
classification: journey-designer
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Add or repair demo data for applications and plugins

If the demo data wasn’t added during the initial installation, administrators can add demo data to a plugin using **Repair** install.

## Before you begin

Role required: admin or sn\_appclient.app\_client\_company\_installer

## About this task

Any demo data from installed dependent applications must be updated when Journey designer is updated. You can view which store applications are installed from the **Journey designer Admin Console**, see. [Configure Journey designer features](../concept/jny-dsgnr-configuration.md).

Run a repair installation on a plugin to add demo data or fix an issue that the plugin is experiencing.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Find the plugin or application that you want to add demo data to and select the more icon \(vertical eclipses\).

3.  Select **Repair**.

4.  Select the check box for **Load demo data**.

5.  Select **Repair**.

6.  Select **View Log** to view and confirm that the demo data was added.

    **Note:** Sort the **Created** column in descending order to see the latest log entries first.

    Example Log:

    ```
    Loading onload_demo_data plugin script: com.sn_hr_lifecycle_ent/sys.scripts/generate_onboarding_cases.js
    ```


**Parent Topic:**[Installation and configuration overview](../concept/jny-inst-config-overview.md)

