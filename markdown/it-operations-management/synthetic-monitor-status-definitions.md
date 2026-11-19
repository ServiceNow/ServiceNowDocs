---
title: Synthetic monitor status definitions
description: Learn what each synthetic monitor test status means, so you can distinguish a genuine endpoint failure from a test that never ran.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/synthetic-monitor-status-definitions.html
release: zurich
topic_type: reference
last_updated: "2026-07-24"
reading_time_minutes: 1
keywords: [status, monitor status, Unknown, Failed, Passed]
breadcrumb: [Reference, Landing page, ITOM AIOps, IT Operations Management]
---

# Synthetic monitor status definitions

Learn what each synthetic monitor test status means, so you can distinguish a genuine endpoint failure from a test that never ran.

## Status definitions

Each synthetic monitor displays one of the following statuses based on its most recent test run and configuration state.

|Status|Definition|
|------|----------|
|Passed|The HTTP response met all configured conditions; status code, response time, and body content on its most recent run.|
|Failed|The monitor's most recent run failed as either a configured condition wasn't met, the target was unreachable, or the assigned location was unavailable \(MID Server or ACC agent\).|
|Unknown|The monitor has no execution locations assigned, or its assigned location was recently removed. No result is currently available.|
|Pending|The monitor has never completed a run yet. This is a UI-computed state, not stored in the database.|
|Paused|The monitor is turned off and will not run until it is active. This is a UI-computed state, not stored in the database.|

## Related topics

[Upgrade issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/troubleshoot-sm-mid.md)

[Identifying system issues with synthetic monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/identifying-system-issues.md)

**Parent Topic:**[Synthetic monitoring reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/synthetic-monitoring-reference.md)

