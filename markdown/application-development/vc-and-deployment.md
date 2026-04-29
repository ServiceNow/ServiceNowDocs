---
title: Vibe coding, AI-assisted development, and deployment
description: After you generate and expand an app on the ServiceNow AI Platform, the deployment process is tightly integrated into the workflow.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [vibe coding, AI-assisted development, deployment, workflow, collaborative design, AI-driven app development, review and testing, deployment approval, autonomous checks, Git-based source control, update sets, application packaging, scoped applications, CI/CD]
breadcrumb: [Develop, Vibe coding and AI-assisted development, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Vibe coding, AI-assisted development, and deployment

After you generate and expand an app on the ServiceNow AI Platform, the deployment process is tightly integrated into the workflow.

## Workflow for deploying an AI-developed app

After development, review, and testing are complete, a typical deployment workflow includes the following steps:

1.  Collaborative design: Business owners and IT collaborate on requirements and ideas using their preferred tools.
2.  AI-driven app development: Now Assist and Build Agent process files, chat history, and diagrams to generate and implement app updates.
3.  Review and testing: Teams preview updates, make revisions, and run rounds of performance and readiness testing.
4.  Developer review: A developer reviews the AI-generated changes, compares versions, and confirms the changes are ready for deployment.
5.  Deployment approval: The project is handed off to a deployment manager, who initiates the deployment approval process.
6.  Autonomous checks: AI agents automatically scan for issues \(such as sensitive data exposure or model integrity problems\) and remediate them before deployment.
7.  Final deployment: After all readiness scans and approvals, the new app is deployed securely and efficiently.

## Deployment options

Build Agent supports the following deployment methods for vibe-coded and AI-developed apps:

-   Git-based source control integration with ServiceNow IDE: ServiceNow supports Git-based workflows for version control and CI/CD.
    -   You can push scoped apps to Git repositories, enabling branching, merging, and automated deployments. ServiceNow IDE supports bring-your-own Git integration, such as GitHub or Bitbucket.
    -   For more information, see [Integrating source control with the ServiceNow IDE](../../servicenow-ide/concept/integrating-source-control-servicenow-ide.md).
-   Update sets and application packaging: Standard ServiceNow deployment uses System Update Sets to track changes.
    -   Advanced guidance includes packing update sets into scoped applications for easier transport and installation across instances, for example using Application Repository \(AppRepo\).
    -   For more information on System Update Sets, see [System update sets](../../system-update-sets/concept/system-update-sets.md).

## Workflows for moving apps through higher instances

After you create an app using Build Agent, you have several options to move the app to the test instance.

1.  Wrap the entire scoped application in an update set. The workflow is as follows:
    1.  Go to the **Custom Applications** list, select an app and swap to its scope.
    2.  Convert the app to AppRepo.
    3.  Publish the update set with demo data.
    4.  Put the update set in a deployment request for ReleaseOps, or follow your standard update set process for deployment.
2.  Publish the app to AppRepo:
    -   You can use a Git-based process or update sets to publish to AppRepo.
    -   Scoped apps, as well as apps that are ready for testing, can be published to the AppRepo for distribution across environments.
    -   After an app is in AppRepo, you can move it through a ReleaseOps pipeline. If ATF tests are included in the pipeline, they automatically run.
    -   Register and entitle apps before publishing.
    -   For more information on Application Repository, see [ServiceNow application repository](../../applications/concept/app-repo.md).

## Additional deployment tools and capabilities

The ServiceNow AI Platform has additional deployment tools that include the following tools:

-   App Engine Management Center \(AEMC\):
    -   After developing an app, submit it to AEMC for governance checks.
    -   AEMC validates ACLs, roles, and compliance settings before deployment.
    -   Use ReleaseOps pipelines to move apps through environments with ATF tests and approval gates.
    -   AEMC provides dashboards for monitoring deployments and managing app versions throughout the lifecycle.
    -   For more information on AEMC, see [Using the App Engine Management Center](../../app-engine-studio/concept/monitor-requests-using-aemc.md).
-   ReleaseOps:
    -   Move changes from development to production through multiple instances using customizable playbooks.
    -   Automate preview, commit, and validation of update sets before deployment.
    -   Run Automated Test Framework \(ATF\) tests as part of the pipeline to validate quality.
    -   Deploy changes immediately or schedule releases for controlled rollouts.
    -   Enforce checks, scans, and approvals before production deployment.
    -   For more information on ReleaseOps, see [ReleaseOps](../../release-ops/concept/releaseops-landing.md).
-   ServiceNow SDK:
    -   Use the ServiceNow SDK to move applications to and from your instance to your local machine. You can integrate the ServiceNow SDK with your off-instance CI/CD process if you have one.
    -   Install the ServiceNow SDK locally and use the command line interface \(CLI\).
    -   Authenticate to a ServiceNow instance from the ServiceNow SDK.
    -   Push to or install an application on the authenticated instance from your local environment.
-   Automated Test Framework \(ATF\)
    -   Tests can be generated by Build Agent and executed in ServiceNow Studio or ServiceNow IDE to confirm functionality after changes.
    -   For more information on ATF, see [Automated Test Framework \(ATF\)](../../../administer/auto-test-framework/concept/atf-landing-page.md).

**Parent Topic:**[Vibe coding and AI-assisted development on the ServiceNow AI Platform](vibe-coding-using.md)

