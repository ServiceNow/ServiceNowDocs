---
title: Deactivate DEX alert grouping
description: Deactivating DEX alert grouping enables individual alert visibility, aiding in detailed analysis and targeted response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-service-management/digital-end-user-experience-dex/deactivate-alert-group.html
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 1
breadcrumb: [DEX administration, Configure, Digital End-User Experience, IT Service Management]
---

# Deactivate DEX alert grouping

Deactivating DEX alert grouping enables individual alert visibility, aiding in detailed analysis and targeted response.

## Before you begin

Role required: sn\_dex.admin

## Procedure

1.  Perform one of the following options.

<table id="choicetable_hm4_cgv_1bc"><thead><tr><th align="left" id="d121542e44">

Options

</th><th align="left" id="d121542e47">

Actions

</th></tr></thead><tbody><tr><td id="d121542e53">

**System Properties table \[sys\_properties\]**

</td><td>

Open the property **sn\_dex.alert.correlation\_rule.device.period** and in the **Value** field, enter 0.

</td></tr><tr><td id="d121542e68">

**Alert Correlation Rules**

</td><td>

Under **All** &gt; **Event Management** &gt; **Rules** &gt; **Alert Correlation Rules**, in DEX Metric Correlation Rule, clear the **Active** check box.

</td></tr></tbody>
</table>
