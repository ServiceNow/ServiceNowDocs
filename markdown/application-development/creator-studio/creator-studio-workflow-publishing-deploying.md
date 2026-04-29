---
title: Publishing, activation, and deployment workflow for forms, automation, and apps
description: When you build an app in Creator Studio, you must create forms and automation. You can also customize the workspace list configurations and records that fulfillers use before everything is deployed to production.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Publishing, activation, and deployment workflow for forms, automation, and apps

When you build an app in Creator Studio, you must create forms and automation. You can also customize the workspace list configurations and records that fulfillers use before everything is deployed to production.

As you develop apps in Creator Studio, you should move sequentially through the following sections. For example, you should mark all of an app's forms as ready in the **Forms** section of Creator Studio before you begin to work on the app's **Automations** section.

1.  When you're done building forms, publish them by marking them as ready.

    Published forms are then available in the catalog on the non-production instance that you're using for development.

2.  When automated playbooks \(which are based on the forms you already created\) are ready, activate them.

    Published playbooks can be triggered when a form is created or updated on the non-production instance you're using for development.

3.  The app's fulfiller workspace is already available on the non-production instance that you're using for development for you to test and customize. Additionally, you can interact with test records by selecting a record in a **List configuration** section. You can then change how the record appears using the **Record details** of the navigation panel.
4.  Test out submitting a form using the **Try it** button.
5.  When everything looks good and you're ready to deploy the app to production, you submit it for review.
6.  After your admin deploys the app to production, the app is available to users whose role gives them access to it. On the production instance:
    -   The app is available to users
    -   The catalog contains all published forms
    -   Activated playbooks are triggered on applicable records
    -   Unactivated playbooks are deployed but must be activated by an admin before they can run
    -   Users can access the workspace to review the app's submitted requests
7.  To update a published app, make the changes on your non-production instance and then request that your admin redeploys the updated app to production.

