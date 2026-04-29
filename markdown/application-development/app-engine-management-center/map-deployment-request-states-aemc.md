---
title: Map deployment request states
description: If your ReleaseOps deployment request has custom states, you must configure the Deployment Request State Map table so that your ReleaseOps deployment request states map to the correct App Engine states.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2025-10-23"
reading_time_minutes: 1
breadcrumb: [Migration tasks, Configure Pipelines and Deployments, Configure, App Engine Management Center, Governing app development, Building applications]
---

# Map deployment request states

If your ReleaseOps deployment request has custom states, you must configure the Deployment Request State Map table so that your ReleaseOps deployment request states map to the correct App Engine states.

## Before you begin

Role required: admin or app\_engine\_admin

## Procedure

1.  On your production instance, navigate to **All** &gt; **App Engine** &gt; **Pipelines and Deployments** &gt; **ReleaseOps State Mapping**.

2.  Select the ReleaseOps deployment request state in the **ReleaseOps DR state** column that you want to update.

    **Important:** It's not recommended to change the mapping of any ReleaseOps deployment request end states, including:

    -   Canceled
    -   Completed
    -   Failed
3.  On the state mapping record page, select the value in the **App Engine DR state** field that corresponds to the ReleaseOps deployment request state.

4.  In the **Notes** field, enter additional details about the state mapping.

5.  Select **Update** or select and hold \(or right-click\) in the header and select **Save** to update the record.

6.  Repeat the procedure in steps 2 through 5 for each deployment request state that you want to update.

7.  To create a deployment request state mapping record, select **New** on the Deployment Request State Maps table.

    You can create a deployment request state mapping record when there are more or new ReleaseOps deployment request states that must be mapped onto corresponding App Engine deployment request states.

    1.  In the **App Engine DR state** field, select the App Engine deployment request state from the list.

    2.  In the **ReleaseOps DR state** field, select the corresponding ReleaseOps deployment request state.

    3.  In the **Notes** field, enter additional details about the state mapping.

    4.  Select **Update** or select and hold \(or right-click\) in the header and select **Save** to update the record.


## Result

You have mapped all ReleaseOps deployment request states onto the corresponding App Engine deployment request states.

## What to do next

If you want to configure additional conditions to enable migration to ReleaseOps, see [Add custom conditions to enable ReleaseOps deployments](add-custom-conditions-to-enable-releaseops-deployment.md).

