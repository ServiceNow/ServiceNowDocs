---
title: Exploring ReleaseOps
description: ServiceNow ReleaseOps is a solution to problem of deploying changes, customizations, and custom apps on the ServiceNow AI Platform. By automating the deployment process, ReleaseOps helps to increase the predictability and reliability of deployments, while also reducing the risk of releasing unwanted changes to production.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/releaseops/exploring-release-ops.html
release: zurich
product: ReleaseOps
classification: releaseops
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 5
keywords: [ReleaseOps, deploy changes, update sets, pipeline, ATF, schedule a release, deployment request, deployment analyzer]
breadcrumb: [ReleaseOps, Deploying applications, Building applications]
---

# Exploring ReleaseOps

ServiceNow® ReleaseOps is a solution to problem of deploying changes, customizations, and custom apps on the ServiceNow AI Platform. By automating the deployment process, ReleaseOps helps to increase the predictability and reliability of deployments, while also reducing the risk of releasing unwanted changes to production.

## ReleaseOps overview

ReleaseOps automates and enhances the process of deploying changes, customizations, and custom applications on the ServiceNow AI Platform. ReleaseOps improves upon the existing pipelines deployment process by internally managing cross-instance trust and credential sharing, simplifying the setup and configuration of custom pipelines. ReleaseOps enables you to deploy changes using update sets and trigger deployment from directly within the ServiceNow Studio development environment. In addition, ReleaseOps leverages the automation capabilities of the ServiceNow Playbooks, resulting in deployments that are less error-prone and manual.

ReleaseOps handles deployments through releases. Releases define which changes, customizations, or custom apps will be moved to the production \(or target\) instance and when the changes will be deployed. The changes within a release are contained in deployment requests. Each deployment request contains one or more update sets or application installs. For more information about releases and deployment requests, see [Releases in ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/releaseops/releases-in-release-ops.md) and [Deployment requests in ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/releaseops/deployment-requests.md).

## ReleaseOps availability

ReleaseOps is not supported in regulated environments or on-premise. Check your entitlements to determine whether you have access to ReleaseOps.

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

A developer is responsible for creating deployment requests to push application installations or update sets of work completed through the pipeline.

</td></tr><tr><td>

Tester

</td><td>

A tester is responsible for signing off on ATF test failures that occur to enable a deployment to continue. A tester can also send it back to development.

</td></tr></tbody>
</table>## ReleaseOps workflow

The following workflow illustrates the sample pipeline workflow installed with ReleaseOps. Your pipeline manager can customize it as needed.

\[Omitted image "releaseops-sample-pipeline-workflow-MMASSET0021906.png"\] Alt text: Flowchart demonstrating the sample pipeline workflow, as the changes in a release are assessed during the assessment playbook stage.

In the traditional development to test to production workflow:

1.  The release manager creates a release, which is associated with a pipeline.
2.  Developers create and promote update sets, adding them to an existing deployment request or create a new deployment request, which is targeted to a release.
3.  The release moves through the pipeline:
    -   The assessment stage moves changes in from deployment requests through non-production instances and is designed to do deployment analysis and run scans and tests.
    -   If there are assessment failures, deployment tasks are created that the Tester can sign off on or redirect to the developer to address.
    -   The release stage moves all changes across its deployment requests that have passed assessment by the scheduled date to production. See sample release workflow, below.

\[Omitted image "releaseops-sample-release-workflow.png"\] Alt text: Diagram showing the progression of a release, from creation through freeze date, preparation, release date, commit, and final deployment.

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
|Define requirements for an application or update to get installed on a target instance.|[Pipelines in ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/releaseops/releaseops-pipeline-environments.md)|Pipeline Manager|
|Deploy changes to a production or another target environment.|[Releases in ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/releaseops/releases-in-release-ops.md)|Release Manager|
|Push application installations or update sets of work completed through the pipeline with deployment requests.|[Deployment requests in ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/releaseops/deployment-requests.md)|Developer|
|Scan deployment requests for changes to the current state of the production instance or target instance with the deployment analyzer. Use those findings to determine your actions in the pipeline.|[Deployment analyzer in ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/releaseops/deployment-analyzer.md)|Developer|

## What to explore next

To learn more about configuring and using ReleaseOps, see:

-   [Configuring ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/releaseops/configuring-releaseops.md)
-   [Using ReleaseOps to manage deployments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/releaseops/using-releaseops-to-manage-deployments.md)
-   [Promote an update set for deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/releaseops/promote-update-set-for-deployment.md)
-   [Create a deployment request for a scheduled release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/releaseops/create-a-new-deployment-request.md)
-   [Create a deployment request for an on-demand release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/releaseops/create-a-deployment-request-for-on-demand-release.md)
-   [Attach an update set to an existing deployment request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/releaseops/attach-an-update-set-to-existing-deployment-request.md)
-   [Create a release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/releaseops/create-a-release.md)

