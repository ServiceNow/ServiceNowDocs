---
title: Creator Studio development instance strategy
description: Make sure to install Creator Studio on all ServiceNow instances where users will be building applications, including the production instance.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Install, Configure, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Creator Studio development instance strategy

Make sure to install Creator Studio on all ServiceNow instances where users will be building applications, including the production instance.

## Deciding on your instance strategy

You need to decide how you want to manage access to Creator Studio within your company. Consider the following options:

-   **Open Access:** Allow everyone in your company to use Creator Studio to create apps.
-   **Restricted Access:** Limit access to a specific group of users.
-   **Request-Based Access:** Set up a form where users can apply for access. Admins will review these requests and decide whether to grant access.

## Development and deploying to production instances

A non-production instance that is similarly configured to your production instance may be the best candidate for your test environment. You can then more accurately find issues that may arise if the application is deployed to production.

You should ensure that developers build apps in Creator Studio on a non-production instance, and then deploy apps that are ready and approved to production.

When you deploy an app, the records are referenced in the Store Apps \[sys\_store\_app\] table on the production instance. But when you're developing an app, the records are referenced in the System Applications \[sys\_app\] table. So if you develop in production, you're developing using the \[sys\_app\] table instead of \[sys\_store\_app\].

After you establish your instance strategy, you must also establish and automate your approval or review process. Creator Studio runs on your non-production environment, and admins then deploy apps to the production environment. For more information on the deployment process, see [Deploying your Creator Studio app](creator-studio-publishing-apps.md).

If your organization has multiple non-production environments, you must decide which non-production environment Creator Studio will run on. You must also determine which pipeline to use for promoting apps from a particular non-production instance to your test instance, and then finally to production where the app will be running live. For more information, see [Pipelines and Deployments](../../app-engine-studio/concept/manage-deployments-using-p-and-d-aemc.md).

## Catalog configuration requirement for Creator Studio

To ensure that forms appear correctly for users, the non-production and production instances must have the same Service Catalog and all of its categories.

## Developer roles and testing apps on instances

If you have a Creator Studio role of sn\_creatorstudio.user or sn\_creatorstudio.restricted\_user, you won't be able to test the apps you build on the non-production instance's Request App Workspace. You should be able to test the app on the non-production instance using Creator Studio's app previews. You will be able to test the apps as a fulfiller in the workspace on the app that's been deployed to production.

**Use case:**

Let's say that a user is in the Creator Studio Users group, so when that user builds an app, that user gets delegated development permissions for that app. That user can then publish a request form, and if there are no roles required for the form, that user can submit requests with the form.

However, that user won't be able to fulfill requests or access the Request App Workspace because that user won't have the x\_acme\_user\_app.agent role, and that user can't give that role to themself. Administrators must assign additional roles as necessary.

**Parent Topic:**[Installing Creator Studio from the ServiceNow Store](installing-creator-studio-from-the-store.md)

