---
title: View deprecated audit records
description: View the deprecated asset audit records that are created before switching to the common Asset Audits \[sn\_itam\_common\_asset\_audit\] table and stored in the Asset Audits \[sn\_hamp\_asset\_audit\] table.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-12-30"
reading_time_minutes: 1
keywords: [deprecated audits]
breadcrumb: [Audit hardware asset inventory, Use, Hardware Asset Management, IT Asset Management]
---

# View deprecated audit records

View the deprecated asset audit records that are created before switching to the common Asset Audits \[sn\_itam\_common\_asset\_audit\] table and stored in the Asset Audits \[sn\_hamp\_asset\_audit\] table.

## Before you begin

Role required: asset

Set the **migrate\_hamaudit** system property to **true**.

## About this task

**Important:** This feature is available with Hardware Asset Management version 15.0.0 onwards.

You can view deprecated asset audit records in the Audits \[Deprecated\] list. These records are read only and you can’t perform any actions on them or create audit records from this view. Before enabling audit enhancements and migrating to the common audit table, you must complete and close all in-progress and new audit records. Once the **migrate\_hamaudit** system property is set to **true**, you can't act on in-progress and new audit records, because they’re considered deprecated audits.

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Asset operations**.

2.  Select **Audits \[Deprecated\]**.

3.  Select an audit number link.


## What to do next

View the details of scanned assets within the asset audit form by selecting the relevant tabs.

**Parent Topic:**[Audit hardware asset inventory](../concept/ham-inventory-audit.md)

