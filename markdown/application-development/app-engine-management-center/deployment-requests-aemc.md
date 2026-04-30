---
title: Deployment requests in AEMC
description: AEMC enables you to deploy changes to production through deployment requests. Learn more about what deployment requests are and where to view them in AEMC. Starting with version 28.2.1 of AEMC, you can also manage ReleaseOps deployment requests from AEMC.
locale: en-US
release: zurich
product: App Engine Management Center
classification: app-engine-management-center
topic_type: concept
last_updated: "2025-08-08"
reading_time_minutes: 2
breadcrumb: [Explore, App Engine Management Center, Governing app development, Building applications]
---

# Deployment requests in AEMC

AEMC enables you to deploy changes to production through deployment requests. Learn more about what deployment requests are and where to view them in AEMC. Starting with version 28.2.1 of AEMC, you can also manage ReleaseOps deployment requests from AEMC.

## App Engine deployment requests

The following information applies to App Engine deployment requests. For information about ReleaseOps deployment requests, see the ReleaseOps deployment requests section.

When a developer submits an application in App Engine Studio, Creator Studio, or ServiceNow Studio, a deployment request is created. A deployment request is a record to track the review of submitted applications.

A reviewer can deploy the app to a test environment, reject it, or publish it, all using the App Engine Management Center. If you integrate an existing Change Management program with AEMC, and your app is ready to deploy to production, you can create a change request and deploy the app within a specified change window.

1.  View details of the deployment request and the application being deployed.
2.  Select **Approve &amp; Create Change Request** when the app is ready for deployment. This action begins the Change Management processes that you configure using Guided Setup.

    **Note:** If you don't have an existing Change Management program integrated with Pipelines and Deployments, select **Approve &amp; Deploy App** to move the deployment to the next stage.

3.  View and edit details of the deployment on the **Scheduled Deployments** tab.
4.  View details of the change request on the **Change Request** tab. Depending on the role you have, you may be able to change some details of the request.
5.  Watch the **Activity** stream for test results, change request progress, and other deployment details.

**Note:** If you submit deployment requests without upgrading all instances in the pipeline, your existing pipeline continues to be used.

For more information on reviewing a deployment request, see [Deployment Request form in the Pipelines and Deployments app](../../app-engine-studio/reference/deployment-req-form-d-and-p.md) and [Manage deployment requests](../../app-engine-studio/task/manage-deployment-requests.md).

## ReleaseOps deployment requests

Starting with version 28.2.1 of AEMC, you can also manage ReleaseOps deployment requests from AEMC. ReleaseOps deployment requests are created when deploying using ReleaseOps or when you have migrated an App Engine pipeline to ReleaseOps.

![View of a ReleaseOps deployment request in AEMC, where you can see the changes, deployment request state, Automated Test Framework and Instance Scan test suites, and the associated playbook.](../image/releaseops-deployment-request.png "ReleaseOps deployment request in AEMC")

A ReleaseOps deployment request references the release the deployment request is associated with. For more information about ReleaseOps releases, see [Releases in ReleaseOps](../../release-ops/concept/releases-in-release-ops.md).

ReleaseOps deployment requests also contain the following information:

-   The update set or update sets with the changes intended to deploy to production
-   Any deployment request tasks, which are generated if a deployment request does not pass the assessment stage
-   The Automated Test Framework \(ATF\) test suites that run during the deployment request assessment
-   The results of the Automated Test Framework \(ATF\) test suites
-   The Instance Scan suites that are run during the deployment request assessment

