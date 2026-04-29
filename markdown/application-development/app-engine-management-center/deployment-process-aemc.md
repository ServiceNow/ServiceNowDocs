---
title: Deployment process in AEMC
description: Learn about the deployment process in AEMC.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: concept
last_updated: "2025-08-08"
reading_time_minutes: 6
breadcrumb: [Explore, App Engine Management Center, Governing app development, Building applications]
---

# Deployment process in AEMC

Learn about the deployment process in AEMC.

## Deployment overview

The deployment process in AEMC is made up of several parts that make deploying changes possible. The following sections describe each part and how they work together to support the larger deployment process within AEMC.

Starting with version 28.2.1 of AEMC, ReleaseOps is integrated into AEMC. See the ReleaseOps deployment section for more information.

## Submitting an application for deployment

The deployment process begins on a development instance when a developer submits an application in App Engine Studio, Creator Studio, or ServiceNow Studio. When an application is submitted for deployment, a deployment request is created, which enables admins to review and approve the application changes. For more information, see [Deployment requests in AEMC](deployment-requests-aemc.md).

## Pipelines

Once an application has been submitted and a deployment request has been created, the application then begins to move through the pipeline that has been specified for the organization. A pipeline is the deployment structure that applications follow within AEMC. A pipeline consists of several instances, typically a development instance, test instance, and production instance, as well as the testing suites and frameworks that an organization has set up to verify that the application is stable and compatible before deploying to production. As the application is reviewed and tested, App Engine admins approve the application to move through pipeline environments until the application is finally deployed to a production or target instance.

With AEMC, you can configure pipelines that are tailored to the specific needs of your organization. AEMC supports any number of instances within each pipeline and as many pipelines as are needed for your organization. For example, if your organization requires that changes move through additional non-production instances prior to deploying to production, you can configure your pipeline so that it reflects each environment that you need. For more information about configuring pipelines, see [Configure Pipelines and Deployments](../../pipelines-and-deployments/task/config-p-and-d.md).

## Change Management integration

You can integrate an existing Change Management program with your app deployment processes to add oversight into your deployments and have apps deploy according to a scheduled Change window. For more information, see [Manage deployment requests](../../app-engine-studio/task/manage-deployment-requests.md).

## Application Repository

AEMC uses Pipelines and Deployments to deploy applications through different instances. Pipelines and Deployments uses the Application Repository to manage these deployments. For more information about the Application Repository, see [ServiceNow application repository](../../applications/concept/app-repo.md).

Each application can either be deployed using the Application Repository or System Update Sets. If you have used update sets in the past, but want to switch to using the Application Repository, you can do a one-time conversion to deploy the app using the Application Repository instead. All apps don't have to follow the same deployment. For more information, see [Convert custom applications to upgrade from the application repository](../../applications/task/convert-custom-app-to-update-app-repo.md) and [System update sets](../../system-update-sets/concept/system-update-sets.md).

## ReleaseOps deployment process

Starting with version 28.2.1 of AEMC, ReleaseOps is integrated into AEMC. Whether you are exclusively using ReleaseOps to manage your deployments, or you have migrated your App Engine pipelines to ReleaseOps, the deployment process differs from the legacy Pipelines and Deployments deployment process in AEMC.

If you are deploying exclusively using ReleaseOps, the deployment process for a scheduled release is as follows. is as follows:

1.  The release manager creates a release, which is associated with a pipeline.
2.  Developers make changes through update sets. Once they mark an update set **Complete** and promote the update set for deployment, the update set is added to an existing deployment request or to a new deployment request, which is targeted to a release.
3.  When the update sets within a deployment request are functional and ready to be deployed, a developer sets the deployment request state to the Ready to Assess.
4.  The assessment playbook runs, during which Automated Test Framework \(ATF\) test suites and instance scans are run on the changes in the deployment request.
5.  If there are failures during assessment, deployment tasks are created that the tester can sign off on or redirect to the developer to address.
6.  Once the deployment tasks have been addressed, the deployment request is set to the Ready for Deployment state.
7.  On the scheduled date for the release, the release playbook runs. All deployment requests in the Ready for Deployment state move through the pipeline to production.

For more information about deploying with ReleaseOps, see [Exploring ReleaseOps](../../release-ops/concept/exploring-release-ops.md).

If you have migrated to ReleaseOps, the deployment process is as follows.

1.  For applications being deployed via the Application Repository, developers submit applications from App Engine Studio, Creator Studio, and ServiceNow Studio using the standard process.
2.  An App Engine deployment request is created and sent to an App Engine admin for approval. At the same time, a corresponding ReleaseOps deployment request is created.

    You can view the corresponding ReleaseOps deployment request record on the App Engine deployment request.

    ![With migration enabled, App Engine deployment requests have corresponding ReleaseOps deployment request records.](../image/aemc-dr-with-releaseops-dr.png)

3.  Open the corresponding ReleaseOps deployment request and either attach it to an existing release or set the deployment request to on-demand. Then save the record.
4.  An App Engine admin approves the App Engine deployment request from the App Engine pipeline, which hands off deployment to ReleaseOps.
5.  An update set with install instructions is created and attached to the ReleaseOps deployment request.
6.  Deployment requests in both the App Engine and ReleaseOps pipelines are synced, but ReleaseOps orchestrates the deployment.

To learn more about migrating to ReleaseOps, see:

-   [Migrating App Engine pipelines to ReleaseOps](migrating-ae-pipelines-to-releaseops-aemc.md)
-   [Migration tasks](migration-tasks-aemc.md)

