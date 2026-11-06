---
title: Use App Engine instead of customizations
description: Use App Engine development tools to extend the ServiceNow AI Platform without customizing existing applications. Building a new app preserves upgrade compatibility and keeps your changes isolated and easier to maintain.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/servicenow-studio-classic/use-app-engine-instead-of-customizations.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Explore, ServiceNow Studio, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Use App Engine instead of customizations

Use App Engine development tools to extend the ServiceNow AI Platform without customizing existing applications. Building a new app preserves upgrade compatibility and keeps your changes isolated and easier to maintain.

To add new functionality to the ServiceNow AI Platform, customize an existing application, such as IT Service Management \(ITSM\), or create a new application with App Engine developer products, such as App Engine Studio, Creator Studio, or ServiceNow Studio. Use this guideline to choose a path:

-   Customize an existing application if the customization extends the application’s intended purpose. For example, add IT functionality to ITSM.
-   Create a new application with App Engine developer products if the customization does not extend the application’s intended purpose. For example, do not repurpose the ITSM workflow to add a travel request workflow.

## When should you use App Engine?

ServiceNow products work best when you use them as intended. If you heavily customize an application to repurpose it, create a new application with App Engine developer products instead.

Create a new application instead of heavily customizing an existing ServiceNow application in these scenarios:

-   Your company has a business process that augments existing product functionality but does not follow the same workflow exactly.
-   You have a novel use case for an app that does not align with any product workflow.
-   You have a use case that you could build by heavily customizing an out-of-the-box application, but it does not align with the intended purpose of that application.

The following sections examine the last scenario in more detail.

## What issues does repurposing existing products cause?

ServiceNow applications include roles, processes, and flows tailored to their use case. For example, ITSM apps support IT users, IT issues, IT reports, and IT cases.

An app idea might be similar to ITSM but not align with it exactly. Because ITSM provides a starting point, it can be tempting to customize ITSM to add the new functionality. For example, ITSM tracks IT issues, and a travel app might track travel requests. The workflows sound similar, but they use different data and different user interfaces, and the details of each workflow vary greatly. Use App Engine developer products instead of heavily customizing ITSM to repurpose it, for these reasons:

-   Combining two workflows creates conflicts.
-   Customizing applications has implications.

## Why does combining two workflows create conflicts?

In the ITSM example, repurposing ITSM to include a travel workflow requires different data, tables, roles, and workflows than ITSM uses. As ITSM, the ITSM customizations, and the travel workflow grow over time:

-   Their features continue to diverge.
-   Adding new functionality or fixing problems in one workflow can adversely affect the other.
-   ITSM performance can suffer.
-   The code base grows, and the two purposes of ITSM make troubleshooting more difficult.
-   Quality engineers need two different testing frameworks.

These issues can cause unnecessary complications, poorer performance, upgrade delays, and software problems.

## What are the implications of customizing applications?

The ServiceNow AI Platform supports both customization and configuration and is flexible enough to fit your company’s business needs. However, how you customize ServiceNow applications can significantly affect ServiceNow support, upgrades to future ServiceNow AI Platform versions, and platform functionality.

Customization and configuration differ as follows:

-   Customization is any change to the code in the baseline installation of a ServiceNow instance. You use code to customize applications.
-   Configuration is any change you make to the behavior of a product that does not touch the code in the baseline installation of a ServiceNow instance. You can use system properties, ServiceNow products, or code to configure an application.

Customizing applications has these implications:

-   If you add code to an application, you own it, whether or not it modifies the code in the baseline installation on a ServiceNow instance.
-   The platform marks all customizations and skips them when you update to a new version of the platform. You are responsible for manually updating the customizations, which can significantly affect the time and resources required to update to new platform versions.
-   The ServiceNow AI Platform uses a framework that supports how applications process tasks, how forms render in multiple browsers, and the overall user experience. Customizations can have unintended consequences on this framework.
-   You are responsible for testing custom code and determining whether it affects platform functionality.
-   ServiceNow Customer Support cannot troubleshoot custom code or issues caused by custom code.

Customization is a key feature of the ServiceNow AI Platform. However, over-customizing an application to repurpose it is likely to generate technical debt, lengthen your upgrade cycle, and complicate future platform upgrades, because custom code might not migrate easily to new platform versions.

## What is the recommended order for customization and configuration?

Customization and configuration let your company tailor workflows to its specific needs on the ServiceNow AI Platform. Follow this order:

1.  Configure ServiceNow applications as much as you can before customizing them.
2.  Customize an application only when it extends the application’s intent.
3.  Use App Engine developer products, such as App Engine Studio, Creator Studio, and ServiceNow Studio, to create new applications rather than customizing an application to create functionality that does not align with its original purpose.

For more information, see [Customization vs configuration with ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-studio-classic/sn-studio-custom-vs-config.md).

