---
title: Next steps when replatforming apps to ServiceNow using ERP-CM
description: After you use ERP Semantic Mining \(ERP-CM\) to identify legacy ERP \(Enterprise Resource Planning\) candidates, use additional ServiceNow AI Platform products and resources to replatform your app.
locale: en-US
release: yokohama
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Exploring ERP Semantic Mining, ERP Semantic Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Next steps when replatforming apps to ServiceNow using ERP-CM

After you use ERP Semantic Mining \(ERP-CM\) to identify legacy ERP \(Enterprise Resource Planning\) candidates, use additional ServiceNow AI Platform products and resources to replatform your app.

First, identify the customization you want to replatform from the ERP system with ERP-CM.

Then, use the remote tables and extraction tables linked in the candidate mining results for fast access to ERP data.

That ERP data can be used as a data source when you build new apps on the ServiceNow AI Platform, for example, with App Engine Studio.

## Build a ServiceNow app that consumes ERP data

The next step in replatforming with App Engine for ERP \(Enterprise Resource Planning\) is to build an app on the ServiceNow AI Platform that consumes the ERP data.

As you plan to replatform a legacy app on the ServiceNow AI Platform, consider where the data is coming from. For example, an old app may retrieve data from a third party into the system of record. When you build a new, replatformed app on the ServiceNow AI Platform, you can configure the new app to pull data directly from that third party instead of having the Zero Copy Connector for ERP model pull it from the ERP system, which adds an extra step of retrieval.

## Working with similar candidates when replatforming apps

If ERP-CM shows that a candidate has a number of similar candidates, consider building one app that meets the needs of some or all similar candidates when you replatform.

![ERP Semantic Mining candidates page with similar candidates column highlighted.](../image/ecm-similar-candidates.png)

When you replatform a custom app from the system of record, you don't have to replicate the old app exactly. Use the replatforming process to design a better app, perhaps one that addresses the needs of multiple similar candidates in a single, new app built using low-code tools on the ServiceNow AI Platform. App Engine Studio is the quickest app to use, but there are other builders available to you, depending on your licensing.

## ServiceNow low- and pro-code builders

After you identify ERP data to replatform, citizen developers can use ServiceNow builders to create apps quickly from the data. Any custom fields that exist in the ERP system of record, such as SAP, can be leveraged by the apps you build using the ServiceNow AI Platform. For more on citizen development, see [Delegated development and deployment](../../applications/concept/c_DelegatedDevelopment.md).

Use any of the following ServiceNow builders to create apps using custom data:

-   [App Engine Studio](../../app-engine-studio/concept/aes-overview.md)
-   [Flows in Workflow Studio](https://www.servicenow.com/docs/access?context=exploring-flows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)
-   [Playbooks in Workflow Studio](https://www.servicenow.com/docs/access?context=exploring-process-automation-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)
-   [Table Builder](../../../administer/form-builder/concept/tb-landing-page.md)
-   [UI Builder](../../../administer/ui-builder/concept/ui-builder-overview.md)
-   [Workspace Builder](../../app-engine-studio/task/add-workspace.md)

For example, use in App Engine Studio, use a template \(or build the app from the ground up\) and incorporate remote tables using ERP models and remote tables. You can combine legacy data from the ERP models and remote tables with other ServiceNow data in tables.

## Using Glide to query ERP data

You can also access data from the system of record through the Glide API.

For more information, see [Sample Glide query for ERP data in ERP Semantic Mining](../reference/using-glide-to-query-erp-data.md).

## After you replatform custom code to a ServiceNow app

Replatformed apps on the ServiceNow AI Platform use live data from the system of record without writing any code back to it.

After you've identified candidates to replatform and taken the recommended action in ERP-CM, you need to use only Zero Copy Connector for ERP to access the remote tables and extraction tables. These tables are data sources for building apps, flows, and workspaces.

If you're sure that the legacy code on the system of record isn't referenced anywhere else, you can remove it from the system after it's replatformed to a ServiceNow instance.

**Parent Topic:**[Exploring ERP Semantic Mining](exploring-ecm.md)

