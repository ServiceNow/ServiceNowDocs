---
title: Synthetic monitoring Landing Page
description: Read the following to understand what is displayed on the Synthetic monitoring landing page where you can view aggregate information about your synthetic monitors.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Synthetic monitoring reference, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Synthetic monitoring Landing Page

Read the following to understand what is displayed on the Synthetic monitoring landing page where you can view aggregate information about your synthetic monitors.

## Aggregate information

The cards show aggregate information for all monitors, whether they're active or not. Select a card to filter the Monitors list.

|Card title|Description|
|----------|-----------|
|Total monitors|Total number of monitors created.|
|Passed|Number of total monitors that have returned the value that was set as the monitor's assertion, for example a status code of `200`.|
|Failed|Number of total monitors that returned a value other than what was configured as the assertion.|
|Pending|Number of total monitors that are in the Pending state. Monitors are set to **Pending** before the first test runs.|
|Paused|Number of total monitors that are in the Paused state. Paused monitors are monitors that have been set to **Monitor disabled** on the Configuration page.|
|Unknown|Number of total monitors that aren't running due to an issue with the related Agent Client Collector \(ACC\) proxy.|

## Monitor list

By default, this list displays all monitors that have been created. You can select a card at the top of the page to filter to a list of monitors with that state. Select a monitor to view its details page.

**Parent Topic:**[Synthetic monitoring reference](synthetic-monitoring-reference.md)

