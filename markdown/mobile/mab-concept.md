---
title: Mobile App Builder
description: The ServiceNow Mobile App Builder \(MAB\) is a configuration tool to build and manage screens and records that make up workflows within ServiceNow mobile apps. The organizational layout and navigation options in the Mobile App Builder facilitate a faster and more intuitive creation of ServiceNow mobile applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Building tools, Building mobile apps, Mobile Platform]
---

# Mobile App Builder

The ServiceNow® Mobile App Builder \(MAB\) is a configuration tool to build and manage screens and records that make up workflows within ServiceNow mobile apps. The organizational layout and navigation options in the Mobile App Builder facilitate a faster and more intuitive creation of ServiceNow mobile applications.

an overview of mobile app builder capabilities 

Benefits and uses of the Mobile App Builder include the following:

-   Organize records in a hierarchical layout for quick access and reference.
-   Support hierarchical tree navigation, enabling users to visualize how records relate to each other and tie into the overall mobile app configuration.
-   View a live preview of how certain components will appear in the mobile app.
-   Support the editing of all ServiceNow base system mobile application scopes.
-   Streamline mobile configurations by doing the following:
    -   Enable the editing of multiple records in a single screen.
    -   Guide users to appropriate record relationships.
    -   Prevent invalid configuration choices.
    -   Auto-populate fields when creating relationships between records.

**Note:**

Mobile App Builder \(MAB\) is automatically installed on your instance with the base system plugin sn\_mab. Starting in version 22.6, when there is a new version of the plugin, a banner appears at the top of the MAB screen indicating a new version is available. Select **Update** in the banner to install the new version.

For more information about the MAB plugin and its associated plugins for the Mobile App Builder API and Mobile Card Builder, see [Mobile plugins](../reference/sg-mobile-plugins.md).

## Mobile App Builder workflow

The building of mobile applications takes place within three screens:

-   The Mobile App Builder application scope selection screen: Select the scope to work on.
-   The Mobile App Builder categories home screen: Select the record to work on.
-   The Mobile App Builder record screen: Work on your records.

In the Mobile App Builder application scope selection screen, you select the application scope to work in. After choosing your application scope, select a category or specific record to create or edit in the Mobile App Builder categories home screen. The record you select then opens in the Mobile App Builder record screen. In this screen, you perform most of your work, by populating record fields and creating relationships between different records.

The following video shows you how to configure records in Mobile App Builder and provides a demonstration of a practical use case.

Video demonstrating how to build a basic app in Mobile App Builder.

## Mobile Publishing integration

In the Washington DC family release and later, Mobile App Builder is now integrated with Mobile Publishing:

![Mobile Publishing sidebar on the Mobile App Builder main page](../image/mob-pub-mab-integration.png)

Select a custom branded app card in the **Manage your branding** side panel to open it in Mobile Publishing. For more information about Mobile Publishing, see [Publish mobile apps with custom branding](mobile-publishing.md).

## Add push notifications to mobile apps with Mobile App Builder

In the Washington DC family release and later, you can now add push notifications to your mobile apps with Mobile App Builder:

![Mobile App Builder menu showing push notifications](../image/push-notif-in-mab.png)

Select **Mobile notifications** in the menu and then select the push notification you want to use. For more information about push notifications, see [Mobile push notifications](sg-mobile-push-notifications.md).

