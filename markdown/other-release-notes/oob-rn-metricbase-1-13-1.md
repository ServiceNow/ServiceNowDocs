---
title: MetricBase 1.13.0 - Hot Fix 1 release notes
description: MetricBase 1.13.0 - Hot Fix 1 includes minor bug fixes and improvements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-metricbase-1-13-1.html
release: other
topic_type: reference
last_updated: "2021-01-27"
reading_time_minutes: 1
breadcrumb: [MetricBase available versions, OOB Other release notes]
---

# MetricBase 1.13.0 - Hot Fix 1 release notes

MetricBase 1.13.0 - Hot Fix 1 includes minor bug fixes and improvements.

## Compatibility

All MetricBase versions are backwards-compatible and can be used on any ServiceNow family release. This MetricBase release is for on-premise/self-hosted customers only.

## Installation

For instructions on how to install and configure MetricBase on your on-premise environment, contact your Support Account Manager or sales representative.

## Fixed problems

<table id="table_gxv_hvs_l4b"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DevOps-metricbase

 PRB1454566

</td><td>

Transforms sometimes returns the wrong value "randomly"

</td><td>

 

</td></tr><tr><td>

DevOps-metricbase

 PRB1472639

</td><td>

Deadlock on injection of weld property

</td><td>

It appears that injection of new property which disables server-side encryption can cause a deadlock in clotho server.

</td></tr><tr><td>

DevOps-metricbase

 PRB1461051

</td><td>

Dimension names with more than 127 characters cause errors in shard scanning

</td><td>

 

</td></tr><tr><td>

DevOps-metricbase

 PRB1453601

</td><td>

java.lang.ArrayIndexOutOfBoundsException during transform due to race condition

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[MetricBase available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-metricbase.md)

