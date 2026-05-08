---
title: Configure OAuth credentials for use in Pipelines and Deployments
description: Use OAuth credentials in your pipelines to add another level of security to your pipeline. This task helps you create and configure OAuth credentials for use in your pipelines.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure environment credentials, Configuration tasks, Configure Pipelines and Deployments, Configure, App Engine Management Center, Governing app development, Building applications]
---

# Configure OAuth credentials for use in Pipelines and Deployments

Use OAuth credentials in your pipelines to add another level of security to your pipeline. This task helps you create and configure OAuth credentials for use in your pipelines.

## Before you begin

In the top right corner of your instance, make sure you set the application scope to **Global**. Open all your instances \(development, test, production, and the like\) in separate browser tabs. The following tasks lay out the steps for a three-instance environment. However, if you use any other non-production instances \(stage, and the like\), there are steps that detail where you may need to repeat a task on that instance.

Role required: admin

## About this task

Creating and connecting OAuth credentials consists of several tasks that must be completed in the order laid out. Pay close attention to make sure you're in the correct instance for each step. For more information, see OAuth 2.0.

## Procedure

1.  Complete all of the steps under [Create OAuth API endpoints for external clients](create-oauth-api-endpoints-for-external-clients.md) on the specified instances.

2.  Complete all of the steps under [Create third-party OAuth provider records](create-third-party-oauth-provider-records.md) on the specified instances.

3.  Complete all of the steps under [Use OAuth to create pipeline credentials](use-oauth-to-create-pipeline-credentials.md) on the specified instances.


## What to do next

When you [Configure your pipeline environments](config-pipeline-environments.md), make sure you select the correct instance credential records for the instance you're configuring.

