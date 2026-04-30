---
title: Manage deployment requests
description: Review and approve or reject deployment requests in the App Engine Studio App Engine Management Center \(AEMC\) as applications move from development to production.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing requests using AEMC, Managing app development using the App Engine Management Center, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Manage deployment requests

Review and approve or reject deployment requests in the App Engine Studio App Engine Management Center \(AEMC\) as applications move from development to production.

## Before you begin

Role required: sn\_app\_eng\_notify.app\_engine\_admin

## About this task

To view deployment requests in AEMC, pipelines must be configured correctly. For details, see [Configure Pipelines and Deployments](../../pipelines-and-deployments/task/config-p-and-d.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Administration** &gt; **App Engine Management Center**.

    The AEMC dashboard shows the number of deployment requests.

    **Note:** To view a list of all deployment requests, either select the number of requests or select the Requests page.

2.  Select a deployment request to review its details.

    ![Pending deployment request record](../image/deployment-record-vs2.png "Pending deployment request record")

3.  Review the details of the deployment request, including details about the application, the developer who requested deployment, and the deployment process.

    At the top of each deployment request, you can see the current position of the app in the pipeline.

    **Note:** If the request is in a testing environment, you can review the Automated Test Framework \(ATF\) test and instance scan results in the Activity stream or on the **Deployment Environment Results** tab.

4.  Review the notes and application activity for the app manifest and any important details the developer may have added.

5.  If a different App Engine Studio \(AES\) admin must review the deployment request, update the request assignee and select **Save**.

6.  Approve or reject the request.

    -   To move the application to the next deployment stage, select **Approve &amp; Deploy app**.
    -   If you have integrated your existing Change Management processes with AEMC, select **Approve &amp; Create Change Request**. This action creates a change request, which can be seen and monitored on the **Change Requests** tab.
    -   If the application is not ready or could potentially cause issues if it was moved on to the next deployment stage, select **Reject**. Add **Work notes** to identify the reasons for the rejection and any changes required to make the application ready for deployment.
    **Note:** Unless you are assigned a Change Management role, most of the information on the **Change Request** tab is read-only. You can monitor the change request and see as it changes states. However, if you have Change Management permissions, you may be able to update certain fields on the change request such as the planned start and end date or the state.


**Parent Topic:**[Managing requests using AEMC](../concept/manage-aemc-requests.md)

