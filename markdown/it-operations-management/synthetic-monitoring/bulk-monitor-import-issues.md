---
title: Bulk monitor import issues
description: Learn to fix issues that might occur when you create monitors in bulk.
locale: en-US
release: australia
product: Synthetic Monitoring
classification: synthetic-monitoring
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Troubleshoot synthetic monitors, Synthetic monitoring reference, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Bulk monitor import issues

Learn to fix issues that might occur when you create monitors in bulk.

## Common bulk monitor import issues

|Issue|Cause|Solution|
|-----|-----|--------|
|cmdb\_ci is required|Missing HTTP endpoint|Create endpoint in CMDB first|
|Location not found|Invalid location sys\_id|Verify location exists|
|Authentication failed|Invalid credentials|Check username/password|
|Job stuck in "pending"|Event queue backed up|Wait or contact admin|
|Timeout errors|Large payload, slow processing|Increase timeout, reduce batch size|

**Parent Topic:**[Troubleshoot synthetic monitors](troubleshoot-synthetic-monitors.md)

