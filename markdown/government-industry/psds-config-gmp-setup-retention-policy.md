---
title: Configure a retention policy for grant cases in Grants Management
description: Set up an Archive Rule to automatically purge active grant cases and their associated data after a set period of time.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Grants Management, Playbooks, Configure Agent Workspaces, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure a retention policy for grant cases in Grants Management

Set up an Archive Rule to automatically purge active grant cases and their associated data after a set period of time.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Rules**.

2.  Select the **Archive Grant Cases after 3 years** record.

    A retention rule that checks for cases created 3 years ago AND are Closed is enabled by default.

3.  Modify the conditions you wish to change based on your agency's retention rule requirements.

    You can add an additional condition, such as adding a condition to ignore Records being Audited, to the retention rule using any of the fields from the Grant Case table.

4.  Under Related links, select **Recalculate Archive Estimate** to calculate archive estimate of the records before running the rule.

    The estimate will populate in the Record Estimate field.

5.  Run the Archive Rule by selecting **Run Archive Now**.


## Result

All cases that match your retention criteria are now purged.

