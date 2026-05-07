---
title: ServiceNow Studio instance strategy
description: ServiceNow Studio should be available on all ServiceNow instances where you develop applications.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Installing ServiceNow Studio, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# ServiceNow Studio instance strategy

ServiceNow Studio should be available on all ServiceNow instances where you develop applications.

You’ll need to establish your company's instance strategy for ServiceNow Studio. Some of the decisions you need to make include:

-   Whether you want to enable anyone within your company to have access to ServiceNow Studio to start building apps.
-   Whether you want to grant access to a select group of people.
-   Whether you want to grant access on a case-by-case basis by setting up a form where individuals can complete information about the app that they’re looking to build. Your admin then decides whether to give those individuals access to build that app.

A non-production instance that is similarly configured to your production instance may be the best candidate for your test environment. You can then more accurately find issues that may arise if the application is deployed to production.

**Note:** If you plan on cloning your production instance to one or more non-production instances, you should also install the ServiceNow Studio product on your production instance prior to cloning. For more information, see [Instance Clone](https://www.servicenow.com/docs/access?context=system-clone-landing&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

After you have established your instance strategy, you must also complete the following tasks.

1.  Establish and automate your approval or review process.
2.  Decide which non-production environment ServiceNow Studio will run on. Because ServiceNow Studio is a product that runs on your non-production environment, you need to select one to run it on.
3.  Determine which method to use for promoting apps from a particular non-production instance to your test instance, and then finally to production where the app will be running live. You can deploy apps using update sets, pipelines, or the Application Repository in ServiceNow Studio.

**Parent Topic:**[Installing ServiceNow Studio](installing-servicenow-studio.md)

