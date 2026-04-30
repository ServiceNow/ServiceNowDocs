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

See [ReleaseOps](https://www.servicenow.com/docs/access?context=releaseops-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

**Important:** ReleaseOps is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Pipelines in ReleaseOps](https://www.servicenow.com/docs/access?context=releaseops-pipeline-environments&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    A pipeline is the flow of a deployment in ReleaseOps. A pipeline's flow is defined within playbooks, which enables you to customize as needed.

-   **[Releases in ReleaseOps](https://www.servicenow.com/docs/access?context=releases-in-release-ops&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Scheduled and on-demand releases are how changes are deployed to target instances with ReleaseOps. Releases can contain one or more deployment requests.

-   **[Deployment requests in ReleaseOps](https://www.servicenow.com/docs/access?context=deployment-requests&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Deployment requests contain one or more update sets, and are contained in a release.

-   **[Configure a new ReleaseOps ecosystem](https://www.servicenow.com/docs/access?context=configure-new-releaseops-ecosystem&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Configure a new ReleaseOps ecosystem using the sample pipelines and playbooks to begin deploying changes from your development to test to production instances.

-   **[Create a custom pipeline](https://www.servicenow.com/docs/access?context=create-release-ops-pipeline&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Create a custom pipeline to move changes through your production environment to testing by duplicating one of the ReleaseOps playbooks.

-   **[Promote an update set for deployment](https://www.servicenow.com/docs/access?context=promote-update-set-for-deployment&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    When you're ready to deploy your changes, promote your update set to begin the deployment process.

-   **[Create a deployment request for a scheduled release](https://www.servicenow.com/docs/access?context=create-a-new-deployment-request&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Create a deployment request for a scheduled release to contain your update set and enable your changes to move through the pipeline for deployment.

-   **[Create a release](https://www.servicenow.com/docs/access?context=create-a-release&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Specify the details for your release, including the target instance that the changes deploy to and when the release should occur.


-   **[ReleaseOps guided setup](https://www.servicenow.com/docs/access?context=complete-guided-setup&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Starting with version 1.2.1 of ReleaseOps, you can use guided setup to help simplify the initial configuration process.


## Activation information

Install ReleaseOps by requesting it from the ServiceNow Store. Visit the ServiceNow Store to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the ServiceNow Store version history release notes.

## Related ServiceNow applications and features

-   **[App Engine Management Center](https://www.servicenow.com/docs/access?context=app-engine-management-center&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Track and manage requests, deployments, applications, and collaborative developers for your custom applications using the App Engine Management Center \(AEMC\).

-   **[Create applications without writing code using Creator Studio](https://www.servicenow.com/docs/access?context=creator-studio-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    If you have ever wanted to create an application but you don't know how to code, then Creator Studio was designed for you.

-   **[ServiceNow IDE](https://www.servicenow.com/docs/access?context=servicenow-ide-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform.

-   **[ServiceNow Studio](https://www.servicenow.com/docs/access?context=servicenow-studio-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Easily create and edit custom apps and app files in one powerful development tool.


**Parent Topic:**[App development and low-code release notes](../now-platform-app-engine/build-automate-rn-landing.md)

