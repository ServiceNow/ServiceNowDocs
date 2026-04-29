---
title: Add ATF and instance scan suites for testing
description: Add your customized test suites as part of an application deployment in addition to the instance scan and Automated Test Framework \(ATF\) testing suites that are standard in AEMC.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration tasks, Configure Pipelines and Deployments, Configure, App Engine Management Center, Governing app development, Building applications]
---

# Add ATF and instance scan suites for testing

Add your customized test suites as part of an application deployment in addition to the instance scan and Automated Test Framework \(ATF\) testing suites that are standard in AEMC.

## Before you begin

Because the ATF and instance scan suites exist only on testing instances, you must have your pipeline set up to complete this task. For more information, see [Configure your pipeline environments](../../pipelines-and-deployments/task/config-pipeline-environments.md).

Role required: admin

## Procedure

1.  On your production instance, navigate to **All** &gt; **App Engine** &gt; **Pipelines and Deployments** &gt; **Scan Suites**.

2.  If this is the first time you are looking at this table, select **Populate default suites** to load the instance and ATF scan suites that ServiceNow provides.

3.  Add a new scan suite by selecting **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Suite|Table with all the ATF and Instance scan suites that exists on your testing instance.|
    |Error severity|Error options that indicate the severity of a scan suite not passing testing.|
    |Instance Type|Type of instance the scan suite will run on. This field should be set to **Testing**.|

5.  Select **Submit**.

    The suites you add will run on apps installed on the instance you selected during testing.


