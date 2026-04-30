---
title: Run health scans for DevOps Change Velocity
description: Run health check scans on your DevOps Change Velocity instance and get recommendations on fixing any errors that might exist.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Run health scans for DevOps Change Velocity

Run health check scans on your DevOps Change Velocity instance and get recommendations on fixing any errors that might exist.

## Before you begin

Role required: sn\_devops.admin

Activate the DevOps Change Health Scan Content Pack application to use this feature. For information on activating a plugin, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## About this task

If you are in version \(3.0 to 5.0\) of DevOps Change Velocity, but you have activated the DevOps Change Health Scan Content Pack application, you can access this feature only from the Classic UI in the ServiceNow AI Platform. For more information on health scans in ServiceNow AI Platform, see [Scan checks](https://www.servicenow.com/docs/access?context=scan-checks&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

Scan suites are collections of security center checks that execute together. The DevOps Change Velocity Health parent suite contains the DevOps Change Velocity Health - Scheduled and DevOps Change Velocity Health - On-demand suites within it.

You can choose to run the DevOps Change Velocity Health parent scan, which executes all the checks available in the DevOps suite of scans or run each child suite individually which executes the checks applicable to that child suite. Using the DevOps Change Velocity Health - Scheduled child suite, you can create a schedule to regularly trigger DevOps Health instance suite scans even when you don’t have an active session. And using the DevOps Change Velocity Health - On-demand suite, you can run the available DevOps Health scan checks on a specific target to obtain focused scan results.

You can also choose to navigate to the Checks list, and run a specific health check scan directly by selecting the check and then selecting **Test Check**. The following checks are available in the DevOps suite.

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace**.

2.  In the Lists module, select **Health scans** &gt; **Suites**.

3.  Select any of the scan suites based on your requirement.

4.  Select **Execute suite scan**.

    For information on the scans available for the DevOps suite, see [DevOps Change Velocity suite health scan checks](../reference/devops-change-velocity-suite-health-scan-checks.md).


## Result

Once the scan is executed, you can view the results and findings of the scan in the Results and Findings lists respectively. You can navigate to the Findings list from the DevOps Change Workspace home page also by selecting **View all findings** in the **Health scan findings** widget. You can navigate to a specific scan finding or check as well from the **Health scan findings** widget. To navigate to a specific scan finding, select the required value in the **Created** column, and to navigate to a specific check, select a value in the **Check** column. The DevOps Change Health Scan Content Pack application must be activated to view data in the **Health scan findings** widget in the home page.

A scan result reports the status and type of the scan. You can also see all the checks that ran as part of the scan and all other information related to the scan such as errors and scan logs. A finding is a reference to a record that has violated a rule from a check on the instance. You can find the source record and the number of times the record triggered the rules of a given check.

**Related topics**  


[DevOps Change Velocity suite health scan checks](../reference/devops-change-velocity-suite-health-scan-checks.md)

