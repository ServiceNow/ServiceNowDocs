---
title: ServiceNow application repository
description: After you develop and test a custom application, you can make the application available to company instances by publishing it to the ServiceNow application repository.
locale: en-US
release: zurich
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Application sharing, Administer your apps, Deploying applications, Building applications]
---

# ServiceNow application repository

After you develop and test a custom application, you can make the application available to company instances by publishing it to the ServiceNow application repository.

The ServiceNow application repository is a central repository for all scoped applications that are published by all ServiceNow customers.

**Note:** The ServiceNow application repository isn’t available for self-hosted \(on premise\) customers.

The application repository enables ServiceNow customers to upload and distribute applications between their instances. When you access the application repository, you can see and manage only the applications that are published by your own organization. You can't see or manage applications that are published by other organizations.

After you have designed, developed, and successfully tested a custom application, you can publish your application to the ServiceNow application repository to share it to other instances in your company.

## Entitlements

An entitlement refers to permission given to an instance to install a scoped application from the application repository. An instance must be entitled to an application in order for you to be able to install the application on the instance.

By default, after you publish an application to the application repository, all your company instances are entitled to the application automatically. To limit which company instances are entitled to the application, access the application repository by going to [https://apprepo.service-now.com/sn\_appstore\_store.do](https://apprepo.service-now.com/sn_appstore_store.do), and then change the entitlement type for the application. You can also entitle an instance again if the application entitlement has already been removed. For more information, see [Manage application entitlements from the application repository](../task/manage-app-entitlements.md).

## Using the application repository

You can access the application repository by going to [https://apprepo.service-now.com](https://apprepo.service-now.com).

**Note:** Customers using the Federal Store must log in to HIWave and then select the Federal Store option at the bottom of the page. Then, under your company name, select My Repository to proceed.

After you [publish an application to the application repository](../task/t_PublishAppsToTheAppRepository.md), you can:

-   [Install an application from the application repository](../task/install-app-from-repo.md)
-   [Manage application entitlements from the application repository](../task/manage-app-entitlements.md)
-   [Delete an application from the application repository](../task/delete-custom-app.md)
-   [Release a scope from the application repository](../task/release-scope.md)

