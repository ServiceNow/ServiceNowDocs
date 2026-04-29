---
title: Determining good candidates for apps in ServiceNow
description: Before creating an app in ServiceNow, determine if the idea is a good candidate for an application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Building apps in ServiceNow, Getting Started guide for developers, Building applications]
---

# Determining good candidates for apps in ServiceNow

Before creating an app in ServiceNow, determine if the idea is a good candidate for an application.

Consider the following questions to determine if you should create an application.

-   Can you configure or customize an existing application instead of building a new one? For more information, see [Modifying versus building an application](../../custom-application/concept/modifying-versus-building-an-application.md).
-   How many people will the application serve, and how often would they use it? If not many people would use it frequently, is it worth the effort?
-   Are you willing to maintain the application as things change over time?

If creating a new application makes sense, then move forward.

## Other considerations

There are other considerations you must factor into the decision of creating an app.

-   Configuring and customizing existing applications can lead to complications with upgrading to a new version of the ServiceNow AI Platform. If you customize your applications, you own that code and are responsible for its upkeep.
-   Creating apps in ServiceNow can have licensing and cost implications. Talk with your admin to determine the best course of action.
-   Customer service and tech support may not be able to support custom code and applications because they don't know the expected functionality. Consider this when creating a new application.

## Examples of when to create apps

Instead of customizing an existing application, you can create apps with App Engine products such as ServiceNow Studio. The following situations are great examples of when you could build a new app.

-   Net-new process: You’re building a new process that doesn’t fit neatly into any of the existing modules.
-   Misaligned intent: You have a use case that could be built by customizing an OOTB app. However, it doesn’t align with the app intent.
-   Separate group workflow: ​Your process is unique, proprietary, or spans multiple departments.

**Parent Topic:**[Overview of building apps in ServiceNow](overview-building-apps-in-servicenow.md)

