---
title: Publish a custom integration profile
description: Publish a custom integration profile to complete the custom integration.
locale: en-US
release: yokohama
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SaaS License Connections, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Publish a custom integration profile

Publish a custom integration profile to complete the custom integration.

## Before you begin

Make sure that all actions and subflows are published in ServiceNow® Workflow Studio before adding them to the integration profile.

Role required: sam\_integrator or admin

## Procedure

1.  Navigate to **All** &gt; **SaaS License** &gt; **Administration** &gt; **All Integration Profiles** and select the custom integration profile that you created.

2.  In the Download Subscription Subflow form section, select the Download Subscriptions subflow for the SaaS application.

3.  Click **Publish**.

    A software model is automatically created for the SaaS application. A scheduled job is created to immediately run the Download Subscription Subflow, which adds user subscriptions for the SaaS application to the Software Subscription table \[samp\_sw\_subscription\].

4.  In the Calculate Activity Subflow form section, select the Update User Activity subflow for the SaaS application.

    **Note:** The scheduled job to get user subscriptions must finish before you can add the Update User Activity subflow.

5.  Choose a value for the **Analyze user activity from** field.

    You can choose to start analyzing data from the current date or from up to 60 days in the past. Choosing a date in the past enables you to detect stale subscriptions without waiting in real time because you can see subscriptions that haven't been used recently. Because choosing a date in the past increases the amount of data that is analyzed, it could take several hours for you to be able to view the results.

    This value is passed as the **Look back time** input for the subflow to get user activity.

6.  In the Reclaim Subscription Subflow form section, select the Reclaim Subscription subflow for the SaaS application.

7.  Click **Save**.


## What to do next

Reclamation rules and stale user reclamation candidates are created automatically after the integration is connected. User subscriptions and reclamation candidates are refreshed daily.

It's important that you review all automatically generated reclamation rules to ensure that they meet your specifications for reclaiming user subscriptions. For more information, see [Review a software reclamation rule](add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track software used against software owned. For more information, see [Create entitlements in Software Asset Management classic](track-software-rights.md).

