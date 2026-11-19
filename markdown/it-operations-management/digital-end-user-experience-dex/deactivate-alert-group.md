---
title: Deactivate DEX alert grouping
description: Deactivate DEX alert grouping to enable individual alert visibility, aiding in detailed analysis and targeted response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/digital-end-user-experience-dex/deactivate-alert-group.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-11-19"
reading_time_minutes: 1
keywords: [deactivate alert grouping, alert correlation rule, individual alert visibility, alert grouping]
breadcrumb: [DEX alerts, Monitor application performance, Manage employee experience, Digital End-User Experience, IT Operations Management]
---

# Deactivate DEX alert grouping

Deactivate DEX alert grouping to enable individual alert visibility, aiding in detailed analysis and targeted response.

## Before you begin

Role required: sn\_dex.admin

## Procedure

1.  Perform one of the following options.

<table id="choicetable_hm4_cgv_1bc"><thead><tr><th align="left" id="d244913e64">

Options

</th><th align="left" id="d244913e67">

Actions

</th></tr></thead><tbody><tr><td id="d244913e73">

**System Properties \[sys\_properties\] table**

</td><td>

Open the property **sn\_dex.alert.correlation\_rule.device.period** and in the **Value** field, enter `0`.

</td></tr><tr><td id="d244913e91">

**Alert Correlation Rules**

</td><td>

Under **All** &gt; **Event Management** &gt; **Rules** &gt; **Alert Correlation Rules**, in DEX Metric Correlation Rule, clear the **Active** check box.

</td></tr></tbody>
</table>
