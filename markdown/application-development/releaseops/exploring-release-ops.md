---
title: Exploring ReleaseOps
description: ServiceNow ReleaseOps is a solution to the problem of the manual and often error-prone nature of deployment of changes, customizations, and custom apps within the ServiceNow AI Platform.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: concept
last_updated: "2026-04-22"
reading_time_minutes: 5
keywords: [ReleaseOps, deploy changes, update sets, pipeline, ATF, schedule a release, deployment request, deployment analyzer, ServiceNow large scale deployments]
breadcrumb: [ReleaseOps, Deploying applications, Building applications]
---

# Exploring ReleaseOps

ServiceNow® ReleaseOps is a solution to the problem of the manual and often error-prone nature of deployment of changes, customizations, and custom apps within the ServiceNow AI Platform.

## ReleaseOps overview

ReleaseOps automates the deployment of changes across your pipeline, increases predictability and reliability of deployments, and reduces the risk of releasing changes to production. ReleaseOps pipelines are defined in a playbook, enabling you to customize as needed.

Releases are managed within a release object that contains one or more deployment requests. Each deployment request tracks one or more update sets, which can contain application installs.

Releases are managed from your production instance, where the playbook is executed. Actions are orchestrated across instance with a cross-instance communication layer, alleviating credential setup across instances.

## ReleaseOps users

<table id="table_o3d_jq4_zfc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Pipeline manager

</td><td>

A pipeline manager is responsible for creating and managing pipelines, including customizing playbooks. Pipelines define the flow of your deployments.

</td></tr><tr><td>

Release manager

</td><td>

A release manager is responsible for creating and scheduling releases, as well as verifying that the contents of a release are both relevant and correct. The release manager can remove deployment request items that don’t meet the criteria for the release.

</td></tr><tr><td>

Developer

</td><td>

A developer is responsible for creating deployment requests to push application installations or update sets of work through the pipeline.

</td></tr><tr><td>

Tester

</td><td>

A tester is responsible for signing off on ATF test failures that occur to enable a deployment to continue. A tester can also send it back to development.

</td></tr></tbody>
</table>## ReleaseOps workflow

The following workflow illustrates the sample pipeline workflow installed with ReleaseOps. Your pipeline manager can customize it as needed.

![Flowchart showing the ReleaseOps assessment playbook workflow from start to deployment.](../image/releaseops-sample-pipeline-workflow-MMASSET0021906.png "ReleaseOps sample pipeline workflow")

In the traditional development to test to production workflow:

1.  A release manager creates a release, which is associated with a pipeline.
2.  Developers make changes through update sets. Once they mark an update set **Complete** and promote the update set for deployment, the update set is added to an existing deployment request or to a new deployment request, which is targeted to a release.
3.  Developers add runbook tasks to deployment requests to enable custom and manual activities to occur throughout the assessment and release playbook stages.
4.  When the update sets within a deployment request are functional and ready to be deployed, a developer sets the deployment request state to the **Ready to assess**.
5.  The assessment playbook runs, during which Automated Test Framework \(ATF\) test suites and instance scans are run on the changes in the deployment request.
6.  If there are failures during assessment, deployment tasks are created that the tester can sign off on or redirect to the developer to address.
7.  If there are any runbook tasks set to occur during the assessment playbook stage, progression pauses until the runbook tasks have been addressed.
8.  Once the deployment and runbook tasks have been addressed, the deployment request state is set to **Ready for deployment**.
9.  On the scheduled date for the release, the release playbook runs.
10. If there are any runbook tasks set to occur during the release playbook stage, progression pauses until the runbook tasks have been addressed.
11. Once the runbook tasks have been addressed, all deployment requests in the **Ready for deployment** state move through the pipeline to production.

![This infographic displays the sample release workflow.](../image/ro-workflow-2.png "ReleaseOps sample release workflow")

In the traditional release workflow:

1.  A release manager creates a release and sets the state to **Active**.
2.  On the scheduled freeze date, the release begins preparing for deployment.
3.  During the preparation process, deployment requests that aren't ready are set to **Deferred** and can be attached to a future release.
4.  Once preparation is complete, the release state is set to **Ready for deployment**.
5.  When the release date arrives, the update sets within the deployment requests move from test to production in the order that they were deployed in the last instance.
6.  The release and deployment requests are set to **Complete**.

## ReleaseOps benefits

|Benefit|Feature|Role|
|-------|-------|----|
|Define requirements for an application or update to get installed on a target instance.|[Pipelines in ReleaseOps](releaseops-pipeline-environments.md)|Pipeline Manager|
|Deploy changes to a production or another target environment.|[Releases in ReleaseOps](releases-in-release-ops.md)|Release Manager|
|Push application installations or update sets of work completed through the pipeline with deployment requests.|[Deployment requests in ReleaseOps](deployment-requests.md)|Developer|
|Scan deployment requests for changes to the current state of the production instance or target instance with the deployment analyzer. Use those findings to determine your actions in the pipeline.|[Deployment analyzer in ReleaseOps](deployment-analyzer.md)|Developer|
|Leverage Automated Test Framework \(ATF\) code coverage to improve the efficacy of ATF test suites.|[Deployment analyzer in ReleaseOps](deployment-analyzer.md)|Developer|
|Add custom, flexible, and manual activities to your assessment and release playbooks, without having to adjust the structure of your playbooks each time.|[Runbook tasks in ReleaseOps](runbook-tasks.md)|Developer|

## What to explore next

To learn more about configuring and using ReleaseOps, see:

-   [Configuring ReleaseOps](configuring-releaseops.md)
-   [Using ReleaseOps to manage deployments](using-releaseops-to-manage-deployments.md)
-   [Promote an update set for deployment](../task/promote-update-set-for-deployment.md)
-   [Create a deployment request for a scheduled release](../task/create-a-new-deployment-request.md)
-   [Create a deployment request for an on-demand release](../task/create-a-deployment-request-for-on-demand-release.md)
-   [Attach an update set to an existing deployment request](../task/attach-an-update-set-to-existing-deployment-request.md)
-   [Create a release](../task/create-a-release.md)

