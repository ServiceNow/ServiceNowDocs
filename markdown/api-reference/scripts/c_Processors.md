---
title: Processors
description: Processors provide a customizable URL endpoint that can execute arbitrary server-side JavaScript code and produce output such as TEXT or JSON. Creating custom processors is deprecated.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Processors

Processors provide a customizable URL endpoint that can execute arbitrary server-side JavaScript code and produce output such as TEXT or JSON. Creating custom processors is deprecated.

**Note:** This feature is deprecated. While legacy, existing custom processors continue to be supported, creating new custom processors has been deprecated. Instead, use the [Scripted REST APIs](../../../integrate/custom-web-services/concept/c_CustomWebServices.md).

**Warning:** When creating a processor, ensure that you use parameter names that are specific to your processor. For example, if your processor exports a list of legal records, and a necessary parameter is the recipient's email address, don't use “email” as the parameter name. Create a more processor specific parameter name, such as legal\_export\_recipient\_email. Failure to do so, and using instance parameter names, such as id, table, sys\_id, service, catalog\_id, or view \(and others\), can cause unexpected results.

## When to create processors

Do not create custom processors. This feature is deprecated. Please use the REST APIs instead of creating custom processors. The remaining information is left for existing processors only.

## Processor form

<table id="table_ck2_yr2_sr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the processor.

</td></tr><tr><td>

Type

</td><td>

Programming language of the processor script.

 Options include:

 -   java: do not select this option
-   script

</td></tr><tr><td>

Application

</td><td>

Application containing this record.

</td></tr><tr><td>

Active

</td><td>

Flag to enable or disable the record.

</td></tr><tr><td>

CSRF protect

</td><td>

Option to protect the processor from running unless the instance uses a CSRF token.

</td></tr><tr><td>

Description

</td><td>

Description of the processor's function or purpose.

</td></tr><tr><td>

Parameters

</td><td>

List of available input parameters.

 Specify parameter values in the URL as **&lt;parameter name&gt;=&lt;parameter value&gt;**.

 **Note:** Parameter names must be processor-specific. Do not choose common parameter names that another processor might use. If you use a common parameter name, such as `id`, `sys_id` or `table` in a processor, it can break other functionality, since the processor wins when that parameter exists in a URL. For example, a processor with an `id` parameter, regardless of the Path value in the same record, breaks the Service Portal, which depends on that parameter for page identification.

</td></tr><tr><td>

Path

</td><td>

URI path used to call this processor.

 Call a processor from the URL as:

 `https://<instance name>.service-now.com/<Path>.do`

</td></tr><tr><td>

Script

</td><td>

Immediately Invoked Function Expression to run when the system calls this processor.

 The function automatically provides input parameters for the following API objects.

 -   g\_request
-   g\_response
-   g\_processor

</td></tr><tr><td>

Protection policy

</td><td>

Policy to use to protect this record's script.

 Options include:

 -   None
-   Read-only
-   Protected

</td></tr></tbody>
</table>-   **[Processor API components](../reference/r_ProcessorAPIComponents.md)**  
Processors have access to dedicated API classes, objects, and methods.
-   **[Secure and protect a processor](../task/t_SecureAProcessor.md#)**  
You can protect your processor against unauthorized use by using role restrictions, and protect it by requiring a CSRF token.
-   **[Create a simple processor](../../../app-store/dev_portal_learning/dev_platform_intro/task/t_CreateSimpleProcessor.md)**  
Create a simple processor to execute a script from a URL query. This feature is deprecated.
-   **[Create a multi-table processor](../../../app-store/dev_portal_learning/dev_platform_intro/task/t_CreateMultiTableProcessor.md)**  
Create a multi-table processor that reports the number of rows in any table on your instance. This feature is deprecated.
-   **[Create a custom processor](../../server-scripting/task/t_CreatingACustomProcessor.md)**  
Create a custom processor to execute a script from a URL query. This feature is deprecated.

**Parent Topic:**[Server-side scripting](../../server-scripting/concept/c_ServerScripting.md)

