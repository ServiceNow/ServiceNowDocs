---
title: Exploring the App Engine Management Center
description: Learn about how the App Engine Management Center \(AEMC\) can help to centralize and streamline your application development and governance at scale.
locale: en-US
release: zurich
product: App Engine Management Center
classification: app-engine-management-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [App Engine Management Center, Governing app development, Building applications]
---

# Exploring the App Engine Management Center

Learn about how the App Engine Management Center \(AEMC\) can help to centralize and streamline your application development and governance at scale.

## App Engine Management Center overview

The App Engine Management Center \(AEMC\) is a powerful tool that innovates and unifies the application development, deployment, and governance experience. AEMC contains all of the features that you need to manage application development within your organization, from idea submission to deployment. Using AEMC, admins can manage requests for new apps and delegate development and collaboration permissions. Admins can also oversee the entire deployment process with insights into individual deployment requests, test suites, and scheduled deployments.

Starting with version 28.2.1 of AEMC, ReleaseOps is integrated into AEMC. See the ReleaseOps in AEMC section for more information.

## App Engine Management Center users

<table id="table_rtv_1dk_tfc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Citizen and pro developers

</td><td>

-   Apply for citizen development to submit ideas for new applications.
-   Submit collaboration requests to enable relevant stakeholders to be involved in the application development process.
-   Submit applications for review.

</td></tr><tr><td>

App Engine admins

</td><td>

-   Configure pipelines that are tailored to an organization's unique needs.
-   Manage which user groups have access to development tools by reviewing application intake and collaboration requests.
-   Manage application deployment requests and testing, verifying that applications are ready to be moved to staging and production instances.

</td></tr></tbody>
</table>## App Engine Management Center workflow

The workflow for managing app development and deployment through an App Engine pipeline using the App Engine Management Center is outlined in the following list:

1.  Developers submit ideas for new applications to build.
2.  App Engine admins review and approve application intake requests.
3.  Developers and collaborators build custom applications using App Engine product offerings.
4.  Once an app is ready, developers submit the app for review.
5.  App Engine admins review and approve deployment requests, moving the app through their organization's unique pipeline.
6.  App Engine admins review test suite logs to verify that the application is ready to be deployed to production instances.
7.  App Engine admins approve apps for deployment to production instances.

## ReleaseOps in AEMC

Starting with version 28.2.1 of AEMC, ReleaseOps is integrated into AEMC. ReleaseOps improves upon the existing pipelines deployment process by supporting the deployment of update sets, leveraging the automation capabilities of ServiceNow Playbooks, and enabling both scheduled and on-demand releases. To learn more about ReleaseOps, see [Exploring ReleaseOps](../../release-ops/concept/exploring-release-ops.md).

Developers working with update sets in version 28.1.2 of ServiceNow Studio and later can trigger ReleaseOps deployments directly within the development environment.

In development environments where full support isn’t available yet, such as App Engine Studio and Creator Studio, you can still take advantage of ReleaseOps features in AEMC by migrating your existing App Engine pipeline to ReleaseOps. For more information about migrating to ReleaseOps, see the following resources:

-   [Migrating App Engine pipelines to ReleaseOps](migrating-ae-pipelines-to-releaseops-aemc.md)
-   [Migration tasks](migration-tasks-aemc.md)

## What to explore next

To learn more about configuring and using App Engine Management Center, see:

-   [Configuring AEMC](configuring-aemc.md)
-   [Using AEMC](using-aemc.md)

