---
title: Software Asset Management Foundation plugin properties
description: You can set default reconciliation properties such as reconciliation run with custom license metrics, and reconciliation debugging settings.
locale: en-US
release: zurich
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Software Asset Management Foundation plugin Administration, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Software Asset Management Foundation plugin properties

You can set default reconciliation properties such as reconciliation run with custom license metrics, and reconciliation debugging settings.

These properties are available for Software Asset Management Foundation plugin.

To access these properties, navigate to **Software Asset** &gt; **Administration** &gt; **Properties**.

<table id="table_ygc_2lb_dbb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run reconciliation with all available custom license metricscom.snc.samp.recon.enablecustommetrics

</td><td>

Enable custom license metrics when running reconciliation.

 If you have a custom license metric configured, it is not applied when this property is set to **No**.

 -   **Type**: Reconciliation
-   **Default value**: Yes

</td></tr><tr><td>

Enable debugging of reconciliation resultscom.snc.samp.debug

</td><td>

Enable debugging of reconciliation results to troubleshoot a result.

 **Note:** Enabling debugging may have an impact on performance.

 -   **Type**: Reconciliation
-   **Default value**: No

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management Foundation plugin Administration](../concept/c_SAMAdministrationSAMF.md)

