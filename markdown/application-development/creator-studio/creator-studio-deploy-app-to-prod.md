---
title: Request deployment for your app from Creator Studio to production
description: After you've tested your app's forms, playbooks, and workspace category on a non-production instance, for example a development instance, deploy it to a production instance so users can access it.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Deploying your Creator Studio app, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
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

3.  Select to **Preview** how different forms appear in various experiences, or select the **View** or **Edit** button to view or edit the application experience.

    Select different previewing options if you want to make sure that you've selected the correct application and see how it will appear in the following formats:

    -   **Portal** \(see a preview of how it'll appear on a desktop website\)
    -   **Now Mobile** \(see a preview of how it'll appear on a mobile phone or device\)
    -   **Virtual agent** \(see a representation of how it'll appear on a chatbot interface\)

        **Note:** Your organization should have the correct plugins installed to see how the form will appear in Virtual Agent. If you're interested, ask your admin and see [Catalog builder preview topic conversation](https://www.servicenow.com/docs/access?context=catalog-builder-preview-topic&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information on previewing forms and their catalog items in Virtual Agent.

    The **View** button displays forms that have been published and doesn't explicitly create a new draft form for development. The **Edit** button takes you to a development form, for example, a new draft version of a form that's already been published.

    ![Preview how your app will look](../image/crs-portal-preview.png "Preview the app's experience")

    You can also check out a representation of how the form submissions workspace will appear by selecting the **Submissions** preview, as well as the records your app generates for it \(by selecting the **Record** preview\).

4.  In the application header, select **Submit for review**.

    ![Select Submit for review to request deployment](../image/cs-submit-review-button.png "Submit for review")

5.  Select **Continue** on the Submit app for review modal.

6.  Now you need to choose which published forms are visible to users in the catalog. In the Ready for review section of the Review request forms modal, select which of the app's published forms that you want to be available after the app is deployed selecting the **Visible to others** option.

    ![Select which forms to deploy](../image/cs-submit-request-forms.png "Review request forms for deployment")

7.  Select **Continue** when you're happy with the forms being deployed to production.

8.  Next, you must decide which of the app's activated playbooks will run on production after the app is deployed. In the Review playbooks modal, select the **Run on production** option for each playbook that you want to run on records that the app generates.

    **Note:** If you can't select a playbook, you need to go back to the **Automations** tab of Creator Studio and activate it. If you need a refresher on that, check out [Activate a playbook in Creator Studio](creator-studio-activate-automation.md).

    Unactivated playbooks still get deployed to production with the app, they just won't run on the records unless your admin activates them on production or redeploys the app with the playbook activated.

9.  Select **Continue** when you're happy with the playbooks being deployed to run on production.

10. Finally, make sure that all the release details for the published app are correct.

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

11. Select **Submit for review** when everything is correct and ready for your admin to review and deploy.


## Result

Woohoo! Your app is ready to be reviewed for deployment.

## What to do next

Your admin uses Pipelines and Deployments to deploy the app to production. You can still make changes to the app after it's been deployed, you'll just need to request re-deployment when it's ready.

If you're an admin, check out [Managing deployments using pipelines in AEMC](../../app-engine-studio/concept/manage-deployments-using-aemc.md#) for the scoop on deploying apps.

**Parent Topic:**[Deploying your Creator Studio app](../concept/creator-studio-publishing-apps.md)

