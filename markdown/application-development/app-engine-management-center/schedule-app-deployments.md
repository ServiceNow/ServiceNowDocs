---
title: Schedule app deployments in AEMC
description: Schedule apps to deploy to production at a future time to load balance your systems using the App Engine Management Center \(AEMC\).
locale: en-US
release: zurich
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage deployments, Use, App Engine Management Center, Governing app development, Building applications]
---

# Schedule app deployments in AEMC

Schedule apps to deploy to production at a future time to load balance your systems using the App Engine Management Center \(AEMC\).

## Before you begin

Role required: admin or app\_engine\_admin

## About this task

Deploying apps through your pipelines requires a certain amount of processing power. Depending on the needs of your organization, you may want to schedule deployments to happen when less processing power is needed elsewhere or when it's generally more convenient.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Administration** &gt; **App Engine Management Center**.

2.  On the **Requests** page, select the deployment request for an application that is ready to go to your production environment.

3.  Select **Deploy app**.

4.  Either deploy your app now or set up a future deployment time.

    -   To deploy now, select **Deploy**.
    -   To deploy in the future, select **Schedule for later**.
5.  If you scheduled the deployment for later, use the date and time picker to select when you want your app to deploy, select **OK**, and select **Deploy**.

    The Activity stream shows the deployment details and the version of the app that will be deployed at the selected date and time. The app is deployed within fifteen minutes of the selected deployment time. If you want to change this time frame, update how often the deployment workflow checks for a scheduled deployment record by navigating to **All** &gt; **System Definition** &gt; **Scheduled Jobs** &gt; **Scheduled Deployments**.

6.  Select **Save**.


**Parent Topic:**[Managing deployments using Pipelines and Deployments](../concept/manage-deployments-using-p-and-d-aemc.md)

