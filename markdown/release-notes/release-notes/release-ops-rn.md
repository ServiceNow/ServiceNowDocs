---
title: ReleaseOps release notes
description: The ServiceNow ReleaseOps application enables developers to manage deployments using pipelines and the automation power of playbooks to streamline testing, validating, and releasing changes to production. ReleaseOps is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# ReleaseOps release notes

The ServiceNow® ReleaseOps application enables developers to manage deployments using pipelines and the automation power of playbooks to streamline testing, validating, and releasing changes to production. ReleaseOps is a new application in the Zurich release.

## ReleaseOps highlights for the Zurich release

-   Use ReleaseOps guided setup to simplify initial configuration.
-   Customize ReleaseOps pipelines to move changes from development to production through as many instances as needed for your ReleaseOps ecosystem.
-   Schedule releases or deploy changes on-demand.
-   Automate the testing and validation process with ReleaseOps to ensure that the proper checks, tests, scans, and approvals are completed before releasing changes to production.

See [ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/releaseops-landing.md) for more information.

**Important:** ReleaseOps is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Pipelines in ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/releaseops-pipeline-environments.md)**

    A pipeline is the flow of a deployment in ReleaseOps. A pipeline's flow is defined within playbooks, which enables you to customize as needed.

-   **[Releases in ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/releases-in-release-ops.md)**

    Scheduled and on-demand releases are how changes are deployed to target instances with ReleaseOps. Releases can contain one or more deployment requests.

-   **[Deployment requests in ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/deployment-requests.md)**

    Deployment requests contain one or more update sets, and are contained in a release.

-   **[Configure a new ReleaseOps ecosystem](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/configure-new-releaseops-ecosystem.md)**

    Configure a new ReleaseOps ecosystem using the sample pipelines and playbooks to begin deploying changes from your development to test to production instances.

-   **[Create a custom pipeline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/create-release-ops-pipeline.md)**

    Create a custom pipeline to move changes through your production environment to testing by duplicating one of the ReleaseOps playbooks.

-   **[Promote an update set for deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/promote-update-set-for-deployment.md)**

    When you're ready to deploy your changes, promote your update set to begin the deployment process.

-   **[Create a deployment request for a scheduled release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/create-a-new-deployment-request.md)**

    Create a deployment request for a scheduled release to contain your update set and enable your changes to move through the pipeline for deployment.

-   **[Create a release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/create-a-release.md)**

    Specify the details for your release, including the target instance that the changes deploy to and when the release should occur.


-   **[ReleaseOps guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/complete-guided-setup.md)**

    Starting with version 1.2.1 of ReleaseOps, you can use guided setup to help simplify the initial configuration process.


## Activation information

Install ReleaseOps by requesting it from the ServiceNow Store. Visit the ServiceNow Store to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the ServiceNow Store version history release notes.

## Additional requirements

ReleaseOps is not supported in regulated environments or on-premise. Check your entitlements to determine whether you have access to ReleaseOps.

## Related ServiceNow applications and features

-   **[App Engine Management Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/app-engine-management-center.md)**

    Track and manage requests, deployments, applications, and collaborative developers for your custom applications using the App Engine Management Center \(AEMC\).

-   **[Create applications without writing code using Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/creator-studio-landing.md)**

    If you have ever wanted to create an application but you don't know how to code, then Creator Studio was designed for you.

-   **[ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/servicenow-ide-landing.md)**

    Create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform.

-   **[ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/servicenow-studio-landing.md)**

    Easily create and edit custom apps and app files in one powerful development tool.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/build-automate-rn-landing.md)

