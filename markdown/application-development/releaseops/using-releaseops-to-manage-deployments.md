---
title: Using ReleaseOps to manage deployments
description: Use ReleaseOps to automate the process of managing your releases and deploying changes to a target instance.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [ReleaseOps, deploy changes, update sets, pipeline, ATF, schedule a release, deployment request, deployment analyzer]
breadcrumb: [ReleaseOps, Deploying applications, Building applications]
---

# Using ReleaseOps to manage deployments

Use ReleaseOps to automate the process of managing your releases and deploying changes to a target instance.

ReleaseOps leverages the automation capabilities of the ServiceNow AI Platform to streamline deployments through a pipeline, empowering teams to manage releases and deploy changes with greater confidence. ReleaseOps enables you to promote changes for deployment easily. Once your changes are promoted for deployment, you can create a deployment request that's tailored to the needs of your release, either scheduled or on-demand. ReleaseOps automates the process of verifying and testing deployment requests, helping to ensure that changes are stable for deployment to target instances. Once the changes are verified and tested, the changes are released to a target instance, often a production instance, automatically.

To learn more about the different components of a ReleaseOps release and the ReleaseOps deployment process, see [Exploring ReleaseOps](exploring-release-ops.md).

The following list outlines the tasks that ReleaseOps can help you to accomplish:

-   Release managers can create a release, enabling them to schedule the release date and select which developers and applications the release applies to.
-   Developers can promote changes for deployment.
-   Developers can create deployment requests for scheduled and on-demand releases, which they attach their update set to.
-   Developers can reconcile deployment tasks, enabling deployment requests to proceed through the pipeline.

-   **[Promote an update set for deployment](../task/promote-update-set-for-deployment.md)**  
When you're ready to deploy your changes, promote your update set to begin the deployment process.
-   **[Create a deployment request for a scheduled release](../task/create-a-new-deployment-request.md)**  
Create a deployment request for a scheduled release to contain your update set and enable your changes to move through the pipeline for deployment.
-   **[Create a deployment request for an on-demand release](../task/create-a-deployment-request-for-on-demand-release.md)**  
Create a deployment request for changes that will deployed with an on-demand release.
-   **[Attach an update set to an existing deployment request](../task/attach-an-update-set-to-existing-deployment-request.md)**  
If you want to attach multiple update sets to a deployment request, you can attach an update set to an existing deployment request on the **Deploy an update set** form.
-   **[Create a release](../task/create-a-release.md)**  
Specify the details for your release, including the target instance that the changes will be deployed to and when the release should occur.
-   **[Create a runbook task](../task/create-runbook-task.md)**  
Create a runbook task to pause deployment and define the steps required to proceed.
-   **[Reconcile a deployment task](../task/reconcile-deployment-task.md)**  
Reconcile a deployment task to enable a deployment request to move to the next stage in deployment.

**Parent Topic:**[ReleaseOps](releaseops-landing.md)

