---
title: View and implement proposed fixes for Scan Engine
description: Some definitions include proposed fixes for resolving them, which you can initiate automatically.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-13"
reading_time_minutes: 1
breadcrumb: [Scan Engine, Platform Health, Using Impact, Impact]
---

# View and implement proposed fixes for Scan Engine

Some definitions include proposed fixes for resolving them, which you can initiate automatically.

## Before you begin

Role required: Admin or scan engine user.

**Note:** Proposed fixes are only available for instance scans findings, not for real-time monitoring findings.

A proposed fix is a recommended remediation option provided for certain definition findings. It includes a specific, predefined solution that developers can apply to resolve issues quickly and accurately. While the fix is not automated—manual intervention is still required—having a clear, guided resolution significantly reduces troubleshooting time and ensures consistency in how issues are addressed.

Proposed fixes are defined in the `autofix_script` field of the scan definition. The script executes against the finding's target record when **Apply Proposed Fix** is selected.

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Proposed Fix Findings**.

    All findings with available proposed fixes display.

2.  Open a record to view the definition finding details.

3.  To implement a fix, select **Apply Proposed Fix** and close the definition finding.


## What to do next

After applying the fix, the system executes the autofix script and marks the finding as resolved. Review the finding record and the target record to verify the fix was applied successfully. Some fixes may require additional manual validation.

