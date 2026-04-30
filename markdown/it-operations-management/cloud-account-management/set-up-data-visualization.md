---
title: Set up scan configuration for data visualization
description: Visualize all account violations by scanning them using the selected policy set. Display the severity of all violations on the admin dashboard to take appropriate actions.
locale: en-US
release: yokohama
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2024-08-25"
reading_time_minutes: 1
breadcrumb: [Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up scan configuration for data visualization

Visualize all account violations by scanning them using the selected policy set. Display the severity of all violations on the admin dashboard to take appropriate actions.

## Before you begin

Make sure you have referred to the default policies \([Policy list for scanning cloud accounts](../reference/policies-for-scanning-cloud-accounts.md)\). To create a custom policy set, see [Create a policy set](../../itom-cloud-accelerate/task/create-ccg-policy-set.md).

Role required: sn\_itom\_cam.cw\_admin or sn\_itom\_ccg.scheduling\_admin

## Procedure

1.  Navigate to **All** &gt; **Cloud Configuration Governance** &gt; **Scan Configurations**.

2.  Create a scan configuration by selecting **New**.

3.  Identify the configuration by entering `Name` and `Description`.

4.  Under the **Configuration** tab, select a **Cloud Provider Type** from the lookup.

5.  Select the **Unlock Policy Sets** icon \(![Lock](../image/unlock_icon.png)\) and select a policy set from the list.

6.  Select the **Lock Policy Sets** icon \(![Unlock](../image/lock_icon.png)\).

7.  Select and hold \(or right-click\) on the top bar and select **Save** to save the current settings.

    ![Save Cloud Configuration Governance Scan Configuration](../image/save-scan-config.png)

8.  Under the **Service Account** column, select all the management accounts and member accounts from the lookup.

    **Note:** Selecting a management account scans all current and future member accounts automatically. Choosing individual member accounts requires manual selection for each scan.

9.  Select **Setup Schedule** and set the schedule as necessary.

10. Select **Update**.

11. Synchronize the configuration with the Cloud Account Management app by selecting **Sync CAM Config**.![Sync Cloud Account Management Config button on the Scan Configuration page](../image/sync_CAM_config.png)

    **Note:**

    -   To view the synchronized configuration, navigate to **All** &gt; **Cloud Workspace** &gt; **Configuration**.
    -   If you have synchronized the configuration, you don’t have to create a Scan Account configuration mentioned in [Create a scan account configuration](create-scan-account-config.md).
12. To run an on-demand scan, select **Execute**.

    **Note:** You can create unlimited configurations for each account. An account may have multiple scan configurations, with violations and assessments based on all of them.


