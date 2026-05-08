---
title: Debug UI customizations for a Service Catalog page
description: Perform the health check of a Service Catalog page. The UI Page Customization Diagnostics window displays the UI macros applicable for the Service Catalog page and their corresponding states. For issues on a Service Catalog page due to customized UI macros, you can identify the source of broken functionality.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Debugging Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Debug UI customizations for a Service Catalog page

Perform the health check of a Service Catalog page. The UI Page Customization Diagnostics window displays the UI macros applicable for the Service Catalog page and their corresponding states. For issues on a Service Catalog page due to customized UI macros, you can identify the source of broken functionality.

## Before you begin

Role required: admin or catalog\_admin.

Watch this seven-minute video to learn more about UI customization debugging, variable action logger, variable watcher, and the Item Diagnostic report.Features available for debugging Service Catalog issues including UI macro customization debugging; variable action logger; variable watcher; item diagnostic report

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Debug UI Customization**.

    The UI Page Customization Diagnostics window is enabled.

2.  Navigate to a Service Catalog page that you want to debug.

3.  Review the information in the UI Page Customization Diagnostics window at the bottom of the page.

    To maximize the UI Page Customization Diagnostics window, click ![Icon to maximize the window](../image/MaxUICustWndw.png). The following information is displayed:

    -   Name of the current Service Catalog page.
    -   State of the Service Catalog page.
    -   All UI macros applicable for the Service Catalog page.
    -   State of each UI macro. For details on possible states, click the Help icon \(![Help icon](../image/Help.png)\).
    -   Number of occurrences of each UI macro in the Service Catalog page.
<table id="table_n2s_cql_xz"><thead><tr><th>

State

</th><th>

Color indicator

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Unchanged

</td><td>

Green

</td><td>

Created by ServiceNow and one of the following scenarios is applicable: -   It has never been customized by the customer.
-   It has been customized by the customer and then reverted to the latest ServiceNow upgrade.


</td></tr><tr><td>

Skipped

</td><td>

Red

</td><td>

Created by ServiceNow and then customized by the customer, and hence skipped the latest ServiceNow upgrade. The customer should resolve a skipped update after an upgrade.

</td></tr><tr><td>

Customized

</td><td>

Orange

</td><td>

Created by ServiceNow, and then customized by the customer after the latest ServiceNow upgrade. The customer can revert a customization to implement the latest ServiceNow upgrade.

</td></tr><tr><td>

New

</td><td>

Blue

</td><td>

Created by the customer. The top element of the UI macro should have the following attribute:```
data-sn-macro-sys-id="${jvar_macro_sys_id}"
```

 **Note:** The top element can be a div, span, or table.

</td></tr></tbody>
</table>    **Note:**

    -   When you click the Service Catalog page name or the UI macro name, the corresponding UI page or the macro page is displayed.
    -   When you point to a macro in the UI Page Customization Diagnostics window, the corresponding UI elements are displayed with a pink border.
    -   The state-based color indication is applicable only for UI macros that have a visible UI.
    ![Screenshot for the UI Page Customization Diagnostics window](../image/DebugUICustmWndw.png "UI Page Customization Diagnostics window")

4.  To minimize the UI Page Customization Diagnostics window, click ![Icon to minimize the window](../image/MinimizeDebugUI.png).


**Parent Topic:**[Debugging Service Catalog](../concept/debugging-service-catalog.md)

**Related topics**  


[bundle-crapiref.c_UIMacros]

[bundle-platadm.c_UpgradeHistory]

