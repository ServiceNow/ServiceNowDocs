---
title: Configure OAuth credentials for use in Pipelines and Deployments
description: Use OAuth credentials in your pipelines to add another level of security to your pipeline. This task helps you create and configure OAuth credentials for use in your pipelines.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/app-engine-studio/configure-oauth-credentials-pipelines-deployments.html
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure environment credentials, Pipelines and Deployments configuration tasks, Configure Pipelines and Deployments, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Configure OAuth credentials for use in Pipelines and Deployments

Use OAuth credentials in your pipelines to add another level of security to your pipeline. This task helps you create and configure OAuth credentials for use in your pipelines.

## Before you begin

In the top right corner of your instance, make sure you set the application scope to **Global**. Open all your instances \(development, test, production, and the like\) in separate browser tabs. The following tasks lay out the steps for a three-instance environment. However, if you use any other non-production instances \(stage, and the like\), there are steps that detail where you may need to repeat a task on that instance.

Role required: admin

## About this task

Creating and connecting OAuth credentials consists of several tasks that must be completed in the order laid out. Pay close attention to make sure you're in the correct instance for each step. For more information, see [OAuth 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-security/authentication/c_OAuthApplications.md).

## Procedure

1.  Complete all of the steps under [Create OAuth API endpoints for external clients](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/create-oauth-api-endpoints-for-external-clients.md) on the specified instances.

2.  Complete all of the steps under [Create third-party OAuth provider records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/create-third-party-oauth-provider-records.md) on the specified instances.

3.  Complete all of the steps under [Use OAuth to create pipeline credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/use-oauth-to-create-pipeline-credentials.md) on the specified instances.


## What to do next

When you [Configure your pipeline environments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/config-pipeline-environments.md), make sure you select the correct instance credential records for the instance you're configuring.

-   **[Create OAuth API endpoints for external clients](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/create-oauth-api-endpoints-for-external-clients.md)**  
Create OAuth API endpoints to enable your controller instance to have two-way communication with your non-production instances. Follow and complete each step carefully on the specified instances before moving on to create your third-party OAuth provider records.
-   **[Create third-party OAuth provider records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/create-third-party-oauth-provider-records.md)**  
Create third-party OAuth provider records to enable each of your instances to access the API endpoints you've created.
-   **[Use OAuth to create pipeline credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/use-oauth-to-create-pipeline-credentials.md)**  
Create credential records on each of your instances to enable OAuth use in your pipeline.

**Parent Topic:**[Configure environment credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/create-pipeline-credentials.md)

