---
title: Script processors
description: Processors provide a customizable URL endpoint that can execute arbitrary server-side JavaScript code and produce output such as TEXT or JSON. Creating custom processors is deprecated.Processors have access to dedicated API classes, objects, and methods.You can protect your processor against unauthorized use by using role restrictions, and protect it by requiring a CSRF token.You can protect a processor by requiring a CSRF token.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/c\_Processors.html
release: brazil
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Write server-side scripts, Scripting, API implementation, API implementation and reference]
---

# Script processors

Processors provide a customizable URL endpoint that can execute arbitrary server-side JavaScript code and produce output such as TEXT or JSON. Creating custom processors is deprecated.

**Note:** This feature is deprecated. While legacy, existing custom processors continue to be supported, creating new custom processors has been deprecated. Instead, use the [Scripted REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_CustomWebServices.md).

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
</table>**Parent Topic:**[Writing server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/server-side-scripting-overview.md)

## Processor API components

Processors have access to dedicated API classes, objects, and methods.

|Class, object, or method|Description|
|------------------------|-----------|
|`g_response`|An object of type HttpServletResponse. See [GlideServletResponse](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideServletResponseScopedAPI.md).|
|`setContentType(‘text/html;charset=UTF-8’)`|A [GlideServletResponse](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideServletResponseScopedAPI.md) method to set the content type of the response being sent to the client.|
|`g_request`|An object of type HttpServletRequest. See [HttpServletRequest](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideServletRequestScopedAPI.md).|
|`getParameter()`|A glide method to get the value of a URL parameter.|
|`canRead()`|A GlideRecord method to determine if the user can read data from a table. See [GlideRecord](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideRecordScopedAPI.md).|
|`g_processor`|A simplified servlet for processors. See [GlideScriptedProcessor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideScriptedProcessorScopedAPI.md).|
|`writeOutput()`|A [GlideScriptedProcessor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideScriptedProcessorScopedAPI.md) method to display information on the client.|
|`g_target`|An object containing the target table name of a processor URL. For example, a processor containing the URI `incident.do` applies to the Incident table.|

## Secure a script processor against unauthorized access

You can protect your processor against unauthorized use by using role restrictions, and protect it by requiring a CSRF token.

### About this task

**Note:** This feature is deprecated. While legacy, existing custom processors continue to be supported, creating new custom processors has been deprecated. Instead, use the [Scripted REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_CustomWebServices.md).

You can re-use a table's user role restrictions to protect it from access by your processor. This protection method assumes the processor will access table data.

### Procedure

1.  Create or select a user role that has access to the table the processor script calls.

2.  Navigate to **System Definition** &gt; **Processors**.

3.  In **Script**, add the following code block.

    ```javascript
    var now_GR = new GlideRecord('your_table_name');
    // canRead() compares the table’s ACL to the user making this request, and returns true if the logged-in user has read access to this table
    if(gr.canRead())  
    { 
      // Perform table query here  
      g_processor.writeOutput('Success!'); 
    } else { 
      g_processor.writeOutput('You do not have permission to read table your_table_name'); 
    }
    ```

4.  Update the code block to use other access restrictions as needed.

    Available access functions include:

    -   canCreate\(\)
    -   canRead\(\)
    -   canWrite\(\)
    -   canDelete\(\)
5.  Click **Update**.


### Protect a processor with a CSRF token

You can protect a processor by requiring a CSRF token.

#### About this task

Script type processors can require a CSRF token check before the processor runs.

#### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Processors**.

2.  Open a processor record.

3.  Select the **CSRF protect** option.

4.  Click **Update**.


**Related topics**  


[Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_AssignARoleToAUser.md)

