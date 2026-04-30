---
title: Building apps with Creator Studio
description: By now, your admin has set up Creator Studio, given you permission to build an app, and you've got a great idea for a request-fulfillment app! How should you think about using Creator Studio to create your app?
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 4
keywords: [build no code apps, building apps]
breadcrumb: [Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Building apps with Creator Studio

By now, your admin has set up Creator Studio, given you permission to build an app, and you've got a great idea for a request-fulfillment app! How should you think about using Creator Studio to create your app?

## What apps are in ServiceNow

A ServiceNow app is a package that performs a specific task for a specified group of users. Think of an app as a container with a set of rules around who can access and edit it. For example, ServiceNow apps can include an API, a table, a workspace, a form, a flow, or any combination of those things.

A Creator Studio app uses forms and automation to enable users to request something and move the request through the approval process. Creator Studio also enables you to the see the fulfiller's view of the Request App Workspace for the app.

## Create forms to gather request information

When finished, your app will look like a catalog of items that people can request. To create your app, you’ll:

1.  Select one of the available [catalog](creator-studio-glossary.md#) templates.
2.  Customize a [form](creator-studio-glossary.md#) to be included in the catalog using a WYSIWYG editor.

    A form describes one item in the catalog and provides space for questions that a requester will answer to specify details about what they want, such as the model number of a laptop. If your catalog needs multiple items, you can create multiple forms.

    **Note:** You can create a form using Now Assist. To learn more, see [Generating forms with Now Assist](creator-studio-text-to-form.md).


## Automate workflows and simplify tasks with playbooks

Streamlining your request-fulfillment process goes beyond just collecting information. Creator Studio empowers you to automate tasks with powerful [playbooks](creator-studio-glossary.md#). Think of them as pre-programmed workflows that kick in after a form is submitted.

Here are some things that playbooks can do:

-   **Effortless approval routing:** Automatically route requests to the right person for approval, eliminating manual steps and bottlenecks. Imagine a laptop request automatically going to the IT manager for a thumbs-up.
-   **Intuitive playbook builder:** No coding required! Create custom playbooks using an easy-to-use editor.

The playbooks you create use the information that people supply when they fill out your forms. So, the more details you ask for, the smoother the process runs.

## Workspaces give fulfillers a place to address requests

Once deployed, your app will sit in its own workspace category, which makes it easy for fulfillers to answer requests. You can customize the workspace or use it as-is.

For sys admin eyes only: Every app built in Creator Studio adds a record in the Request App Config table, which contains the table that the app uses. Your admin can change the table for an app, see [Administering an app's underlying table](creator-studio-admin-app-table.md) for more information.The name of the table follows the format of scope\_request, for example, x\_snc\_02\_03\_request.

-   **[Find existing apps in Creator Studio](../task/view-apps-creator-studio-home-page.md)**  
Perhaps you’ve been given permission to work on an app someone else created, or you want to add new items to the catalog in your app. The Creator Studio home page acts as your central hub, listing all the apps people in your company have built using Creator Studio.
-   **[Work with bookmarked apps in Creator Studio](../task/crs-work-with-bookmarked-apps.md)**  
Bookmark an app to quickly find it in Creator Studio, as well as ServiceNow Studio.
-   **[Change your development experience](../task/crs-change-dev-experience.md)**  
Choose a different development experience if you want a more robust environment using the experience switcher in Creator Studio.
-   **[App creation in Creator Studio](creator-studio-creating-apps.md)**  
Have you ever dreamed of creating your own app? With Creator Studio, you might be closer than you think! The following links will send you to the sections in this guide that will walk you through the steps.
-   **[Collaborating with others to build apps in Creator Studio](../reference/creator-studio-collaboration-roles.md)**  
Sometimes you need help building out your app, and that’s ok! And sometimes other people need your help building their apps, which is great! This is where collaboration comes into play.
-   **[Working with forms in Creator Studio](creator-studio-work-with-forms.md)**  
To add items or services to your catalog, you must create a different form for each thing being requested.
-   **[Working with automation in Creator Studio](creator-studio-working-with-automations.md)**  
How do you simplify and streamline tasks for fulfillers? Use automation! For example, you can have a task assigned automatically to someone based on what type of request it is. We’ll use playbooks to accomplish adding this automation to your app.
-   **[Configuring workspace lists and records for form submissions](creator-studio-form-submissions-workspace-about.md)**  
So, you’ve built your app, and people are submitting requests through it, that’s great! However, you might be wondering where those requests go after they’re submitted. They live in lists in a workspace where fulfillers can work on submitted forms, which you can customize in Creator Studio to suit your needs.
-   **[Testing and previewing Creator Studio apps and records](creator-studio-testing-apps.md)**  
Before you request deployment for your app, you can test out submitting a form and interact with any associated automation results on the record it creates.
-   **[Deploying your Creator Studio app](creator-studio-publishing-apps.md)**  
Congrats, you’ve built your app and are ready to share the first version of it with the world. That’s great! Deployment is the next step in the process.
-   **[I've built my app in Creator Studio, now what?](creator-studio-made-your-app-now-what.md)**  
You've added forms and automation to your app, and customized the workspace list configurations. Now what?

**Parent Topic:**[Creator Studio](creator-studio-landing.md)

