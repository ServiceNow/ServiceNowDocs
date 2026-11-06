---
title: Customization vs configuration with ServiceNow Studio
description: There are important differences between customizing and configuring ServiceNow applications. The ServiceNow platform is built to embrace customization and configuration, but how you do so can have significant impacts on ServiceNow support, upgrading to future ServiceNow platform versions, and the functionality of the ServiceNow platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/servicenow-studio-classic/sn-studio-custom-vs-config.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 10
breadcrumb: [Explore, ServiceNow Studio, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Customization vs configuration with ServiceNow Studio

There are important differences between customizing and configuring ServiceNow applications. The ServiceNow platform is built to embrace customization and configuration, but how you do so can have significant impacts on ServiceNow support, upgrading to future ServiceNow platform versions, and the functionality of the ServiceNow platform.

The general rules around customization are:

-   Customize an application only if it extends the original intent of the application. For example, add IT functionality to ITSM but don’t add a travel workflow. Instead of over-customizing an application, create a new application using App Engine products, such as Creator Studio or ServiceNow Studio.
-   Configure as much as you can before customizing an application.
-   If you add code or make other modifications to out-of-the-box functionality, you own them.

## What is configuration?

Configuration is the process of using ServiceNow built-in tools and features to modify an application’s behavior without changing flows or the code in the baseline installation on a ServiceNow instance.

Configuration can include using ServiceNow built-in tools to add tables, setting instance-wide parameters, and using code to extend an application’s functionality to meet business needs, as long as the code does not modify the baseline code installation. The entire platform is designed for you to add configuration code.

If you add code, such as workflow scripts, you own it, even if it does not alter the baseline code installation. You also own the impact it has on the entire ServiceNow platform. Debugging issues that arise from added code is beyond the scope of ServiceNow support.

Reverting a configuration should not require any change to the baseline code.

Configuration examples include:

-   Forms: Configure tables, fields, data types, default values, and field dependencies to control the data you capture and display.
-   UI elements: Modify layouts, add related lists, add buttons, and change field names.
-   Service Catalog: Configure portals where your customers can request catalog items such as service and product offerings.
-   ACLs: Restrict unauthorized users from accessing forms and data.
-   System property values: Modify the application’s experience for all users.

## What is customization?

Customization is any change to the flows or the code in the baseline installation on a ServiceNow instance. You use ServiceNow products or code to customize applications.

If you add code, you own it, even if it does not alter the baseline installation. You also own the impact it has on the entire ServiceNow platform.

Customization examples include:

-   Scripting: Customize ServiceNow through scripting using JavaScript. This includes creating client scripts, server-side scripts, and business rules with intricate logic that modify the baseline code.
-   Custom tables: Develop custom tables to store specialized data that does not fit in standard tables.
-   Integration: Customize integration with external systems, such as APIs and web services, to enable data exchange.
-   Widgets and portals: Create custom widgets and portals to provide unique features and user experiences.
-   Workflows: Create and modify workflows using Workflow Studio. Create and manage playbooks, flows, actions, decision tables, and integrations from one design environment to automate tasks. Upgrading to a new version of a flow requires reapplying your customizations.

## Which tools support customization and configuration?

ServiceNow offers many tools and features, such as business rules, to modify the out-of-the-box behavior of ServiceNow applications. Whether a tool customizes or configures an application depends on how you use it. Using these tools to modify the installed code base is customization. Using these tools to add code that does not modify the flows or the installed code base is configuration. In both cases, you own the code you add and the impact it has on the ServiceNow platform.

ServiceNow tools include:

-   UI Policies: Dynamically modify the visibility of fields and attributes on a form according to user inputs.
-   Business rules: Automatically trigger actions based on specified conditions.
-   UI Actions: Extend and customize forms and lists by adding buttons, context menu items, or other UI elements that perform specific actions when users select them.
-   Client-side scripts: Scripts that run in the user’s browser when certain actions occur on a form or a UI page.
-   Server-side scripts: Scripts that run on the ServiceNow server or database, for example, to update record fields when a database query runs.

## What is personalization?

Personalization is when users use out-of-the-box application tools to modify an application’s look and feel only for themselves. When admins change the look and feel for all users, that change is configuration. Personalization examples include a user choosing dark mode or choosing which table columns to display.

Personalization does not change the baseline code installation on a ServiceNow instance. As a result, personalization does not affect customer support or interfere with upgrades to new ServiceNow versions.

## What are the ramifications of customizing ServiceNow products?

The ServiceNow platform is flexible and supports customization and configuration to fulfill a wide range of business requirements. However, how you customize ServiceNow applications can significantly affect ServiceNow support, upgrades to future ServiceNow platform versions, and platform functionality. Use App Engine development products, such as Creator Studio and ServiceNow Studio, to create new applications instead of customizing ServiceNow applications.

The ServiceNow platform uses a framework that supports how applications process tasks, how forms render in multiple browsers, and the overall user experience. ServiceNow relies on the integrity of this framework to develop and provide support consistently. Customizations can impair this framework, change platform functionality, and impair workflows and upgradeability.

Customizations trigger the platform to create sys\_update\_xml records, which are stored in the Customer Update table. When you update to a new version of the ServiceNow platform, the platform marks all customizations and skips the customized records. You are responsible for manually updating the customizations, which can significantly affect the time and resources required to update to new platform versions.

**Note:** The Customer Update table also contains modifications or additions to configuration metadata, for example, creating a new catalog item or a new workflow.

For more information, see the Customer Updates table. The complexity of maintaining customizations increases significantly as the number of customizations increases.

Customizing the installed code base can be costly, generate technical debt, lengthen your upgrade cycle, and complicate future platform upgrades, because custom code might not migrate easily to new platform versions. Custom code can change the standard functionality of the ServiceNow platform in unintended ways. Evaluate demands for customization carefully, and customize only when there is clear business value and no alternative. Wherever possible, use configuration instead of customization.

If you customize a product:

-   You are responsible for maintaining the customization going forward.
-   Customer Service and Support does not support problems caused by custom code. If custom code causes the problems, the support team is likely to advise you to revert to the out-of-the-box code.

## What is the Customer Service and Support stance on supporting customization?

The ServiceNow Customer Service and Support stance on customization is that if you add code, you own it and its consequences. Customer Support cannot support custom code for these reasons:

-   Customer Support is not familiar with your custom business logic.
-   Customer Support does not know the expected behavior of custom code.
-   Customer Support cannot reproduce the issue on an out-of-the-box instance.
-   Customer support engineers are not certified implementation specialists, so they are not certified to review customized code logic.

## What alternatives exist to customization?

If you have requirements and ideas for enhancements, use one of these alternatives instead of customizing the installed code base:

-   Use configuration instead of customization.
-   Submit an Enhancement Request to the ServiceNow development team. The team evaluates each request and incorporates approved requests into a future release.
-   Create an app using App Engine developer products to handle the desired functionality.

## When should you use App Engine developer products instead of customizing?

To add new functionality to the ServiceNow platform, customize an existing application, such as ITSM, or create a new application with App Engine developer products, such as Creator Studio or ServiceNow Studio. Use this guideline to choose a path:

-   Customize an existing application if the customization extends the application’s intended purpose. For example, add IT functionality to ITSM.
-   Create a new application with App Engine developer products if the customization does not extend the application’s intended purpose. For example, do not repurpose the ITSM workflow to create a travel request workflow.

For example, ITSM is designed to handle IT issues. Customizing it to handle travel requests goes beyond the original intention of ITSM. Because IT and travel requests have different workflows, create a travel request app using App Engine developer tools, such as Creator Studio and ServiceNow Studio, instead of customizing ITSM.

For more information, see [Use App Engine instead of customizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-studio-classic/use-app-engine-instead-of-customizations.md).

## What are examples of when to use App Engine developer products?

ServiceNow products work best when you use them as intended. If you heavily customize an application to repurpose it, create a new application with App Engine developer products instead.

Create a new application instead of heavily customizing an existing ServiceNow application in these scenarios:

-   You have a novel use case for an app that does not align with any product workflow.
-   You have a use case that you could build by heavily customizing an out-of-the-box application, but it does not align with the intended purpose of that application.
-   Your company has a user group or business process that needs to be separate from the out-of-the-box product workflow.

## What guidelines apply when customizing ServiceNow products?

If you must make a customization, follow these guidelines:

-   Maximize configuration options first.
-   Avoid copying objects. Instead, update objects in place wherever possible, except for Service Portal widgets and other items designated for reuse.
-   Follow the “add before edit” principle. For example, add fields to forms instead of changing the type of an existing field. Avoid using the same names as out-of-the-box objects, methods, or classes when you add them.
-   Minimize the number of fields you add to a form. The more fields a form has, the longer it can take to load.
-   Export original records as backups before customizing them. Keep track of their out-of-the-box sys\_id values in case you must restore them in the future.
-   Use scoped applications as your default for any new custom development.
-   Document all customizations. Add comments explaining why you customized, including the business justification. Review all comments before upgrading to determine whether you can revert to out-of-the-box code.
-   Create tests for all customizations. Write Automated Test Framework \(ATF\) tests for all customizations where possible.
-   Use HealthScan regularly to identify unnecessary customizations.
-   Make customizations to baseline objects where necessary, so that you can record conflict resolution and decision-making in the updates. Hidden customizations can cause administrators to overlook updates in future assessments if reverts or merges are necessary.
-   Test your customization for all use cases. Include performance testing and testing for unintended consequences.
-   Administrators are responsible for verifying that their customizations work after a ServiceNow platform upgrade and for tracking the customizations they make.

## How do you handle customizations when you upgrade?

Customizations trigger the platform to create sys\_update\_xml records, which are stored in the Customer Updates table. Platform version upgrades do not update these records. ServiceNow marks them as skipped records in the ServiceNow Upgrade Monitor. To make sure the records port successfully to the upgraded instance, manually process the skipped changes. For more information, see the [Customer Updates table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_CustomerUpdatesTable.md).

If you have documented all your customizations, including the business justification, compare your documented inventory with the skipped records identified in the Upgrade Monitor. After you filter out low-risk changes that resulted in skipped records, such as field labels or form layouts, decide whether to:

-   Retain each customization
-   Revert to out-of-the-box
-   Merge your customization with the base system to resolve conflicts

