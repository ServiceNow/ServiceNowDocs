---
title: Initiate instance scans
description: You can scan your ServiceNow instance for findings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/impact/initiate-instance-scans.html
release: zurich
topic_type: task
last_updated: "2025-11-13"
reading_time_minutes: 1
breadcrumb: [Running on-demand scans, Scan Engine, Platform Health, Using Impact, Impact]
---

# Initiate instance scans

You can scan your ServiceNow instance for findings.

## Before you begin

Role required: Scan Engine Admin

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Scheduled Scan**.

2.  To run a full scan, set `force_full_scan` to **True**.

    By default, `force_full_scan` is set to **False**, meaning it will only run delta scans.

3.  Select **Execute Now**.

4.  To review the scan as it runs or after it is completed, open the **Scan Status** module.

    See [View scan results for Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/viewing-scan-results-scan-engine.md) .


