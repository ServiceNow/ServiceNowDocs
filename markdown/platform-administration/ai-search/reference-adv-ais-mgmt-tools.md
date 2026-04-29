---
title: Advanced AI Search Management Tools reference
description: This reference topic describes system components installed with the Advanced AI Search Management Tools application.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Advanced AI Search Management Tools, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Advanced AI Search Management Tools reference

This reference topic describes system components installed with the Advanced AI Search Management Tools application.

## Plugins installed with Advanced AI Search Management Tools

|Plugin|Description|
|------|-----------|
|Advanced AI Search Management Tools \(sn\_ais\_admin\_tools\)|Includes AI Search dashboards and Search Preview tool.|

## Scheduled jobs installed with Advanced AI Search Management Tools

<table id="table_ugk_xkm_gbc"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Load AI Search Dashboard Documents by Month

</td><td>

Populates the Indexed Documents by Month data visualization on the AI Search dashboard. Runs every minute.

</td></tr><tr><td>

Load AI Search Dashboard Documents by Profile

</td><td>

Populates the Documents by Search Profile data visualization on the AI Search dashboard. Runs every hour.

</td></tr><tr><td>

Load AI Search Dashboard Documents by Search Source

</td><td>

Populates the Documents by Search Source data visualization on the AI Search Profile dashboard. Runs every hour.

</td></tr><tr><td>

Load AI Search Dashboard Total Indexed Documents

</td><td>

Populates the Total Indexed Documents data visualization on the AI Search dashboard. Runs every hour.

</td></tr><tr><td>

Update Search Analytics Data

</td><td>

Pre-calculates metrics to improve load time for the AI Search Analytics dashboard. Runs every hour.**Note:** If you pause or disable this scheduled job, the AI Search Analytics dashboard takes longer to load and displays the metrics calculated by the last scheduled job run. You can specify a new date range for the dashboard to force recalculation of metrics.

</td></tr></tbody>
</table>## List of all components installed with Advanced AI Search Management Tools

To view the complete list of components installed with Advanced AI Search Management Tools, follow the steps described in [Find components installed with an application](../../../administer/plugins/task/find-components.md). The application's package name is **Advanced AI Search Management Tools**.

