---
title: Activating an exception rule
description: A rule is activated on its "Valid from" date. After activation, it automates the exception process for findings.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring an exception rule, Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Activating an exception rule

A rule is activated on its "Valid from" date. After activation, it automates the exception process for findings.

The exception rule follows this life cycle:

1.  The new findings that you create or reopen, and that meet the specified condition, are deferred. If you enable the Execute on existing data option when you run the exception rule for the first time, all the active and non-deferred findings that match the exception rule condition are moved to the newly created remediation task \(RT\) and its state is changed to Deferred.
2.  If a newly created finding matches the exception rule condition, it is moved to the deferred RT that is associated with the rule and the group rule is not run on it.
3.  On the "Valid from" date, existing findings are added if you enable the Execute on existing data option.
4.  The RT stops accepting new findings when the rule expires on the "Valid to" date. The RT remains in existence until the "Deferred until" date.
5.  The exception rule expires on the "Valid to" date.

