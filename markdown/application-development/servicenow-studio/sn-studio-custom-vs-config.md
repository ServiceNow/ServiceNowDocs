---
title: Customization vs configuration with ServiceNow Studio
description: There are important differences between customizing and configuring ServiceNow applications. The ServiceNow platform is built to embrace customization and configuration, but how you do so can have significant impacts on ServiceNow support, upgrading to future ServiceNow platform versions, and the functionality of the ServiceNow platform.
locale: en-US
release: xanadu
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-04-22"
reading_time_minutes: 10
breadcrumb: [Exploring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Customization vs configuration with ServiceNow Studio

There are important differences between customizing and configuring ServiceNow applications. The ServiceNow platform is built to embrace customization and configuration, but how you do so can have significant impacts on ServiceNow support, upgrading to future ServiceNow platform versions, and the functionality of the ServiceNow platform.

The general rules around customization are:

-   Customize an application only if it extends the original intent of the application. For example, add IT functionality to ITSM but don’t add a travel workflow. Instead of over-customizing an application, create a new application using App Engine products, such as Creator Studio or ServiceNow Studio.
-   Configure as much as you can before customizing an application.
-   If you add code or make other modifications to out-of-the-box functionality, you own them.

## What is configuration

Configuration is the process of using ServiceNow built-in tools and features to modify an application’s behavior without making changes to flows or the code that is part of the baseline installation on a ServiceNow instance.

Configuration can take the form of using ServiceNow built-in tools to add tables and more, setting instance-wide parameters, as well as using code to extend an application’s functionality to meet business needs as long as the code does not modify the baseline code installation. The entire platform is designed for you to add configuration code.

If you add code, such as workflow scripts, you own it, even if it doesn’t alter the baseline code installation. That includes owning the impact it has on the entire ServiceNow platform. Issues that arise from added code are beyond the scope of ServiceNow support to debug.

Reverting a configuration should not require any change to the baseline code.

Configuration examples include:

-   Forms: Configure tables, fields, data types, default values, and field dependencies to configure the data you capture and display.
-   UI elements: Modify layouts, add related lists, add buttons, and change field names.
-   Service Catalog: Configure portals where your customers can request catalog items such as service and product offerings.
-   ACLs: Restrict unauthorized users from accessing forms and data.
-   System property values: Modify the application’s experience for all users.

## What is customization

Customization is any change made to the flows or the code that is part of the baseline installation on a ServiceNow instance. You use ServiceNow products or code to customize applications.

If you add code, you own it, even if it doesn’t alter the baseline installation. That includes owning the impact it has on the entire ServiceNow platform.

Customization examples include:

-   Scripting: Customize ServiceNow through scripting using JavaScript. This includes creating client scripts, server-side scripts, and business rules with intricate logic that modify the baseline code.
-   Custom tables: Develop custom tables to accommodate specialized data that doesn't fit within standard tables.
-   Integration: Customize integration with external systems, such as APIs and web services, for seamless data exchange.
-   Widgets and portals: Create custom widgets and portals to provide unique features and user experiences.
-   Workflows: Create and modify workflows using Workflow Studio. Create and manage playbooks, flows, actions, decision tables, and integrations from one design environment to automate tasks. Upgrading to a new version of a flow requires reapplying your customizations.

## Tools for customization and configuration

ServiceNow offers many tools and features, such as business rules, to modify the out-of-the-box behavior of ServiceNow applications. Whether they customize or configure an application depends on how they’re used. Using these tools to modify the installed code base constitutes customization. Using these tools to add code that does not modify the flows, or the installed code base constitutes configuration. In both cases, you own the code you add as well as the impact it has on the ServiceNow platform.

ServiceNow tools include:

-   UI Policies: Dynamically modify the visibility of fields and attributes on a form according to user inputs.
-   Business rules: Automatically trigger actions based on specified conditions.
-   UI Actions: Extend and customize forms and lists by adding buttons, context menu items, or other UI elements that perform specific actions when clicked.
-   Client-side scripts: Scripts that execute within the user's browser when certain actions occur on a form or a UI page.
-   Server-side scripts: Scripts that execute on the ServiceNow server or database, for example, to update record fields when a database query runs.

## What is personalization

Personalization is when users use out-of-the-box application tools to modify an application’s look and feel only for themselves. Admins can change the look and feel for all users and that is considered configuration. Personalization examples include a user choosing to use dark mode or choosing which table columns to display.

Personalization does not change the baseline code installation on a ServiceNow instance. So, personalization does not impact customer support or interfere with upgrades to new ServiceNow versions.

## Ramifications of customizing ServiceNow products

The ServiceNow platform is extremely flexible and built to embrace customization and configuration to fulfill a wide range of business requirements. How you customize ServiceNow applications, however, can have significant impacts on ServiceNow support, upgrading to future ServiceNow platform versions, and the functionality of the platform. Instead of customizing ServiceNow applications, consider using App Engine development products, such as Creator Studio and ServiceNow Studio to create new applications.

The ServiceNow platform uses a framework that supports applications in how they process tasks, how forms are rendered in multiple browsers, and the overall user experience. ServiceNow relies on the framework's integrity to develop and provide support in a consistent manner. Customizations can impair this framework, change platform functionality, and impair workflows and upgradeability.

Customizations trigger the platform to create sys\_update\_xml records, which are stored in the Customer Update table. The platform marks all customizations and skips the customized records when you update to a new version of the ServiceNow platform. That means you are responsible for manually updating the customizations. This can have a significant impact on the time and resources required to update to new platform versions.

**Note:** The Customer Update table also contains modifications or additions to configuration metadata, for example, creating a new catalog item or a new workflow.

For more information, see the [Customer Updates table](https://www.servicenow.com/docs/access?context=r_CustomerUpdatesTable&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US). Note that the complexity of maintaining customizations dramatically increases as the number of customizations increases.

Customizing the installed code base can be costly, generate technical debt, lengthen your upgrade cycle, and complicate future platform upgrades because the custom code may not easily migrate to new platform versions. Custom code can change the standard functionality of the ServiceNow platform in unintended ways. Evaluate demands for customization carefully and only resort to customization where there is clear business value and no alternative. Wherever possible, avoid customization by using configuration instead.

If you customize a product:

-   You are responsible for maintaining the customization going forward.
-   Customer Service and Support will not support problems caused by custom code. If it is the cause of the problems, the support team will likely advise you to revert to the out-of-the-box code.

## What is the Customer Service and Support stance on supporting customization

The ServiceNow Customer Service and Support stance on customization is if you add code, you own it and its consequences. Why? Customer Support is not privy to your custom business logic, doesn’t know what the expected behavior should be, is unable to reproduce the issue on an out-of-the-box instance, and customer support engineers are not certified implementation specialists, so they are not certified to review customized code logic.

## Alternatives to customization

If you have requirements and ideas for enhancements, instead of customizing the installed code base, you can:

-   Use configuration instead of customization.
-   Submit an Enhancement Request to the ServiceNow development team. Each request is evaluated and, if approved, will be incorporated into a future release.
-   Create an app using App Engine developer products to handle desired functionality.

## When to use App Engine developer products instead of customizing

When your company needs to add new functionality to the ServiceNow platform, you can customize existing applications, such as ITSM, or create a new application using App Engine developer products, such as Creator Studio or ServiceNow Studio. A simple guideline for which path to choose is:

-   If the customization extends the intended purpose of the application, it works better to customize. For example, you can add IT functionality to ITSM.
-   If the customization doesn’t extend the intended purpose of the application, it works better to create a new application using App Engine developer products. For example, do not repurpose the ITSM workflow to create a travel request workflow.

For example, ITSM is designed to handle IT issues. To customize it to handle travel requests goes beyond the original intention of ITSM. Because IT and travel requests have different workflows, it’s better to create a travel request app using App Engine developer tools, such as Creator Studio and ServiceNow Studio, instead of customizing ITSM.

For more information, see [Use App Engine instead of customizations](use-app-engine-instead-of-customizations.md).

## Examples of when to use App Engine developer products

ServiceNow products work best when they’re used as they were intended. If you find yourself heavily customizing an application to repurpose it, a better plan is to create a new application using App Engine developer products.

The following scenarios demonstrate where creating a new application works better than heavily customizing an existing ServiceNow application:

-   You have a novel use case for an app that doesn’t align with any product workflow.
-   You have a use case that could be built by heavily customizing an out-of-the-box application, but it doesn’t align with what the existing application was intended to do.
-   Your company has a user group or business process that should be separate from the OOTB product workflow.

## Guidelines for customizing ServiceNow products

If you must make a customization, consider the following suggestions:

-   Maximize configuration options first.
-   Avoid copying objects. Instead, update objects in place wherever possible, except for Service Portal widgets and other items designated to be reused.
-   Default to “add before edit.” This means that you should, for example, add fields to forms rather than change the type of an existing field. Avoid using the same names as out-of-the-box objects, methods, or classes when adding them.
-   Minimize the number of fields you add to a form. The more fields you have on a form, the longer it may take to load.
-   Export original records as backups before customizing them. Keep track of their out-of-the-box sys\_id’s in case you must restore them in the future.
-   Use scoped applications as your default for any new custom development.
-   Document all customizations. Add comments explaining why you customized \(including business justification\). Review all comments before upgrading to determine if you can revert to out-of-the-box code.
-   Create tests for all customizations. Write Automated Test Framework \(ATF\) tests for all customizations where possible.
-   Use HealthScan regularly to identify unnecessary customizations.
-   Customizations should be made to baseline objects where necessary so that conflict resolution and decision-making can be appropriately recorded in the updates. Hidden customizations may cause administrators to overlook updates in future assessments in case reverts or merges are necessary.
-   Test your customization for all use cases. Include performance testing and the introduction of unintended consequences.
-   Administrators are responsible for verifying that their customizations work after a ServiceNow platform upgrade, and for keeping track of what customizations are made.

## Handling customizations when you upgrade

Customizations trigger the platform to create sys\_update\_xml records, which are stored in the Customer Updates table. These records are not updated during platform version upgrades. ServiceNow marks them as skipped records in the ServiceNow Upgrade Monitor. To make sure they’re successfully ported to the upgraded instance, you must manually process the skipped changes. For more information, see the [Customer Updates table](https://www.servicenow.com/docs/access?context=r_CustomerUpdatesTable&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

Assuming you’ve documented all your customizations—including the business justification—take your documented inventory and compare it with the skipped records identified in the Upgrade Monitor. After filtering out low-risk changes that have resulted in skipped records \(for example, field labels or form layouts\), you’ll need to decide whether to:

-   Retain each customization
-   Revert to out-of-the-box
-   Merge your customization with the base system to resolve conflicts

