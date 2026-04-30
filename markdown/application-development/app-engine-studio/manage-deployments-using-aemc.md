---
title: Managing deployments using pipelines in AEMC
description: Manage applications at all stages of deployment, view multiple pipelines, and approve or reject deployment requests using the App Engine Management Center \(AEMC\).Schedule apps to deploy to production at a future time to load balance your systems using the App Engine Management Center \(AEMC\).Change the details of a deployment request in App Engine Management Center \(AEMC\).Cancel a scheduled app deployment in App Engine Management Center \(AEMC\) if you no longer need to deploy the app to production. Canceling the scheduled deployment request cancels the scheduled deployment and also the entire request itself.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Managing app development using the App Engine Management Center, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Managing deployments using pipelines in AEMC

Manage applications at all stages of deployment, view multiple pipelines, and approve or reject deployment requests using the App Engine Management Center \(AEMC\).

The Active deployment requests in the pipeline section of the AEMC Overview page shows the number of apps at each deployment stage within each of your pipelines. You can select **Show all requests**, **Show requests**, or **Show published requests** next to the corresponding sections to see an overview of each group of requests.

![Pipelines in each stage of deployment](../image/pipeline.png)

For a full picture of all your pipeline deployment requests, access the Pipelines page in AEMC. View all of your pipelines, quickly access each deployment request record, and filter each pipeline section to see only the requests that match your criteria.

![Show and filter deployment requests on the Pipelines page](../image/pipeline-show-requests.png)

## Change Management integration

You can integrate an existing Change Management program with your app deployment processes to add oversight into your deployments and have apps deploy according to a scheduled Change window. For more information, see [Manage deployment requests](../task/manage-deployment-requests.md).

**Parent Topic:**[Managing app development using the App Engine Management Center](monitor-requests-using-aemc.md)

## Schedule app deployments in AEMC

Schedule apps to deploy to production at a future time to load balance your systems using the App Engine Management Center \(AEMC\).

### Before you begin

Role required: admin or app\_engine\_admin

### About this task

Deploying apps through your pipelines requires a certain amount of processing power. Depending on the needs of your organization, you may want to schedule deployments to happen when less processing power is needed elsewhere or when it's generally more convenient.

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Administration** &gt; **App Engine Management Center**.

2.  On the **Requests** page, select the deployment request for an application that is ready to go to your production environment.

3.  Select **Deploy app**.

4.  Either deploy your app now or set up a future deployment time.

    -   To deploy now, select **Deploy**.
    -   To deploy in the future, select **Schedule for later**.
5.  If you scheduled the deployment for later, use the date and time picker to select when you want your app to deploy, select **OK**, and select **Deploy**.

    The Activity stream shows the deployment details and the version of the app that will be deployed at the selected date and time. The app is deployed within fifteen minutes of the selected deployment time. If you want to change this time frame, update how often the deployment workflow checks for a scheduled deployment record by navigating to **All** &gt; **System Definition** &gt; **Scheduled Jobs** &gt; **Scheduled Deployments**.

6.  Select **Save**.


## Update a deployment request in AEMC

Change the details of a deployment request in App Engine Management Center \(AEMC\).

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Administration** &gt; **App Engine Management Center**.

2.  On the **Requests** page, select the deployment request that you want to update.

3.  On the **Scheduled Deployments** tab, select the deployment record you want to update.

4.  In the **Scheduled Deployment Date** field, select an updated date and time for the app to deploy to production.

5.  Select **Save**.


## Cancel a scheduled deployment in AEMC

Cancel a scheduled app deployment in App Engine Management Center \(AEMC\) if you no longer need to deploy the app to production. Canceling the scheduled deployment request cancels the scheduled deployment and also the entire request itself.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Administration** &gt; **App Engine Management Center**.

2.  On the **Requests** page, select the deployment request that you want to update.

3.  On the deployment request, select **Cancel deployment**.


