---
title: Deactivate DEX alert grouping
description: Deactivate DEX alert grouping to enable individual alert visibility, aiding in detailed analysis and targeted response.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [DEX Alerts, Configure, Digital End-User Experience, IT Service Management]
---

# Deactivate DEX alert grouping

Deactivate DEX alert grouping to enable individual alert visibility, aiding in detailed analysis and targeted response.

## Before you begin

Role required: sn\_dex.admin

## Procedure

1.  Perform one of the following options.

<table id="choicetable_hm4_cgv_1bc"><thead><tr><th align="left" id="d121205e44">

Options

</th><th align="left" id="d121205e47">

Actions

</th></tr></thead><tbody><tr><td id="d121205e53">

**System Properties table \[sys\_properties\]**

</td><td>

Open the property **sn\_dex.alert.correlation\_rule.device.period** and in the **Value** field, enter 0.

</td></tr><tr><td id="d121205e68">

**Alert Correlation Rules**

</td><td>

Under **All** &gt; **Event Management** &gt; **Rules** &gt; **Alert Correlation Rules**, in DEX Metric Correlation Rule, clear the **Active** check box.

</td></tr></tbody>
</table>
