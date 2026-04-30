---
title: Transaction quota rule condition builder
description: A description of the options available in the condition builder for the Transaction Quota Rule form.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Platform performance, Maintain and monitor, Administer]
---

# Transaction quota rule condition builder

A description of the options available in the condition builder for the Transaction Quota Rule form.

<table id="table_cgn_hw1_rp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

URL

</td><td>

The URL of the page.

</td></tr><tr><td>

Thread Name

</td><td>

The name of the execution thread that is running the transaction. Foreground threads have names like http-bio-8080-exec-1. Background threads can have various names, and are useful where the URL is not sufficiently descriptive.

</td></tr><tr><td>

Foreground

</td><td>

Whether the transaction was completed in the foreground or background:-   **True**: a foreground transaction.
-   **False**: a background transaction.

</td></tr><tr><td>

Type

</td><td>

The type of transaction:-   **List**: Any list transaction, such as incident\_list.do.
-   **Form**: All forms, UI pages, CMS pages, and so on.
-   **XMLHttp**: Transactions that run through GlideAjax, where the URL is xmlhttp.do.
-   **Report**: The page`sys_report_template.do`.
-   **SOAP**: SOAP transactions.
-   **Export**: When a list is exported in a format such as XML or Excel.
-   **Scheduler**: When a scheduled job is performed.
-   **Text Search**: The text search transaction or any of its related operations.
-   **Other**: Any type that does not meet the qualities of another type.

 **Note:** Match the transaction quota **Type** to the transaction type listed in the Quota Manager [log entry for the transaction](../task/t_EnableDebuggingInformation.md).

</td></tr><tr><td>

User

</td><td>

The user performing the transaction.

</td></tr><tr><td>

Homepage

</td><td>

The homepage that is running. This condition is populated only if the URL is `home.do`.

</td></tr><tr><td>

Homepage Widget

</td><td>

The widget that is rendered in the transaction. When a homepage or non-responsive dashboard renders, each widget renders in parallel.

 When a responsive dashboard renders, each widget renders in sequence.

 When the quota is exceeded, users see the message: `Widget cancelled - maximum execution time exceeded`. Increase the quota value if you don't want to show this message.

</td></tr><tr><td>

Attributes

</td><td>

Miscellaneous attributes that are related to the transaction.

</td></tr></tbody>
</table>**Parent Topic:**[Platform performance reference](../concept/platform-performance-references.md)

