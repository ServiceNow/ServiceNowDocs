---
title: Managing Creator Studio deployments and monitoring app usage
description: After users create apps, they submit them for you, the admin, to review and deploy. How you deploy them depends on whether you have App Engine Management Center \(AEMC\) installed on the instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/creator-studio/managing-creator-studio-deployments.html
release: australia
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administer, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Managing Creator Studio deployments and monitoring app usage

After users create apps, they submit them for you, the admin, to review and deploy. How you deploy them depends on whether you have App Engine Management Center \(AEMC\) installed on the instance.

## Managing app deployment with AEMC

Apps aren't deployed directly from Creator Studio. Instead, use App Engine Management Center \(AEMC\).

Find details on deploying apps in [App Engine Management Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/app-engine-management-center.md).

## Managing app deployment without AEMC

If you don't have AEMC installed, you can use Pipelines and Deployments and the Deployment Tasks table to publish to the Application Repository. For more information, see [Pipelines and Deployments workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/pipelines-deployments-workflow-vs2.md).

You can view and edit details of the deployment on the **Scheduled Deployments** tab of Pipelines and Deployments For more information, see [Managing deployments using Pipelines and Deployments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/manage-deployments-using-p-and-d-aemc.md).

## Monitoring deployed app usage

After you deploy an app to production, you can monitor its usage, adoption, and response rate, for each request form in the same way that you do for catalog items/record producers or scoped apps.

For example, you can use AEMC to monitor apps. For more information, see [Managing custom apps using AEMC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/manage-custom-apps-using-aemc.md).

**Parent Topic:**[Administering Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/administering-creator-studio.md)

