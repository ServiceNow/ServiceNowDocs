---
title: Publish app changes to the Application Repository from ServiceNow Studio
description: Publish app changes from ServiceNow Studio to the Application Repository \(App Repo\) so your updates are available to all instances of your application.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Studio quick start, Explore, ServiceNow Studio, Developing your application, Building applications]
---

# Publish app changes to the Application Repository from ServiceNow Studio

Publish app changes from ServiceNow Studio to the Application Repository \(App Repo\) so your updates are available to all instances of your application.

## Before you begin

Role required: admin or delegated\_developer

## About this task

The App Repo is one deployment option available in ServiceNow. You can also [create update sets](qs-create-update-set.md) to publish changes. If your company has a deployment pipeline configured, you can deploy changes through the pipeline in ServiceNow Studio. For more information about the App Repo, see [ServiceNow application repository](../../applications/concept/app-repo.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Open the **App details** page for the application you want to update.

    -   On the ServiceNow Studio home page, select the **Deployment** tab, select **Applications**, then select your application from the **Name** column.
    -   In the Navigator panel, select the Apps icon ![Apps icon](../image/sn-studio-app-nav-icon.png), select your application, then select **App details**.
3.  On the App details page, select **Publish**.

4.  In the **New version** field, enter a version number for the changes.

5.  In the **Release notes** field, enter notes about the changes you are publishing.

6.  Select **Publish**.

    Your changes are submitted for review and approval. After approval, your updates are available to all instances of your application.


