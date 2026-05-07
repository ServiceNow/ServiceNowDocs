---
title: Next steps when replatforming apps to ServiceNow using ERP Semantic Mining
description: After you use ERP Semantic Mining to identify legacy ERP \(Enterprise Resource Planning\) candidates, use additional ServiceNow AI Platform products and resources to replatform your app.
locale: en-US
release: australia
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, ERP Semantic Mining overview, Workflow Data Fabric]
---

# Next steps when replatforming apps to ServiceNow using ERP Semantic Mining

After you use ERP Semantic Mining to identify legacy ERP \(Enterprise Resource Planning\) candidates, use additional ServiceNow AI Platform products and resources to replatform your app.

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

First, identify the customization you want to replatform from the ERP system with ERP Semantic Mining.

Then, use the remote tables and extraction tables linked in the candidate mining results for fast access to ERP data.

That ERP data can be used as a data source when you build new apps on the ServiceNow AI Platform, for example, with ServiceNow Studio.

## Build a ServiceNow app that consumes ERP data

The next step in replatforming with ServiceNow Studio for ERP \(Enterprise Resource Planning\) is to build an app on the ServiceNow AI Platform that consumes the ERP data.

As you plan to replatform a legacy app on the ServiceNow AI Platform, consider where the data is coming from. For example, an old app may retrieve data from a third party into the system of record. When you build a new, replatformed app on the ServiceNow AI Platform, you can configure the new app to pull data directly from that third party. Using that method, the Zero Copy Connector for ERP model no longer pulls the data from the ERP system, which adds an extra step of retrieval.

## Working with similar candidates when replatforming apps

If ERP Semantic Mining shows that a candidate has a number of similar candidates, consider building one app that meets the needs of some or all similar candidates when you replatform.

When you replatform a custom app from the system of record, you don't have to replicate the old app exactly. Use the replatforming process to design a better app. For example, an app that addresses the needs of multiple similar candidates in a single, new app built using low-code tools on the ServiceNow AI Platform. ServiceNow Studio is the quickest app to use, but there are other builders available to you, depending on your licensing.

## ServiceNow low- and pro-code builders

After you identify ERP data to replatform, citizen developers can use ServiceNow builders to create apps quickly from the data. Any custom fields that exist in the ERP system of record, such as SAP, can be leveraged by the apps you build using the ServiceNow AI Platform.

Use any of the following ServiceNow builders to create apps using custom data:

-   [ServiceNow Studio](https://www.servicenow.com/docs/access?context=servicenow-studio-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Workflow Studio flows, subflows, and actions](https://www.servicenow.com/docs/access?context=workflow-studio-flows-subflows-and-actions-landing&version=australia&pubname=australia-build-workflows&ft:locale=en-US)
-   [Workflow Studio playbooks](https://www.servicenow.com/docs/access?context=workflow-studio-playbooks-landing&version=australia&pubname=australia-build-workflows&ft:locale=en-US)
-   [Table Builder](https://www.servicenow.com/docs/access?context=tb-landing-page&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Workspace Builder](https://www.servicenow.com/docs/access?context=workspace-builder-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)

For example, use in ServiceNow Studio, use a template \(or build the app from the ground up\) and incorporate remote tables using ERP models and remote tables. You can combine legacy data from the ERP models and remote tables with other ServiceNow data in tables.

## Using Glide to query ERP data

You can also access data from the system of record through the Glide API.

For more information, see [Sample Glide query for ERP data in ERP Semantic Mining](../reference/using-glide-to-query-erp-data.md).

## After you replatform custom code to a ServiceNow app

Replatformed apps on the ServiceNow AI Platform use live data from the system of record without writing any code back to it.

After you have identified candidates to replatform and taken the recommended action in ERP Semantic Mining, you must only use Zero Copy Connector for ERP to access the remote tables and extraction tables. These tables are data sources for building apps, flows, and workspaces.

If you're sure that legacy code on the system of record isn't referenced elsewhere, you can remove it from the system after it's replatformed.

**Parent Topic:**[Exploring ERP Semantic Mining](exploring-ecm.md)

