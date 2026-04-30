---
title: Configuration Compliance discovery
description: Configuration Compliance data is imported from third-party SCA scanner applications. They structure groups of software and hardware tests into data records to expedite conducting assessments.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Import, Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance discovery

Configuration Compliance data is imported from third-party SCA scanner applications. They structure groups of software and hardware tests into data records to expedite conducting assessments.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

When an import is complete, an event is sent to indicate end-of-import actions. For every active remediation task, the following actions are taken:

-   Resolved remediation tasks with failed results return to the **Awaiting Implementation** state.
-   Remediation tasks where all results have passed, are **Closed**.
-   The state of test results that are in active remediation tasks are updated.
-   The flag indicating whether a result is part of an active remediation task is updated.

**Parent Topic:**[Configuration Compliance imported data](vuln-config-compl-policies.md)

