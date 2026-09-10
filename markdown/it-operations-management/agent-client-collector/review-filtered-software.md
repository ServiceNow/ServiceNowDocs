---
title: Review filtered software
description: Review the entries in the Software Install Filter Staging table \(samp\_sw\_install\_filter\_staging\) to confirm your rules are filtering only the software you expect.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/review-filtered-software.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [filter staging, audit log, review, exclusion, SAM]
breadcrumb: [Software filter, ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# Review filtered software

Review the entries in the Software Install Filter Staging table \(samp\_sw\_install\_filter\_staging\) to confirm your rules are filtering only the software you expect.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

The Software Install Filter Staging table automatically records every software item that has been excluded by an active filter rule.

When the same software is reported on a later scan, its staging table entry is automatically refreshed with the new confirmation date. Entries that have not been updated indicate software that has not been reported recently by your devices.

## Procedure

1.  Navigate to the Software Install Filter Staging table \(**All** &gt; **Software Install Filter Staging**\).

2.  Review the records to verify the software that has been excluded and by which rule.

    Each entry contains the following information:

    -   The software's display name, publisher, version, and discovery source.
    -   The custom rule that excluded it \(appears blank if it was excluded by a rule from the base-system\).
    -   The date it was last reconfirmed as excluded.
3.  Confirm that your rules are excluding only the software you intended.

    If you find unexpected exclusions, check your active rules and adjust them as needed.


**Parent Topic:**[Software filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/software-filter.md)

