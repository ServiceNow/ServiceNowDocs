---
title: Testing applications in AEMC
description: Testing an application helps to ensure the viability of the changes on the production instance. Learn about how testing works in AEMC and the different kinds of tests that automatically run during the deployment process.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: concept
last_updated: "2025-08-08"
reading_time_minutes: 2
breadcrumb: [Explore, App Engine Management Center, Governing app development, Building applications]
---

# Testing applications in AEMC

Testing an application helps to ensure the viability of the changes on the production instance. Learn about how testing works in AEMC and the different kinds of tests that automatically run during the deployment process.

## Testing an application

Before you publish a submitted application, test it in a non-production instance. To begin testing, an admin must open the deployment request and select **Approve**. The pipeline record is read and determines the next state for the request.

The goal of testing the application is to ensure the viability of the production instance. When the app has transitioned to the Testing state, ServiceNow Automated Test Framework tests run if you have [enabled the appropriate properties](../../pipelines-and-deployments/task/enable-atf-properties.md).

If the application doesn't pass testing, then you reject the deployment request.

## Deploying to a test environment

When you deploy or install an application to a test environment, two jobs are automatically executed:

-   Application Deployment Test Suite
-   Scoped App Definitions instance scan

These tests can be useful to the administrator for diagnosing issues before an app is deployed.For more information about what goes on during an application deployment, see [Pipelines and Deployments workflow version 24.1.2](../../pipelines-and-deployments/concept/pipelines-deployments-workflow-vs2.md).

<table id="table_ojh_znc_5rb"><thead><tr><th>

Job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application Deployment Test Suite

</td><td>

A set of Automated Test Framework \(ATF\) tests. The suite consists of a single test called **Log**. When the test is run, scan results are logged to the Test Results \[sys\_atf\_test\_result\] table.**Note:** The following two system properties must be enabled to run the Application Deployment Test Suite:

-   sn\_atf.runner.enabled
-   sn\_atf.schedule.enabled

If they aren't enabled, only the instance scan runs. For more information, see [Enable Automated Test Framework \(ATF\) properties](../../pipelines-and-deployments/task/enable-atf-properties.md).

</td></tr><tr><td>

Scoped App Definitions instance scan

</td><td>

Instance scans aid in diagnosing health issues on a non-production instance, and are useful for addressing best practices. For more information, see [Instance Scan](https://www.servicenow.com/docs/access?context=hs-landing-page&version=australia&pubname=australia-platform-administration&ft:locale=en-US).The instance scan checks all tables in the app that extend Task \[task\].

</td></tr></tbody>
</table>The admin can view the results of the scans for troubleshooting purposes by selecting the **Deployment Environment Results** tab in the deployment request.

Simply open the record of the instance. The results are split into three tabs:

-   **ATF Results**
    -   Test suite name
    -   Test URL
    -   Success and failure counts
    -   Overall error count
-   **Instance Scan Results**
    -   Scan suite name
    -   Scan URL
    -   Finding count for the scan
-   **Results \(JSON\)** includes unformatted JSON code of the ATF and instance scan results, as well as any errors identified during the scans. This JSON can also be found in the **Notes** related list.

