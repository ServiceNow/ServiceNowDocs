---
title: ReleaseOps release notes
description: The ServiceNow ReleaseOps application enables developers to manage deployments using pipelines and the automation power of playbooks to streamline testing, validating, and releasing changes to production. ReleaseOps is a new application in the Zurich release.The ServiceNow ReleaseOps application enables developers to manage deployments using pipelines and the automation power of playbooks to streamline testing, validating, and releasing changes to production. ReleaseOps is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# ReleaseOps release notes

The ServiceNow® ReleaseOps application enables developers to manage deployments using pipelines and the automation power of playbooks to streamline testing, validating, and releasing changes to production. ReleaseOps is a new application in the Zurich release.

## About ReleaseOps

-   Use ReleaseOps guided setup to simplify initial configuration.
-   Customize ReleaseOps pipelines to move changes from development to production through as many instances as needed for your ReleaseOps ecosystem.
-   Schedule releases or deploy changes on-demand.
-   Automate the testing and validation process with ReleaseOps to ensure that the proper checks, tests, scans, and approvals are completed before releasing changes to production.

See  for more information.

## Activation and other requirements

**Important:** ReleaseOps is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install ReleaseOps by requesting it from the ServiceNow Store. Visit the ServiceNow Store to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the ServiceNow Store version history release notes.

-   **Additional requirements**

    ReleaseOps is not supported in regulated environments or on-premise. Check your entitlements to determine whether you have access to ReleaseOps.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/build-automate-rn-landing.md)

## Zurich

The ServiceNow® ReleaseOps application enables developers to manage deployments using pipelines and the automation power of playbooks to streamline testing, validating, and releasing changes to production. ReleaseOps is a new application in the Zurich release.

### What's new

-   ****

    A pipeline is the flow of a deployment in ReleaseOps. A pipeline's flow is defined within playbooks, which enables you to customize as needed.

-   ****

    Scheduled and on-demand releases are how changes are deployed to target instances with ReleaseOps. Releases can contain one or more deployment requests.

-   ****

    Deployment requests contain one or more update sets, and are contained in a release.

-   ****

    Configure a new ReleaseOps ecosystem using the sample pipelines and playbooks to begin deploying changes from your development to test to production instances.

-   ****

    Create a custom pipeline to move changes through your production environment to testing by duplicating one of the ReleaseOps playbooks.

-   ****

    When you're ready to deploy your changes, promote your update set to begin the deployment process.

-   ****

    Create a deployment request for a scheduled release to contain your update set and enable your changes to move through the pipeline for deployment.

-   ****

    Specify the details for your release, including the target instance that the changes deploy to and when the release should occur.


-   **ReleaseOps guided setup**

    Starting with version 1.2.1 of ReleaseOps, you can use guided setup to help simplify the initial configuration process.


