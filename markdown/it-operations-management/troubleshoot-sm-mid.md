---
title: Upgrade issues
description: What to do when monitors don't work after upgrading synthetic monitoring.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Troubleshoot synthetic monitors, Synthetic monitoring reference, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Upgrade issues

What to do when monitors don't work after upgrading synthetic monitoring.

## Condition

After upgrading synthetic monitoring, monitors remain in unknown state.

## Cause

After upgrading synthetic monitoring, if the monitor is hosted on a MID Server, the server must be restarted to re-recognize the hosted monitors.

## Remedy

Restart the MID Server. See [Manually start, stop, and restart a MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_InstallMIDServerAsWinService.md).

**Parent Topic:**[Troubleshoot synthetic monitors](troubleshoot-synthetic-monitors.md)

