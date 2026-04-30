---
title: Deferring findings automatically without manual intervention using exception rules
description: Exception rules for Security Exposure Management Workspace enable you to automate the deferral process for findings. Request an exception for the findings that can't be remediated or deferred immediately, by identifying the impacted vulnerabilities, configuration items \(CIs\), or VIs. Defer the matching findings based on the rule when the system identifies them by automating the finding deferral process.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Deferring findings automatically without manual intervention using exception rules

Exception rules for Security Exposure Management Workspace enable you to automate the deferral process for findings. Request an exception for the findings that can't be remediated or deferred immediately, by identifying the impacted vulnerabilities, configuration items \(CIs\), or VIs. Defer the matching findings based on the rule when the system identifies them by automating the finding deferral process.

**Using exception rules in your organization**

Use exception rules to automatically defer new and existing findings for a specific period if they match the approved rule condition. Automation minimizes the risk of missing service level agreements and makes it easier to manage multiple items, because you’re eliminating manual intervention.

Deferral rules support ordering, that is, the rule with the highest priority is run first. When a high-priority rule is applied on a finding, no subsequent rules are applied on it again even if the condition matches the Finding.

The life cycle of an exception rule is as follows:

-   Creating an exception rule
-   Approving an exception rule request
-   Activating an exception rule
-   Deferring an exception rule
-   Expiry of an exception rule

**Creating an exception rule**

You can create an exception rule to automatically defer the findings that match the defined conditions for the specified period. After you create an exception rule, submit it for approval.

**Approving an exception rule request**

Approving an exception rule request is a two-level process. If only the first-level approver is present, the exception rule can be assessed and approved by a single approval. However, if there's no first-level approver, an exception rule approval can't be approved. See [Approve an exception rule request](../task/sem-approve-ex-rule-request.md) for more information.

**Note:** The Change Approval \(CA\) is now also created during exception rule submission. This enhancement ensures consistency across exception workflows and improves traceability.

After an exception rule request is approved, you can perform the following actions:

-   Cancel
-   Delete

**Activating an exception rule**

Starting from the "Valid from" date, the exception rule runs on all the findings that are created and also on the ones that are moved from the Closed to the Open state.

**Note:** If you enable the Execute on existing data option, a scheduled job runs once on the existing data on the "Valid from" date.

**Deferring an exception rule**

You can defer findings that match the conditions defined in this exception rule, up to the "Deferred until" date that is defined for the rule. On this date, the remediation task that you created for the exception rule is closed and all the findings in this group move back to the Open state.

**Expiry of an exception rule**

After the exception rule expires, it no longer runs on new or reopened findings.

**Parent Topic:**[Automating prioritization and triaging](sem-automating-prioritization-triaging.md)

**Related topics**  


[Configuring an exception rule](sem-configure-exception-rule.md)

