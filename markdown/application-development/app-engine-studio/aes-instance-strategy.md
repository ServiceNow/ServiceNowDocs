---
title: AES instance strategy
description: You should install App Engine Studio \(AES\) on all ServiceNow instances where users will develop applications.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Installing App Engine Studio, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# AES instance strategy

You should install App Engine Studio \(AES\) on all ServiceNow instances where users will develop applications.

You will need to establish your company's instance strategy for AES. Some of the decisions you will need to make include:

-   Whether you want to allow anyone within your company to have access to AES to start building apps.
-   Whether you want to grant access to a select group of people.
-   Whether you want to grant access on a case-by-case basis by setting up a form where individuals can complete information about the app that they are looking to build. IT then decides whether to give those individuals access to build that app.

A non-production instance that is similarly configured to your production instance may be the best candidate for your test environment. You can then more accurately find issues that may arise if the application is deployed to production.

**Note:** If you plan on cloning your production instance to one or more non-production instances, you should also install the AES product on your production instance prior to cloning. For more information, see [System clone](https://www.servicenow.com/docs/access?context=c_SystemClone&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) and [Cloning instances with AES](cloning-aes-applications.md).

After you have established your instance strategy, you must also establish and automate your approval or review process. AES is a product that runs on your non-production environment. For an organization with multiple non-production environments, you will need to decide which non-production environment AES will run on. You must also determine which pipeline to use for promoting apps from a particular non-production instance to your test instance, and then finally to production where the app will be running live. For more information, see [Pipelines and Deployments](aes-review-apps-p-and-d.md).

**Parent Topic:**[Installing App Engine Studio](../task/install-aes.md)

