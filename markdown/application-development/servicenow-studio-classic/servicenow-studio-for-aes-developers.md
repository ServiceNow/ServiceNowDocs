---
title: ServiceNow Studio for App Engine Studio \(AES\) developers
description: If you currently develop in App Engine Studio, use ServiceNow Studio to access advanced development capabilities while retaining the core features you already use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/servicenow-studio-for-aes-developers.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Explore, ServiceNow Studio, Developing your application, Building applications]
---

# ServiceNow Studio for App Engine Studio \(AES\) developers

If you currently develop in App Engine Studio, use ServiceNow Studio to access advanced development capabilities while retaining the core features you already use.

ServiceNow Studio is organized differently from App Engine Studio. Use the following sections to find the features you are familiar with from App Engine Studio.

## What features work the same way in ServiceNow Studio?

Several key features from AES work the same way in ServiceNow Studio, including app creation, source control integration, and collaboration. For more information, see the following topics.

-   [Create an application in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/create-an-application-in-servicenow-studio.md)
-   [Source control integration in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/source-control-integration.md)
-   [Collaborating on apps using ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/manage-app-collab-servicenow-studio.md)

## Where are my apps?

When you first open ServiceNow Studio, not all of your apps are visible by default. To find them, open the Navigator panel, select the Apps section, and filter for custom apps.

\[Omitted image "sn-studio-app-list-zs2.png"\] Alt text: Access the Apps list in the Navigator panel to see all your applications.

To access frequently used apps, app files, and lists quickly, bookmark them. For more information, see [Bookmark apps and files in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/qs-bookmark-apps-files.md) and [Bookmark lists in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/bookmark-lists-in-sns.md).

## How do I work with different file types in ServiceNow Studio?

In AES, you can create files in four categories: Data, Experiences, Logic and Automation, and Security.

ServiceNow Studio supports all four of those categories and many additional file types. Unlike AES, where you must be inside an app to create a file, ServiceNow Studio lets you create files from the home page and specify the application afterward. You can also select **Add** next to any category on the App details page to create a file of that type.

\[Omitted image "sn-studio-aes-devs-add.png"\] Alt text: Use the Add or Create options on the App details page to create new files of any category.

App files define how an application functions. For example, add a business rule to perform server-side actions when a record changes, or add AI files to automate tasks.

For more information about file types and how to work with them, see the following topics.

-   [Create an app file in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sn-studio-create-app-file.md)
-   [Metadata app file categories in the ServiceNow Studio Navigator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sn-studio-working-with-metadata.md)
-   [ServiceNow Studio Navigator panel taxonomy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-file-navigator-taxonomy.md)

## How does scope work in ServiceNow Studio?

In ServiceNow Studio, the scope updates automatically based on which app you are working in — you do not need to switch it manually. The current scope and update set appear at the bottom left of the page for each open application.

\[Omitted image "sn-studio-integrated-tabs.png"\] Alt text: Integrated tabs with different types of files open are color coded and grouped. Upon hovering, see the scope the application or file is in.

1.  Any file in a scoped app opens in a color-coded tab with information about what kind of file it is. In this instance, the playbook opened in an integrated tab, where you can update it using the Workflow Studio interface.
2.  Tabs without colors indicate that the file is in the global scope. You can edit global files in ServiceNow Studio.
3.  Any tab that's actively open in the canvas shows a contrasting color to indicate the open state.
4.  Tabs that are color-coded and grouped are in the same scope. In this example, both actions are in the same application, so they open in the same color tab.

\[Omitted image "sn-studio-scope-update-set-zs1.png"\] Alt text: See the application scope and update set at the bottom of the open tab.

Some builders override automatic scope switching. For example, when you use Table Builder to edit a form or table file, a message indicates that the scope is controlled by the builder.

\[Omitted image "sn-studio-scope-builder.png"\] Alt text: Some builders control the scope for apps open in ServiceNow Studio.

For more information, see [Open apps and app files across scopes in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/qs-open-apps-files-across-scopes.md) and [Access integrated development tools and builders in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/open-and-switch-between-integrated-development-tools.md).

## Where are app templates?

AES provides a library of application templates for creating apps. ServiceNow Studio does not have templates, but the App Gallery provides examples of completed apps and metadata files you can use for reference. To access the App Gallery, select **Create** &gt; **App** and select the App Gallery link on the right side of the page.

**Note:** The App Gallery is for reference only. You cannot create an application directly from App Gallery files as you would from a template in AES.

\[Omitted image "sn-studio-app-gallery.png"\] Alt text: Explore the App Gallery in ServiceNow Studio to find examples of completed applications.

