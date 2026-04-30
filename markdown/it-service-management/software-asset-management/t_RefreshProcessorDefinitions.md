---
title: Refresh your legacy Software Asset Management plugin processor definitions
description: After activating the legacy IBM PVU Process Pack, use the Refresh Processor Definitions module in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to create process definitions for existing computers in the Computer \[cmdb\_ci\_computer\] table.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Legacy IBM PVU Process Pack, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Refresh your legacy Software Asset Management plugin processor definitions

After activating the legacy IBM PVU Process Pack, use the Refresh Processor Definitions module in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to create process definitions for existing computers in the Computer \[cmdb\_ci\_computer\] table.

## Before you begin

Role required: sam

## About this task

After this step, business rules in SAM update the Processor Definition \[CMDB\_processor\_definition\] table automatically when changes are made to computers or when new computers are added. You should not need to use the Refresh Processor Definitions module a second time, but it is always available if you make significant changes to the Computer \[cmdb\_ci\_computer\] table.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **System** &gt; **Refresh Processor Definitions**.

2.  Click **Proceed**.


**Parent Topic:**[Legacy IBM PVU Process Pack](../concept/c_IBMPVUProcessPack.md)

