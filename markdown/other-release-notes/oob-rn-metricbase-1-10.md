---
title: MetricBase v1.10 release notes
description: MetricBase v1.10 includes minor bug fixes and improvements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-metricbase-1-10.html
release: other
topic_type: reference
last_updated: "2021-01-27"
reading_time_minutes: 1
breadcrumb: [MetricBase available versions, OOB Other release notes]
---

# MetricBase v1.10 release notes

MetricBase v1.10 includes minor bug fixes and improvements.

## Version history

This release version also includes minor bug fixes and improvements.

<table id="table_gxv_hvs_l4b"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

PRB1360522

</td><td>

Transform may expand the time range unexpectedly

</td><td>

1.  Create a report with several series selected, with at least one series missing a few days of the most recent data time range.
2.  Select "Resample" with 10 minute period.
3.  Select "Relative Time Range".
4.  Select "Last 7 Days".
5.  Run the report.

 Expected behavior: Show the last 7 days of data.

 Actual behavior: Result starts at the date required to give the series missing data a complete 7 days of data.

</td></tr></tbody>
</table>**Parent Topic:**[MetricBase available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-metricbase.md)

