---
title: Use App Engine instead of customizations
description: App Engine development tools offer an excellent alternative to customizing existing ServiceNow AI Platform applications.
locale: en-US
release: xanadu
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-01-23"
reading_time_minutes: 4
breadcrumb: [Exploring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Use App Engine instead of customizations

App Engine development tools offer an excellent alternative to customizing existing ServiceNow AI Platform applications.

When your company needs to add new functionality to the ServiceNow AI Platform, you can customize existing applications, such as IT Service Management \(ITSM\), or create a new application using App Engine developer products, such as App Engine Studio, Creator Studio, or ServiceNow Studio. A simple guideline for which path to choose is:

-   If the customization extends the intended purpose of the application, it works better to customize. For example, you can add IT functionality to ITSM.
-   If the customization doesn’t extend the intended purpose of the application, it works better to create a new application using App Engine developer products. For example, do not repurpose the ITSM workflow to add a travel request workflow.

## Examples of when to use App Engine

ServiceNow products work best when they’re used as they were intended. If you find yourself heavily customizing an application to repurpose it, a better plan is to create a new application using App Engine developer products.

The following scenarios demonstrate where creating a new application works better than heavily customizing an existing ServiceNow application:

-   Your company has a business process that augments existing product functionality but doesn’t follow the same workflow exactly.
-   You have a novel use case for an app that doesn’t align with any product workflow.
-   You have a use case that could be built by heavily customizing an out-of-the-box application, but it doesn’t align with what the existing application was intended to do.

Let’s dive deeper into the last use case.

## Issues with repurposing existing products

ServiceNow applications come with roles, processes, and flows that are specially tailored to their use case. For example, ITSM apps help with IT users, IT issues, IT reports, and IT cases.

You might have an idea for an app that’s similar to but doesn't exactly align with ITSM. Because ITSM gives you a starting point, you might be tempted to customize ITSM to add the new functionality. For example, ITSM tracks IT issues, and a travel app you want to create might track travel requests. While the workflows sound similar, in fact, they use very different data, different user interfaces, and the details of each workflow vary greatly. Rather than heavily customize ITSM to repurpose it, a better plan is to use App Engine developer products for the following reasons:

-   Combining two workflows creates conflicts.
-   Customizing applications has implications.

## Combining two workflows creates conflicts

In the ITSM example, the repurposing of ITSM to include a travel workflow uses different data, different tables, different roles, and different workflows than ITSM. As ITSM, ITSM customizations, and the travel workflow grow over time:

-   Their features will continue to diverge.
-   Adding new functionality or fixing problems in one workflow might adversely impact the other.
-   The performance of ITSM may suffer.
-   The code base will grow and the two purposes of ITSM will make troubleshooting more difficult.
-   Quality engineers will require two different testing frameworks.

All these issues may cause unnecessary complications, poorer performance, upgrade delays, and software problems.

## Customizing applications has implications

The ServiceNow AI Platform is built to embrace customization and configuration. The ServiceNow AI Platform is flexible enough to fit your company’s business needs. How you customize ServiceNow applications, however, can have significant impacts on ServiceNow support, upgrading to future ServiceNow AI Platform versions, and the functionality of the platform.

Let’s start by differentiating customization and configuration:

-   Customization is any change made to the code that is part of the baseline installation of a ServiceNow instance. You use code to customize applications.
-   Configuration is any change you make to the behavior of a product that does not touch the code in the baseline installation of a ServiceNow instance. You can use system properties, ServiceNow products, or code to configure an application.

The following are some of the implications that result from customizing applications:

-   If you add code to an application, you own it whether or not it modifies the code in the baseline installation on a ServiceNow instance.
-   The platform marks all customizations and skips them when you update to a new version of the platform. That means you are responsible for manually updating the customizations. This can have a significant impact on the time and resources required to update to new platform versions.
-   The ServiceNow AI Platform uses a framework that supports applications in how they process tasks, how forms are rendered in multiple browsers, and the overall user experience. Introducing customizations can have unintended consequences on this framework.
-   You own the burden of testing custom code and determining if it impacts platform functionality.
-   ServiceNow Customer Support cannot troubleshoot custom code or issues caused by custom code.

Customization is one of the key features of the ServiceNow AI Platform. However, over-customizing an application to repurpose it is likely to generate technical debt, lengthen your upgrade cycle, and complicate future platform upgrades because the custom code may not easily migrate to new platform versions.

## Conclusion

Customization and configuration are hallmarks of the ServiceNow AI Platform that enable your company to customize workflows to fit its specific needs. Proceed with these tasks in the following order:

1.  Configure ServiceNow applications as much as you can before customizing them.
2.  Customize an application only when it extends the intent of the application.
3.  Use App Engine developer products, such as App Engine Studio, Creator Studio, and ServiceNow Studio, to create new applications rather than customizing an application to create functionality that doesn’t align with its original purpose.

For more information, see [Customization vs configuration with ServiceNow Studio](sn-studio-custom-vs-config.md).

