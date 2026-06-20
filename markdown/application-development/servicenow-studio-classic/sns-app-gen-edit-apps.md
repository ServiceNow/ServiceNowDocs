---
title: Edit applications in Now Assist for App generation with ServiceNow Studio
description: In Xanadu Store Release 2, use the generative AI capabilities in Now Assist for Creator to edit applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/servicenow-studio-classic/sns-app-gen-edit-apps.html
release: xanadu
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2024-10-17"
reading_time_minutes: 2
keywords: [app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai]
breadcrumb: [Generate apps with Now Assist for Creator for ServiceNow Studio, Now Assist for app generation in ServiceNow Studio, Using ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Edit applications in Now Assist for App generation with ServiceNow Studio

In Xanadu Store Release 2, use the generative AI capabilities in Now Assist for Creator to edit applications.

## Before you begin

You have created an application using Now Assist for Creator.

Role required: admin and now.assist.creator \(as of Xanadu Store Release 2, if you have users that only need to edit, not create, apps, they can be assigned the delegated\_developer, now\_assist\_panel\_user, and now.assist.creator roles\)

## Procedure

1.  Open the Now Assist panel by navigating to App Engine &gt; ServiceNow Studio and selecting the Now Assist icon.

    \[Omitted image "app-generation-task-initiation-xsr2.png"\] Alt text: Now Assist highlighted in banner.

2.  In the Now Assist panel, select **Update an app**.

3.  Select the app to edit.

    The apps that appear in the Now Assist panel for editing are custom applications you have created or to which you have access.

    Users with the admin and now.assist.creator roles can create and edit applications. Users with the delegated\_developer, now\_assist\_panel\_user, and now.assist.creator roles can edit applications.

    If you have the delegated\_developer, now\_assist\_panel\_user, and now.assist.creator roles, but do not see the app that you need, contact your App Engine admin. Ask them to add you to the app as a delegated developer. For more information, see [Delegated development and deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/delegated-development-and-deployment/c_DelegatedDevelopment.md).

    To edit with Now Assist, ensure that your scope is set to the same scope as the app. If you aren't in the correct scope, return to the browser tab you used to launch ServiceNow Studio and use the scope picker to change the scope. \(For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/building-applications/c_ApplicationPicker.md).\) When you're finished, select the tab with ServiceNow Studio open and select **Done**.

4.  Interact with Now Assist to edit the app.

    For example, request new metadata such as a form or request a new table that is extended from an existing table.

    **Note:** Now Assist may encounter issues while updating a large app. Consider updating the app manually in ServiceNow Studio instead.


## What to do next

Continue interacting with Now Assist to edit and refine the app. For more information, see [General guidelines for using app generation in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/servicenow-studio-classic/sns-app-gen-guidelines.md).

**Parent Topic:**[Generate apps with Now Assist for Creator for ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/servicenow-studio-classic/sns-app-gen-using-landing.md)

