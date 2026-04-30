---
title: Plan before you build
description: Essentially, an application is a digital program that supports user tasks. Some actions you take when building an application might be irreversible. Be aware of these actions and plan for them in advance.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Plan your application development, Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Plan before you build

Essentially, an application is a digital program that supports user tasks. Some actions you take when building an application might be irreversible. Be aware of these actions and plan for them in advance.

## Agentic AI

Create applications with help from agentic AI. For more information, see [Use AI capabilities in custom applications](../../ai-capabilities/concept/use-ai-capabilities-in-custom-apps.md).

## Application scope

One of the first major decisions to make when creating an application is: Should the application be in a private scope or a global scope?

By default, applications are created in their own private application scope. Applications in a private application scope restrict access to their application artifacts so only application artifacts in the same scope have full access to create, modify, remove, or run application data. Scoped applications can use source control integration and delegated development. Globally scoped applications cannot use delegated development.

Create custom business applications in scope unless:

-   The application has to delete global data.
-   The application needs to change application access settings on multiple default tables to function.
-   The application needs to access APIs only available in the global scope. Creating a globally scoped passthrough script include would not be enough for this requirement.

**Note:** Globally scoped passthrough is a script include created in a global scope that is accessible from the private scope. The passthrough gives access to a global API that is not accessible by default from a private application scope.

For more information, see [Application scope](../../applications/concept/c_ApplicationScope.md) and [Understanding Application Scope on the ServiceNow AI Platform \(Whitepaper\)](https://www.servicenow.com/community/developer-articles/understanding-application-scope-on-the-now-platform-whitepaper/ta-p/2326214).

## Instance selection

Proof of Concept \(PoC\) application builds can and should be built in a separate instance from a regular development instance. The instance can be a sandbox instance or a Personal Developer Instance \(PDI\) from the [Developer Site](https://developer.servicenow.com/). The PDI naming format is **dev12345.service-now.com**.

If using an instance with a different scope namespace, rebuild the PoC applications in the organization’s development instance. Do not import the applications into the organization's development instance. The scoped namespace for the applications will not match the scoped namespace for the company’s development instance.

Applications the organization intends to use \(i.e. production apps\) should be created in the organization’s developer instance, so the application can follow the organization’s testing and deployment process.

## Naming decisions

The application name matters. ServiceNow suggests a scope based on the application’s name. Application file names are appended to the scope to uniquely identify application resources in an instance. Scope is in the format: x\_\[company code\]\_\[application\_name\] with a maximum of 18 characters. For example, an application name **Legal Request** has a suggested scope of **x\_acme\_legal\_reque**.

All application files within the application inherit the scope, so carefully consider what the value should be. The application name can always be changed.

**Parent Topic:**[Plan your application development](plan-your-app-development.md)

