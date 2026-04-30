---
title: Release a scope from the application repository
description: Release a scope from the application repository so that the scope can be used to create new scoped applications.
locale: en-US
release: xanadu
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage applications, ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Release a scope from the application repository

Release a scope from the application repository so that the scope can be used to create new scoped applications.

## Before you begin

You can release an application scope only if the scope isn't being used by any application. If your scope is being used by an application, follow the steps in [Delete an application from the application repository](delete-custom-app.md) before releasing the scope.

Role required: Primary customer admin of the account

## About this task

The application repository stores the scopes of all your custom applications. You cannot create a new application using a scope that is being stored in the application repository. To release a scope means to remove the scope from the application repository so that you can create new applications using the scope.

## Procedure

1.  Go to [https://apprepo.service-now.com](https://apprepo.service-now.com).

2.  Log in using your HI credentials.

3.  **Note:** Customers using the Federal Store must log in to HIWave and then select the Federal Store option at the bottom of the page. Then, under your company name, select My Repository to proceed.

4.  Open the Scopes tab.

5.  Next to the scope listing, click the trash icon \(![Trash icon](../../app-engine-studio/image/trash-icon.png)\).


