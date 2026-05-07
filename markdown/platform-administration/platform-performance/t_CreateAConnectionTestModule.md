---
title: Add a module to test connection speed
description: A connection test can indicate the connection speed between your computer and your instance. A connection speed test \(/connection\_test.do\) is available as a UI page.
locale: en-US
release: australia
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resolve issues, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Add a module to test connection speed

A connection test can indicate the connection speed between your computer and your instance. A connection speed test \(/connection\_test.do\) is available as a UI page.

## Before you begin

Role required: admin

## Procedure

1.  Perform the appropriate action for your version of the UI.

<table id="choicetable_bbq_5lz_hfc"><thead><tr><th align="left" id="d64047e54">

UI version

</th><th align="left" id="d64047e57">

Steps

</th></tr></thead><tbody><tr><td id="d64047e63">

**Core UI**

</td><td>

1.  Navigate to **System Definition** &gt; **Application Menus**.
2.  Open the application menu to which you want to add the module, for example, **System Diagnostics**.


</td></tr><tr><td id="d64047e94">

**UI15**

</td><td>

Select and hold \(or right-click\) an application menu, such as **System Diagnostics**, and select **Edit Application Menu** or the pencil icon.

</td></tr></tbody>
</table>2.  Select **New** in the list of modules.

3.  Complete the Module form using the following values:

    -   **Title**: Unique name such as `Connection Test`
    -   **Link type**: **URL \(from Arguments\)**
    -   **Arguments**: `connection_test.do`
4.  Select **Submit**.


**Parent Topic:**[Resolving platform performance issues](../concept/resolving-plat-performance-issues.md)

