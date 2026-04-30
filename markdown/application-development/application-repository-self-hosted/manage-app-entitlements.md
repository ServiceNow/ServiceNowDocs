---
title: Manage application entitlements from the application repository
description: Add or remove application entitlements to limit which instances the application can be installed on.
locale: en-US
release: yokohama
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage applications, ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Manage application entitlements from the application repository

Add or remove application entitlements to limit which instances the application can be installed on.

## Before you begin

You can manage only the applications that you've published to the application repository. For more information, see [Publish an application to the application repository](t_PublishAppsToTheAppRepository.md).

Role required: none

## About this task

By default, after you publish an application to the application repository, all your company instances are entitled to the application automatically. To limit which company instances are entitled to the application, access the application repository by going to [https://apprepo.service-now.com/sn\_appstore\_store.do](https://apprepo.service-now.com/sn_appstore_store.do), and then change the entitlement type for the application. You can also entitle an instance again if the application entitlement has already been removed.

## Procedure

1.  Go to [https://apprepo.service-now.com/sn\_appstore\_store.do](https://apprepo.service-now.com/sn_appstore_store.do).

2.  Log in using your Now Support credentials.

3.  **Note:** Customers using the Federal Store must log in to HIWave and then select the Federal Store option at the bottom of the page. Then, under your company name, select My Repository to proceed.

4.  Next to the application listing, click **Select Action** and then click **Manage Entitlements**.

5.  Choose an entitlement type for your application.

    |Option|Description|
    |------|-----------|
    |**Remove all existing entitlements**|None of your company instances can install the application.|
    |**Entitle all instances**|Any of your company instances can install the application. This option is selected by default when you publish an application to the application repository.|
    |**Entitle selected instances**|Only instances that you select can install the application. Pick which instances to entitle by moving instances from the **Available Instances** list to the **Selected Instances** list.|

6.  Select **OK**.


