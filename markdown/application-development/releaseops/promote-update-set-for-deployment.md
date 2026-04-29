---
title: Promote an update set for deployment
description: When you're ready to deploy your changes, promote your update set to begin the deployment process.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [ReleaseOps, deploy changes, update sets, pipeline, ATF, schedule a release, deployment request, deployment analyzer]
breadcrumb: [Use, ReleaseOps, Deploying applications, Building applications]
---

# Promote an update set for deployment

When you're ready to deploy your changes, promote your update set to begin the deployment process.

## Before you begin

Role required: developer or release\_admin

**Note:** You must have the sn\_releaseops.deployment\_controller property set on your development instance or the instance from which you intend to promote changes for deployment.

This procedure describes the process of promoting an update set for deployment once an update set has already been created. To learn more about the process of creating an update set, see [Working with update sets](../../system-update-sets/concept/using-system-update-sets.md).

## Procedure

1.  Open the update set record with the changes that you want to promote for deployment.

    1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

    2.  Select the update set record with the changes that you want to promote for deployment.

2.  If the update set **State** field isn't already set to complete, set the state to complete.

    The **Promote update set** button, which enables you to promote the update set changes for deployment, displays only once the update set **state** field is set to Complete.

    1.  Select the **State** field, then select Complete from the list.

    2.  Select and hold \(or right-click\) in the update set record header, then select **Save**.

3.  Select the **Promote update set** button.

    ![The Promote update set button appears when an update set State field is set to Complete.](../image/releaseops-promote-update-set-button.png)

    When you select **Promote update set**, you’re automatically redirected to the deployment request form on the production instance, where you can select the deployment request to which the update set changes should be attached.

    ![The deployment request form on the production instance enables you to promote your changes for deployment through the pipeline.](../image/releaseops-deployment-request-form.png)


## What to do next

Choose from one of the following options to attach the update set to a deployment request and submit the changes for deployment through the pipeline.

-   To attach the update set to an existing deployment request, see [Attach an update set to an existing deployment request](attach-an-update-set-to-existing-deployment-request.md).
-   To attach the update set to a new deployment request for a scheduled release, see [Create a deployment request for a scheduled release](create-a-new-deployment-request.md).
-   To attach the update set to a new deployment request for an on-demand release, see [Create a deployment request for an on-demand release](create-a-deployment-request-for-on-demand-release.md).

**Parent Topic:**[Using ReleaseOps to manage deployments](../concept/using-releaseops-to-manage-deployments.md)

