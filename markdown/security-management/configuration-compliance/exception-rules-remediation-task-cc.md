---
title: Direct Deferral of Configuration items \(CIs\) by Exception Rules Without Remediation Task Creation
description: Exception rules are applied directly to the Configuration Items \(CIs\) eliminating the process of creating a remediation task. Auto- Exception Rule column is added to the form view, which populates the current exception rule applied on the Configuration Item \(CI\)
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-06-03"
reading_time_minutes: 1
breadcrumb: [Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Direct Deferral of Configuration items \(CIs\) by Exception Rules Without Remediation Task Creation

Exception rules are applied directly to the Configuration Items \(CIs\) eliminating the process of creating a remediation task. Auto- Exception Rule column is added to the form view, which populates the current exception rule applied on the Configuration Item \(CI\)

## Approval of Exception Rule/Reapply:

An exception rule is created for a particular Configuration Item \(CI\), which is in an **open, under investigation, awaiting implementation** state initially. Once the rule is approved, it is processed by a daily, nightly scheduled job that reapplies the exception rule.

When the scheduled job runs, in case the CI gets deferred \(postponed\) due to the incorrect mapping of CI to the exception rule, the scheduled job reopens the CI to reapply a new exception rule.

A new rule with a later execution order can also be activated to replace the previous one.

**Note:** The Deferred until date is set to 12 months by default and you can edit is as necessary from the Exception Management configuration settings page. If you try to select a deferred date beyond the default date, the system throws an error.

## Handling canceled or Deleted Exception Rules:

If the old exception rule is canceled or deleted, it triggers a background job to:

-   Open all associated CIs.
-   Move Exception rule into the draft state when the rule is canceled.
-   Apply a new exception rule to the CIs. \(If there’s an applicable exception rule then the CI will be associated with it and the CI status will be deferred\).

## New CI Creation \(Insertion\):

When a new CI is created \(such as an ingestion\), it is automatically assigned the exception rule. The new CI will also get deferred with the same reasoning and until date, following the same process as when an exception rule is canceled.

A click-able link is available in the CC Manager Workspace to access the exception rule directly, allowing the user to see which exception rule is affecting a given CI.

