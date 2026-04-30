---
title: Form logic
description: Controlling what users see when they visit a form can increase productivity and responsiveness. For example, users should only see fields that are useful to them. Users may only need to see certain fields based on what is configured on the form. Apply form logic to control what is visible, read-only, and mandatory on a form.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Build form and business logic, Build your application, Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Form logic

Controlling what users see when they visit a form can increase productivity and responsiveness. For example, users should only see fields that are useful to them. Users may only need to see certain fields based on what is configured on the form. Apply form logic to control what is visible, read-only, and mandatory on a form.

## Agentic AI

Create applications with help from agentic AI. For more information, see [Use AI capabilities in custom applications](../../ai-capabilities/concept/use-ai-capabilities-in-custom-apps.md).

## Determine when to control user access

The following question will help direct you to the right decision for when to control user access to information: Is this a suggestion or enforcement? A suggestion makes the form easier to complete whereas enforcement forces the user to do something in order to complete the form.

UI policies are useful for conditional suggestions like showing and hiding fields or adding field messages based on another field’s value, while Data policies and Business Rules are better suited for doing conditional enforcement like making a field mandatory.

The best user experience is to utilize both suggestion and enforcement together.

For more information, see the [UI Policy](https://developer.servicenow.com/dev.do#!/learn/courses/paris/app_store_learnv2_scripting_paris_scripting_in_servicenow/app_store_learnv2_scripting_paris_client_side_scripting/app_store_learnv2_scripting_paris_ui_policies) article in the Client-side Scripting Module.

Build UI Policies and Data Policies to handle client-side activities before scripting any client-side logic. Use of Client Scripts to validate user input and provide feedback while the user is completing the form.

Some general practices for client scripting are:

-   Optimize for performance by using asynchronous GlideAjaxover client-side GlideRecordor multiple getReference\(\)calls.
-   Keep the isLoadingcheck in onChangeclient scripts.
-   Keep the newValuecheck and add a newValue != oldValuecheck.
-   Use all client-side scripts possible before making a server call with GlideAjax. Server roundtrips can impact performance.

Some client scripting practices to avoid are:

-   Global Client Scripts or Global UI Scripts: Global scripts will run on every page load and introduce browser load delay.
-   DOM Manipulation: Using document object model manipulation against default UI elements introduces upgrade risk and maintainability issues. The exception is using DOM manipulation against the DOM in pages authored in the same scoped application, like UI Pages or Service Portal widgets.

**Parent Topic:**[Build form and business logic](build-form-and-business-logic.md)

