---
title: Add ATF and instance scan suites for testing
description: Add your customized test suites as part of an application deployment in addition to the instance scan and Automated Test Framework \(ATF\) testing suites that are standard in AEMC.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Pipelines and Deployments configuration tasks, Configure Pipelines and Deployments, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
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


**Parent Topic:**[Pipelines and Deployments configuration tasks](../../pipelines-and-deployments/reference/p-and-d-config-tasks.md)

