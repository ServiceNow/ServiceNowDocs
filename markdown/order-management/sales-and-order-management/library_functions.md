---
title: Library functions
description: Library functions can speed implementation and reduce maintenance costs by enabling code reuse across rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/library\_functions.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up enrichments and rules scripting, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Library functions

Library functions can speed implementation and reduce maintenance costs by enabling code reuse across rules.

Library functions enable efficient code reuse across rules and enrichments. They are designed to minimize redundant logic, speed up implementation, and reduce maintenance costs, especially in complex scenarios that involve high-SKU or physics-driven configurations.

## Attributes and capabilities

Centralized management: Search and manage library functions through a dedicated UI.

Reusable and namespaced: Define a library function once and invoke it using `fn.functionName(params)`.

Configurable parameters: Define input parameters with data types and default values. Parameter schemas can be modified post-creation, allowing flexibility in managing function inputs.

Customized output: Specify return types.

Callable across modules: Library functions are callable in both the configurator and Transaction Manager.

Managed table queries: Library functions support managed table lookups.

## Enabling library functions

Submit a support ticket to enable library functions.

**Note:** Submit a support ticket by using the [ServiceNow Support portal](https://support.servicenow.com). For step-by-step instructions, see [Create a case on Now Support for CPQ \(Logik.ai\) Customers](https://support.servicenow.com/kb?sys_kb_id=d67d3e71475d7a90f64de825126d4326&id=kb_article_view).

Once library functions are enabled, turn on the new UI by navigating to **Utilities** &gt; **Settings** &gt; **Admin Version** &gt; **New**, and clicking **Save**.

This setting can be toggled at any time.

## Supported input/output data types

|Type|Description|
|----|-----------|
|TEXT|Plain text strings|
|NUMBER|Numeric values|
|BOOLEAN|Logical true/false values|
|DATE|Dates \(without time component\)|
|JSON OBJECT|JSON formatted objects|
|ARRAY|Ordered collections of values|

**Note:** Empty MAP or ARRAY types are not supported. Unsupported types default to TEXT.

## Usage examples

Library functions can be found in the function library \(in the Utilities section\).

\[Omitted image "cpq-library-functions-function-library.png"\] Alt text: Function library

To add a function:

1.  On the Function Library tab, click **Add Function**.
2.  Name the function, specify the return type, and enter a description.

Script content:

\[Omitted image "cpq-library-functions-script-content.png"\] Alt text: Sccript parameters

Calling the function:

\[Omitted image "cpq-library-functions-calling-the-function.png"\] Alt text: Code

## Limitations

-   Recursive calls are not supported.
-   External API calls and async operations are not supported.
-   Parameters are passed by copy, not by reference.
-   Functions must be free of side effects, external calls, and Logik field references.

## General guidelines

-   When a library function changes, redeploy the affected blueprints.
-   When defining a function, name and describe its inputs to provide visibility into its usage.

