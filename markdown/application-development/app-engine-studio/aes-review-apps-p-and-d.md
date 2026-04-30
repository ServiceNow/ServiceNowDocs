---
title: Managing app deployments using Pipelines and Deployments
description: Review the applications developers build using App Engine Studio \(AES\) so you can deploy with confidence.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Managing app deployments using Pipelines and Deployments

Review the applications developers build using App Engine Studio \(AES\) so you can deploy with confidence.

## Deployment requests

After a developer submits an application in App Engine Studio, a deployment request is created. A deployment request is a record to track the review of submitted applications.

A reviewer can deploy the app to your test environment, reject it, or publish it, all using the App Engine Management Center. If you integrate an existing Change Management program with AEMC, and your app is ready to deploy to production, you can create a change request and deploy the app within a specified change window.

![Deployment request in App Engine Management Center](../image/deployment-record-vs2.png "Deployment request")

1.  View details of the deployment request and the application being deployed.
2.  Select **Approve &amp; Create Change Request** when the app is ready for deployment. This action begins the Change Management processes you configure using Guided Setup.

    **Note:** If you don't have an existing Change Management program integrated with Pipelines and Deployments, select **Approve &amp; Deploy App** to move the deployment to the next stage.

3.  View and edit details of the deployment on the **Scheduled Deployments** tab.
4.  View details of the change request on the **Change Request** tab. Depending on the role you have, you may be able to change some details of the request.
5.  Watch the **Activity** stream for test results, change request progress, and other deployment details.

**Note:** If you submit deployment requests without upgrading all instances in the pipeline, your existing pipeline continues to be used.

For more information on reviewing a deployment request, see [Deployment Request form in the Pipelines and Deployments app](../reference/deployment-req-form-d-and-p.md).

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

Instance scans aid in diagnosing health issues on a non-production instance, and are useful for addressing best practices. For more information, see [Instance Scan](https://www.servicenow.com/docs/access?context=hs-landing-page&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).The instance scan checks all tables in the app that extend Task \[task\].

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

## Publishing an application

If an application passes testing, open the deployment request and deploy the application to your production environment. It is then available to all employees in your organization. For more information, see [Managing deployments using pipelines in AEMC](manage-deployments-using-aemc.md#).

## Guides for more information

If you need more information, you can try these external guides sponsored by ServiceNow.

<table id="table_m51_zrm_jtb"><thead><tr><th>

Learn more about Pipelines and Deployments

</th><th>

Additional ServiceNow resources

</th></tr></thead><tbody><tr><td rowspan="2">

The Pipelines and Deployments app is used to deploy the apps you are creating using App Engine Studio between instances in a pre-defined order. Unlike previous versions, Pipelines and Deployments allows you to deploy your apps to an unlimited number of instances for app creation, testing, staging, and production.

</td><td>

![](../../../reuse/icons/brand-icons/bus-webinar.svg) [Promoting apps through the AES pipeline](https://youtu.be/pUklspebh2w)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-video-play.svg) [Create apps fast with App Engine Studio](https://www.youtube.com/watch?v=kQ8jjcsPf4M&t=19s)

</td></tr></tbody>
</table>-   **[Pipelines and Deployments workflow version 24.1.2](../../pipelines-and-deployments/concept/pipelines-deployments-workflow-vs2.md)**  
As you manage requests for app deployment in App Engine Management Center \(AEMC\), use this workflow to understand how app deployments move through your pipelines in version 24.1.2, released in November 2023.

**Parent Topic:**[Build apps using App Engine Studio](aes-overview.md)

