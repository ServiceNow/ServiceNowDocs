---
title: Request deployment for your app from Creator Studio to production
description: After you've tested your app's forms, playbooks, and workspace category on a non-production instance, for example a development instance, deploy it to a production instance so users can access it.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Deploying apps, Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Request deployment for your app from Creator Studio to production

After you've tested your app's forms, playbooks, and workspace category on a non-production instance, for example a development instance, deploy it to a production instance so users can access it.

## Before you begin

Your admin must set up a deployment pipeline before you can submit your app for review. Contact your admin if you need a pipeline configured.

To request that your app is deployed to production, you must be given permission to work on the app.

## About this task

You can't cancel the review cycle after you submit an app for deployment review, so make sure that your app is ready to go.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that you want to deploy to production.

3.  In the navigation panel, select **Submit for review**.

    ![Select Submit for review to request deployment](../image/crs-submit-review-btn.png "Submit for review")

4.  Select **Continue** on the Submit app for review modal.

5.  Now you need to choose which published forms are visible to users in the catalog. In the Ready for review section of the Review request forms modal, select which of the app's published forms that you want to be available after the app is deployed by selecting the **Visible to others** option.

    ![Select which forms to deploy](../image/cs-submit-request-forms.png "Review request forms for deployment")

6.  Select **Continue** when you're happy with the forms being deployed to production.

7.  Next, you must decide which of the app's activated playbooks will run on production after the app is deployed. In the Review playbooks modal, select the **Run on production** option for each playbook that you want to run on records that the app generates.

    **Note:** If you can't select a playbook, you need to go back to the **Automations** section of Creator Studio and activate it. If you need a refresher on that, check out [Activate a playbook in Creator Studio](creator-studio-activate-automation.md).

    Unactivated playbooks still get deployed to production with the app, they just won't run on the records unless your admin activates them on production or redeploys the app with the playbook activated.

8.  Select **Continue** when you're happy with the playbooks being deployed to run on production.

9.  Finally, make sure that all the release details for the published app are correct.

<table id="table_a5n_phs_m1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New version

</td><td>

[Version number](../concept/creator-studio-glossary.md#) of the app you're requesting for deployment. Creator Studio automatically generates an updated version number, but you can change it.Follow your organization's versioning guidelines, or use the x.y.z format, where x = major update, y = minor update, and z = patch.

</td></tr><tr><td>

[Release notes](../concept/creator-studio-glossary.md#)

</td><td>

Details on what's changed in this new version of the app, or a general description of what the app does if this is its first version.

</td></tr></tbody>
</table>    Read more about this step of requesting deployment in [App versioning and release notes for Creator Studio apps](../concept/creator-studio-app-release-versioning.md).

    ![Versioning info on deployment request](../image/cs-deploy-versioning.png "App versioning info")

10. Select **Submit for review** when everything is correct and ready for your admin to review and deploy.


## Result

Woohoo! Your app is ready to be reviewed for deployment.

## What to do next

Your admin uses Pipelines and Deployments to deploy the app to production. You can still make changes to the app after it's been deployed, you'll just need to request re-deployment when it's ready.

If you're an admin, check out [Managing deployments using Pipelines and Deployments](../../app-engine-studio/concept/manage-deployments-using-p-and-d-aemc.md) for the scoop on deploying apps.

**Parent Topic:**[Deploying your Creator Studio app](../concept/creator-studio-publishing-apps.md)

