---
title: Self service
description: Your application may need a way for end users to be able to access your data model, so there are self-service options available.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create design elements, Build your application, Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Self service

Your application may need a way for end users to be able to access your data model, so there are self-service options available.

## Service Portal

If the application has Requestor or Self-Service users, use Service Portal to provide a friendly web experience.

To give self-service users the ability to easily create application records from the Service Portal, create a [record producer](https://servicenow.com/docs/bundle/paris-servicenow-platform/page/product/service-catalog-management/task/t_CreatingRecordProducersFromTables.html). A record producer can provide a better end-user experience than a regular form. Talk to your ServiceNow Administrator about the appropriate catalog and categorization to make the record producer accessible through the Service Portal.

Alternatively, create a Service Portal for your app if the following is true:

The application needs different branding, navigation, or user experience than an organization’s current Service Portal.

**OR**

The organization does not have an existing Service Portal.

**AND**

The application needs more functionality than the default portals provide.

**AND**

The application requires a more customized user experience than the default forms and lists can provide.

**OR**

The application needs more control over branding and themes than the default interface provides.

**Tip:** Do not try to reuse any existing service portal pages in an application. Create new pages and then reuse components in your pages, such as widgets and headers.

## Widgets

Widgets are what define the portal content. The base system widgets provided with Service Portal can be used, or developers can build custom widgets to fit business needs.

Considerations for creating custom Service Portal widgets for an application:

-   Start from an existing widget instead of creating a widget from scratch. To protect existing widgets from accidental modifications, all baseline widgets are read-only.
-   When developing a widget, use the preview pane to quickly test the widget's behavior. Always test the widget on a portal page before releasing a widget to production.
-   Use third-party debugging tools when debugging browser-based applications. For example, the [ng-inspector Chrome extension for Angular JS](https://chrome.google.com/webstore/detail/ng-inspector-for-angularj/aadgmnobpdmgmigaicncghmmoeflnamj?hl=en).
-   Avoid the use of $rootScope.$broadcast\(\). Instead, use $rootScope.$emit\(\) to publish an event to the rootscope.
-   Use widget options to make widgets more easily reusable. The widget option schema defines the user-configurable fields.
-   For field types not supported in the option schema, create an extension table to store a custom widget option schema.
-   Make use of Angular Providers, which are reusable components that can be injected into multiple widgets. To ensure quick loading widgets and a high performing portal, create Angular Providers instead of overloading your client controllers with persistent data and additional logic. With Angular Providers, you can maintain data for the lifetime of your Service Portal and reuse components and data objects across multiple widgets.

For more information, see [Service Portal training](https://developer.servicenow.com/dev.do#!/learn/courses/utah/app_store_learnv2_serviceportal_utah_service_portal).

**Parent Topic:**[Create design elements](create-design-elements.md)

