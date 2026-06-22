---
title: Secure and protect a processor
description: You can protect your processor against unauthorized use by using role restrictions, and protect it by requiring a CSRF token.You can protect a processor by requiring a CSRF token.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/scripts/t\_SecureAProcessor.html
release: zurich
product: Scripts
classification: scripts
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Processors, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Secure and protect a processor

You can protect your processor against unauthorized use by using role restrictions, and protect it by requiring a CSRF token.

## About this task

**Note:** This feature is deprecated. While legacy, existing custom processors continue to be supported, creating new custom processors has been deprecated. Instead, use the [Scripted REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/rest-api-explorer/c_CustomWebServices.md).

You can re-use a table's user role restrictions to protect it from access by your processor. This protection method assumes the processor will access table data.

## Procedure

1.  Create or select a user role that has access to the table the processor script calls.

2.  Navigate to **System Definition** &gt; **Processors**.

3.  In **Script**, add the following code block.

    ```
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


**Parent Topic:**[Processors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/c_Processors.md)

## Protect a processor with a CSRF token

You can protect a processor by requiring a CSRF token.

### About this task

Script type processors can require a CSRF token check before the processor runs.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Processors**.

2.  Open a processor record.

3.  Select the **CSRF protect** option.

4.  Click **Update**.


**Related topics**  


[Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/user-administration/t_AssignARoleToAUser.md)

