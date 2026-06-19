---
title: Viewing app origination information in ServiceNow Studio
description: View app origination information on the App details page in ServiceNow Studio to determine where an app was created and which environment to use for editing and deployment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/viewing-app-origination-information-in-sns.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-05-27"
reading_time_minutes: 2
breadcrumb: [Change your development experience, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Viewing app origination information in ServiceNow Studio

View app origination information on the App details page in ServiceNow Studio to determine where an app was created and which environment to use for editing and deployment.

## What does the App details page show?

Each App details page shows whether the app was created in Creator Studio or created in ServiceNow IDE and converted to Fluent. Apps created in ServiceNow Studio do not display a badge. This information determines whether the app can continue to be edited and deployed through ServiceNow Studio, or whether it must be opened and deployed in a different environment.

\[Omitted image "sn-studio-crs-badge.png"\] Alt text: The app details page shows badges for AI, Creator Studio, and Fluent to let you know where the app was created and may need to be deployed.

## How do I edit an app created in Creator Studio?

Only apps created in Creator Studio can be edited in Creator Studio. Creator Studio supports only a subset of the metadata supported in ServiceNow Studio.

Open an app in Creator Studio by selecting the more options icon \[Omitted image "sn-studio-more-options-icon.png"\] Alt text: on the Navigator panel or the App details page and selecting **Open with Creator Studio**. For more information, see [Building apps with Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/building-apps-with-creator-studio.md).

\[Omitted image "sn-studio-open-in-crs.png"\] Alt text: Option to open the current app in Creator Studio from the Navigator panel.

\[Omitted image "sn-studio-open-w-creator-studio.png"\] Alt text: Option to open the current app in Creator Studio from the App details page.

## How do I deploy an app created in ServiceNow IDE?

Apps created in ServiceNow IDE can be edited in ServiceNow Studio.

**Important:** Apps created in ServiceNow IDE or converted to Fluent cannot be deployed from ServiceNow Studio. Deploy these apps using the ServiceNow IDE.

When you see the **Fluent** badge on an app, follow the normal app deployment process used in the ServiceNow IDE. For more information, see [Developing applications with the ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/developing-applications-servicenow-ide.md).

## How do I filter apps by origination environment?

Access Creator Studio or Fluent apps using the filter in the Apps section of the Navigator panel. Select the **Creator Studio** or **Fluent** options to display only those apps.

\[Omitted image "sn-studio-app-filter-ys2.png"\] Alt text: Filter the list showing All, Custom, Store, Creator Studio, and Fluent options to see the apps you need.

For more filtering options, select **Open list**. Use the classic UI16 list sorting and filtering options to find the apps you need. The **IDE Created** column shows which internal development environment the app was created in.

\[Omitted image "sn-studio-ide-created.png"\] Alt text: In the IDE Created column, find information about which environment your app was created in. This image shows two apps created in Creator Studio and two in ServiceNow Studio.

**Parent Topic:**[Change your development experience in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/change-your-development-experience.md)

