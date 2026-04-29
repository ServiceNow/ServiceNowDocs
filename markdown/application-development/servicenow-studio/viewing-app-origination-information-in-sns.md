---
title: Viewing app origination information in ServiceNow Studio
description: Select the best environment for app development and deployment by seeing where your app was created. View app origination information on the App details page in ServiceNow Studio.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Change your development experience, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Viewing app origination information in ServiceNow Studio

Select the best environment for app development and deployment by seeing where your app was created. View app origination information on the App details page in ServiceNow Studio.

## App details page

Each App details page shows if the app was created in Creator Studio or created in ServiceNow IDE and converted to Fluent. If the app was created in ServiceNow Studio, it won't have a badge on it. This information helps you know whether the app can continue being edited and deployed through ServiceNow Studio, or if it should be opened and deployed in a different application.

![The app details page shows badges for AI, Creator Studio, and Fluent to let you know where the app was created and may need to be deployed.](../image/sn-studio-crs-badge.png)

## Apps created in Creator Studio

Only apps created in Creator Studio can be edited in Creator Studio. This is because only a subset of the metadata supported in ServiceNow Studio is supported in Creator Studio.

You can open your app in Creator Studio by selecting the more options icon ![more options icon](../image/sn-studio-more-options-icon.png) on the Navigator panel or the App details page and selecting **Open with Creator Studio**. For more information, see [Building apps with Creator Studio](../../creator-studio/concept/building-apps-with-creator-studio.md).

![Option to open the current app in Creator Studio from the Navigator panel.](../image/sn-studio-open-in-crs.png)

![Option to open the current app in Creator Studio from the App details page.](../image/sn-studio-open-w-creator-studio.png)

## Apps created in ServiceNow IDE

Apps created in ServiceNow IDE can be edited in ServiceNow Studio.

**Important:** However, you cannot make changes to a Fluent app in ServiceNow Studio and deploy from ServiceNow Studio. Apps created in ServiceNow IDE or converted to Fluent must be deployed using the ServiceNow IDE.

When you see the **Fluent** badge on an app, follow the normal app deployment process used in the ServiceNow IDE. For more information, see [Developing applications with the ServiceNow IDE](../../servicenow-ide/concept/developing-applications-servicenow-ide.md).

## Accessing apps using filters

Easily access your Creator Studio or Fluent apps using the filter in the Apps section of the Navigator panel. Select the **Creator Studio** or **Fluent** options to see a list of only those apps.

![Filter the list showing All, Custom, Store, Creator Studio, and Fluent options to see the apps you need.](../image/sn-studio-app-filter-ys2.png)

For more filtering options, select **Open list**. Use the classic UI16 list sorting and filtering options to find the list of apps that you need. The **IDE Created** column shows which internal development environment the app was created in.

![In the IDE Created column, find information about which environment your app was created in. This image shows two apps created in Creator Studio and two in ServiceNow Studio.](../image/sn-studio-ide-created.png)

**Parent Topic:**[Change your development experience in ServiceNow Studio](../task/change-your-development-experience.md)

