---
title: Create a deployment request for a scheduled release
description: Create a deployment request for a scheduled release to contain your update set and enable your changes to move through the pipeline for deployment.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [ReleaseOps, deploy changes, update sets, pipeline, ATF, schedule a release, deployment request, deployment analyzer]
breadcrumb: [Use, ReleaseOps, Deploying applications, Building applications]
---

# Create a deployment request for a scheduled release

Create a deployment request for a scheduled release to contain your update set and enable your changes to move through the pipeline for deployment.

## Before you begin

Role required: developer or release\_admin

This procedure applies to deployment requests for scheduled releases. To create a deployment request for an on-demand release, see the procedure in [Create a deployment request for an on-demand release](create-a-deployment-request-for-on-demand-release.md).

## Procedure

1.  On the **Deploy an update set** form, select the check box for **Create new deployment request**.

    Additional fields appear on the **Deploy an update set** form, which enable you to define the properties of the new deployment request.

2.  Enter a short description for the deployment request in the **Short description** field.

3.  Assign the deployment request to either an assignment group or a user.

    You can assign a deployment request to both an assignment group and a user, depending on who in your organization might need to be notified about issues with the deployment request. You must select at least one of the assignment options in order to complete the deployment request form.

    -   To assign the deployment request to an assignment group, select the **Assignment group** field, then select the group that you want to assign the deployment request to from the list.
    -   To assign the deployment request to a user, select the **Assigned to** field, then select the user that you want to assign the deployment request to from the list.
4.  Select the **Source environment** field, then select your development environment from the list.

5.  Select the **Release** field, then select the release that you want to want your deployment request to apply to from the list.

    **Note:** Releases must be activated in order to select them in a deployment request form.

    If your deployment request applies to a release that hasn’t already been created, ask your release admin to create a release for you. The procedure for creating a release is outlined in [Create a release](create-a-release.md). You can only select releases that have been activated.

    If your deployment request applies to an on-demand release, see the procedure in [Create a deployment request for an on-demand release](create-a-deployment-request-for-on-demand-release.md).

6.  Select the **ATF suites** field, then select the tests that you want to run for your deployment request.

    The list of ATF suites is populated by the tests that are available on your production instance. The ATF suites that you select within the deployment request form aren't the only tests that might run for your deployment request. Additional tests might be defined at the pipeline level, depending on the pipeline that your organization has configured.

7.  Select **Submit** to create your deployment request.

    Your deployment request is created. You can make additional changes to the deployment request as needed, such as adding additional update sets to the request.

8.  When you're ready to submit your deployment request through the pipeline, select the **Ready to assess** button.

    **Warning:** When you select **Ready to assess**, assessment of the deployment request begins immediately, and making additional changes to the deployment request isn't recommended. Only select **Ready to assess** when you're ready to deploy your changes to the pipeline.

    When you have selected **Ready to assess**, ReleaseOps automatically begins assessing your deployment request. You can see how the assessment is running and any issues that the assessment encountered in the **Activity** section of the deployment request form. Once your deployment request has passed the assessment checks, your deployment request will be moved into the pipeline that your organization has configured.


**Parent Topic:**[Using ReleaseOps to manage deployments](../concept/using-releaseops-to-manage-deployments.md)

