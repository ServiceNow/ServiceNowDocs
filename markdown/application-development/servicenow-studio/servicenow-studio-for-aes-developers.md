---
title: ServiceNow Studio for App Engine Studio \(AES\) developers
description: As a current App Engine Studio developer, you can take advantage of new development capabilities in ServiceNow Studio while keeping many of the best features of AES.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Explore, ServiceNow Studio, Developing your application, Building applications]
---

# ServiceNow Studio for App Engine Studio \(AES\) developers

As a current App Engine Studio developer, you can take advantage of new development capabilities in ServiceNow Studio while keeping many of the best features of AES.

ServiceNow Studio is set up a bit differently than App Engine Studio, so use the following information to find your favorite features from App Engine Studio.

## Similar functionality

Several key features from AES look and behave very similarly in ServiceNow Studio. For example, the app creation path, integrating with source control, and the collaboration functions should all look familiar.

For more information, see the following topics.

-   [Create an application in ServiceNow Studio](../task/create-an-application-in-servicenow-studio.md)
-   [Source control integration in ServiceNow Studio](source-control-integration.md)
-   [Collaborating on apps using ServiceNow Studio](manage-app-collab-servicenow-studio.md)

## My apps

When you first open ServiceNow Studio, you likely won't see all of the apps you're used to working on. But, all you have to do is open them in ServiceNow Studio using the Navigator panel Apps section, filtered for custom apps.

![Access the Apps list in the navigator panel to see a list of all your applications.](../image/sn-studio-app-list-zs2.png)

The best way to access frequently used apps, app files, and full lists is to bookmark them. For more information, see [Bookmark apps and files in ServiceNow Studio](../task/qs-bookmark-apps-files.md) and [Bookmark lists in ServiceNow Studio](../task/bookmark-lists-in-sns.md).

## File types

In AES, there are options to create four categories of files, or metadata: Data, experiences, logic and automation, and security.

In ServiceNow Studio, you can create many different types of files, including the four categories you've seen in AES. In contrast to AES, where you have to be in an app to create a file, you can create files right from the home page of ServiceNow Studio and specify the application afterward. You can also select **Add** next to any category on an application's App details page to add a file of that type.

![Use the Add or Create options on the App details page to create new files of any category.](../image/sn-studio-aes-devs-add.png)

App files define aspects of how an application functions. For example, you could add a business rule to your application to perform server-side actions when a record is changed in some way. Or, you could add AI files to automate tasks.

For more information about the types of files you can add in ServiceNow Studio and how to work with them, see the following topics.

-   [Create an app file in ServiceNow Studio](../task/sn-studio-create-app-file.md)
-   [Working with metadata app file categories in the ServiceNow Studio Navigator](sn-studio-working-with-metadata.md)
-   [ServiceNow Studio Navigator panel taxonomy](../reference/servicenow-studio-file-navigator-taxonomy.md)

## Application scope

Manually switching scope when working on several different applications has been the norm for many ServiceNow app builders. In ServiceNow Studio, the scope automatically updates based on which app you're working in. ServiceNow Studio also groups the integrated tabs based on scope, so you can see which app files are related.

![Integrated tabs with different types of files open are color coded and grouped. Upon hovering, see the scope the application or file is in.](../image/sn-studio-integrated-tabs.png)

1.  Any file in a scoped app opens in a color-coded tab with information about what kind of file it is. In this instance, the playbook opened in an integrated tab, where you can update it using the Workflow Studio interface.
2.  Tabs without colors indicate that the file is in the global scope. You can edit global files in ServiceNow Studio.
3.  Any tab that's actively open in the canvas shows a contrasting color to indicate the open state.
4.  Tabs that are color-coded and grouped are in the same scope. In this example, both actions are in the same application, so they open in the same color tab.

In each application, you can find the scope and update set at the bottom left of the page.

![See the application scope and update set at the bottom of the open tab.](../image/sn-studio-scope-update-set-zs1.png)

Some builders in ServiceNow Studio override the automatic scope switching feature. For example, if you're using Table Builder to edit a form or table file, you wiIl see a message saying the scope is controlled and indicated by the builder.

![Some builders control the scope for apps open in ServiceNow Studio.](../image/sn-studio-scope-builder.png)

For more information, see [Open apps and app files across scopes in ServiceNow Studio](qs-open-apps-files-across-scopes.md) and [Access integrated development tools and builders in ServiceNow Studio](open-and-switch-between-integrated-development-tools.md).

## Templates

AES contains a library of application templates that you can use to create apps. Templates are also a great way to find inspiration for functionality you would like in your apps. In ServiceNow Studio, you can find inspiration from the App Gallery. When you select **Create** &gt; **App**, you can choose from several options to get started. On the right side of the page, you will see a link to the app gallery, which contains files for all different kinds of apps and metadata.

**Note:** While the App Gallery contains apps and files for inspiration, you cannot create an application from those files as you would a template in AES.

![Explore the app gallery in ServiceNow Studio to find inspiration from completed applications.](../image/sn-studio-app-gallery.png)

