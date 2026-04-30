---
title: Run health scans for DevOps Change Velocity
description: Run health check scans on your DevOps Change Velocity instance and get recommendations on fixing any errors that might exist.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Run health scans for DevOps Change Velocity

Run health check scans on your DevOps Change Velocity instance and get recommendations on fixing any errors that might exist.

## Before you begin

Role required: sn\_devops.admin

Activate the DevOps Change Health Scan Content Pack application to use this feature. For information on activating a plugin, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## About this task

If you are in version \(3.0 to 5.0\) of DevOps Change Velocity, but you have activated the DevOps Change Health Scan Content Pack application, you can access this feature only from the Classic UI in the ServiceNow AI Platform. For more information on health scans in ServiceNow AI Platform, see [Scan checks](https://www.servicenow.com/docs/access?context=scan-checks&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

Scan suites are collections of security center checks that execute together. The DevOps Change Velocity Health parent suite contains the DevOps Change Velocity Health - Scheduled and DevOps Change Velocity Health - On-demand suites within it.

You can choose to run the DevOps Change Velocity Health parent scan, which executes all the checks available in the DevOps suite of scans or run each child suite individually which executes the checks applicable to that child suite. Using the DevOps Change Velocity Health - Scheduled child suite, you can create a schedule to regularly trigger DevOps Health instance suite scans even when you don’t have an active session. And using the DevOps Change Velocity Health - On-demand suite, you can run the available DevOps Health scan checks on a specific target to obtain focused scan results.

You can also choose to navigate to the Checks list, and run a specific health check scan directly by selecting the check and then selecting **Test Check**. The following checks are available in the DevOps suite.

|Suite name|Check name|Check description|Resolution details|
|----------|----------|-----------------|------------------|
|DevOps Change Velocity Health - Scheduled|DevOps - subflows frequently exceeding execution timeouts|DevOps capability handler subflows have a default time out limit of 45 seconds in the base system. Under normal operating conditions, these timeouts aren’t exceeded. When multiple subflows are timing out frequently, it indicates a potential issue.|Increase the timeout value for the subflow that is timing out, in the Integration Capability table. You must have the DevOps Admin role to perform this action.|
|DevOps Change Velocity Health - Scheduled|DevOps - empty roles in the base system|If any of your base system roles have an empty role reference, it could impact a wide range of DevOps functionality, including the Discover action and event processing.|See the \[[KB1642669](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1642669)\] article for resolution details.|
|DevOps Change Velocity Health - Scheduled|DevOps - duplicate pipelines|The DevOps data model doesn't enforce uniqueness on key records like pipelines, which can lead to intermittent or unpredictable issues. This check identifies duplicate pipeline records in primary DevOps tables, which could cause processing problems if not addressed.|Delete the duplicate pipeline that does not have any associated pipeline executions or is not linked to an app.|
|DevOps Change Velocity Health - Scheduled|DevOps System user access|The devops.system user is used for most server side transaction processing, and in the course of that processing if it cannot access certain key tables the process will fail. Because it's not practical to verify if the user has appropriate access every time it makes a query, the failures tend to manifest indirectly, making them hard and time consuming to diagnose. This check will ensure the devops.system has appropriate access to a specific list of tables required for core product functionality.|Make sure DevOps System user exists. Ensure there are no field level ACLs on sys\_connection and credential table|
|DevOps Change Velocity Health - Scheduled|DevOps - related plugins compatibility|If the plugin versions for applications associated with DevOps Change Velocity are not compatible with the DevOps Change Velocity version in an instance, it might result in various features not functioning correctly. This check identifies if any plugin starting with the name "sn\_devops"\(excluding the sn\_devops\_pipeline plugin\) does not have same version as that of sn\_devops\_chgvlcty.|Upgrade the related plugins to the version compatible with DevOps Change Velocity.|
|DevOps Change Velocity Health - Scheduled|DevOps - chronically failing or waiting pipelines|If a pipeline is chronically failing or in the waiting state indefinitely, it might cause the DevOps processes to not proceed further. This check identifies pipelines that have failed for the previous ten executions, so that you can take remedial action.|Verify the most recent executions for the pipelines flagged, and investigate inbound events and DevOps error logs tables to help determine the root cause for the failures.|
|DevOps Change Velocity Health - On-demand|DevOps - incorrectly configured module access policies|If there are missing or incorrectly configured module access policies in your instance, it could impact a wide range of DevOps functionality, including tool connectivity, event processing, pipeline processing, and change creation. Auto-generated module access policies are set to reject by default. This check identifies the module access policies that are configured with the reject result state.|Set the result value of the module access policy for the DevOps application to "Track' to allow the DevOps application to access the credentials. See the \[[KB1112530](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1112530)\] KB article for more details.|
|DevOps Change Velocity Health - On-demand|DevOps - change control steps with untracked pipelines|If a pipeline has change control enabled but it is not marked for tracking, a change request might not get created when it is run, and the pipeline may get stuck.|Enable tracking for pipelines under change control by selecting the Track option in the tool record page or add the pipeline to an app.|
|DevOps Change Velocity Health - On-demand|DevOps - Jenkins plugin compatibility|If the Jenkins plugin version installed in your instance is not compatible with the DevOps Change Velocity version, it might result in Jenkins features not functioning correctly.|Upgrade your Jenkins plugin to the version compatible with DevOps Change Velocity.|
|DevOps Change Velocity Health - On-demand|DevOps – changes in update set records|If there are modifications in any of the DevOps applications, it could potentially result in updates being skipped or overlooked when upgrading to a newer version. This check scans the update.xml file for DevOps Change Velocity scoped changes.|Before working with update sets, create a standard process for moving customizations. For more information, see the [Get started with update sets](https://www.servicenow.com/docs/access?context=get-started-update-sets&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) topic in product documentation.|
|DevOps Change Velocity Health - On-demand|DevOps - files skipped during upgrade|If any file was skipped during the upgrade process, it could lead to potential issues or an unstable application state. Proactively addressing missing files ensures the upgrade's integrity and prevents unexpected errors or failures.|Manually merge the new updates for the skipped files. See the KB article \[[KB0952456](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0952456)\] for more information.|

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace**.

2.  In the Lists module, select **Health scans** &gt; **Suites**.

3.  Select any of the scan suites based on your requirement.

4.  Select **Execute suite scan**.


## Result

Once the scan is executed, you can view the results and findings of the scan in the Results and Findings lists respectively. A scan result reports the status and type of the scan. You can also see all the checks that ran as part of the scan and all other information related to the scan such as errors and scan logs. A finding is a reference to a record that has violated a rule from a check on the instance. You can find the source record and the number of times the record triggered the rules of a given check.

