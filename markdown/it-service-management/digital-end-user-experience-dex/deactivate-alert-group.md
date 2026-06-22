---
title: Deactivate DEX alert grouping
description: Deactivating DEX alert grouping allows for individual alert visibility, aiding in detailed analysis and targeted response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-service-management/digital-end-user-experience-dex/deactivate-alert-group.html
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 1
breadcrumb: [Metric rules for Digital End-User Experience, Configuring Digital End-User Experience, Digital End-User Experience, IT Service Management]
---

# Deactivate DEX alert grouping

Deactivating DEX alert grouping allows for individual alert visibility, aiding in detailed analysis and targeted response.

## Before you begin

Role required: sn\_dex.admin

## Procedure

1.  Perform one of the following options.

<table id="choicetable_hm4_cgv_1bc"><thead><tr><th align="left" id="d198071e44">

Options

</th><th align="left" id="d198071e47">

Actions

</th></tr></thead><tbody><tr><td id="d198071e53">

**System Properties table \[sys\_properties\]**

</td><td>

Open the property **sn\_dex.alert.correlation\_rule.device.period** and in the **Value** field, enter 0.

</td></tr><tr><td id="d198071e68">

**Alert Correlation Rules**

</td><td>

Under **All** &gt; **Event Management** &gt; **Rules** &gt; **Alert Correlation Rules**, in DEX Metric Correlation Rule, clear the **Active** check box.

</td></tr></tbody>
</table>
