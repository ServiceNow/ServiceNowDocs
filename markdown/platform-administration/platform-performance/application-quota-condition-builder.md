---
title: Application quota condition builder
description: A description of the options available in the condition builder for the Application Quota Rule form.
locale: en-US
release: xanadu
product: Platform Performance
classification: platform-performance
topic_type: reference
last_updated: "2025-05-09"
reading_time_minutes: 1
breadcrumb: [Platform performance reference, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Application quota condition builder

A description of the options available in the condition builder for the Application Quota Rule form.

<table id="table_cgn_hw1_rp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attributes

</td><td>

Miscellaneous attributes that are related to the transaction.

</td></tr><tr><td>

Created

</td><td>

When the transaction was created.

</td></tr><tr><td>

Created by

</td><td>

Who created the transaction.

</td></tr><tr><td>

Foreground

</td><td>

Whether the transaction was completed in the foreground or background:-   True: a foreground transaction.
-   False: a background transaction.

</td></tr><tr><td>

Homepage

</td><td>

The homepage that is running. This value is populated only if the URL is `home.do`.

</td></tr><tr><td>

Homepage Widget

</td><td>

The homepage widget that is rendered in the transaction. When a homepage is rendered initially, each homepage widget is rendered in parallel.

</td></tr><tr><td>

Initial Scope Name

</td><td>

Scope where the method that created the transaction is defined. Setting this name to anything other than the selected application means that the rule is never used. The rule only looks at transactions of the selected application, and this value has the rule look for a different application, so the condition is never satisfied.

</td></tr><tr><td>

Scope Name

</td><td>

Scope of the application that called the method that created the transaction.

</td></tr><tr><td>

Sys ID

</td><td>

A sys\_id of the transaction.

</td></tr><tr><td>

Thread Name

</td><td>

The name of the execution thread that is running the transaction. Foreground threads have names like `http-bio-8080-exec-1`. Background threads may have various names, and may be useful where the URL is not sufficiently descriptive.

</td></tr><tr><td>

Type

</td><td>

The type of transaction:-   **List**: Any list transaction, such as incident\_list.do.
-   **Form**: All forms, UI pages, CMS pages, and so on.
-   **XMLHttp**: Transactions that run through GlideAjax, where the URL is xmlhttp.do.
-   **Report**: The page `sys_report_template.do`.
-   **SOAP**: SOAP transactions.
-   **Export**: When a list is exported in a format such as XML, Excel.
-   **Scheduler**: When a scheduled job is performed.
-   **Text Search**: The text search transaction or any of its related operations.
-   **Other**: Any type that does not meet the qualities of another type.

 **Note:** Match the transaction quota **Type** to the transaction type listed in the Quota Manager [log entry for the transaction](../task/t_EnableDebuggingInformation.md).

</td></tr><tr><td>

URL

</td><td>

The URL of the page.

</td></tr><tr><td>

Updated

</td><td>

When the transaction was updated.

</td></tr><tr><td>

Updated by

</td><td>

Who updated the transaction.

</td></tr><tr><td>

Updates

</td><td>

What was updated.

</td></tr><tr><td>

User

</td><td>

The user performing the transaction.

</td></tr></tbody>
</table>**Parent Topic:**[Platform performance reference](../concept/platform-performance-references.md)

