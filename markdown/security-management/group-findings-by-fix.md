---
title: Group findings by fix
description: Use a remediation task rule to group the findings that share a fix, so your team can remediate them together as a single unit of work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/group-findings-by-fix.html
release: zurich
topic_type: task
last_updated: "2026-07-29"
reading_time_minutes: 2
keywords: [group findings by fix, remediation task rule, grouping]
breadcrumb: [Use, Fix Intelligence for Security Exposure Management, Integrations, Unified Security Exposure Management, Security Operations]
---

# Group findings by fix

Use a remediation task rule to group the findings that share a fix, so your team can remediate them together as a single unit of work.

## Before you begin

Prerequisites:

-   Fix Intelligence for SEM has linked findings to fixes.
-   You have the roles required to configure remediation task rules in USEM.

## About this task

USEM remediation task rules automatically group findings into remediation tasks based on conditions you define. When Fix Intelligence for SEM links findings to fixes, you can group findings by their fix so that a single remediation task covers the findings that fix resolves.

Fix Intelligence for SEM ships one remediation task rule out of the box, in an inactive state, that groups findings by assignment group and fix. Ensure that the rule is active. For how remediation task rules work and how to create them, see [Configuring remediation task rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-configure-remediation-task-rules.md) and [Create remediation task rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-configure-remediation-task-rules.md).

## Procedure

1.  Open the remediation task rule configuration in USEM.

2.  Create or edit a remediation task rule for the findings you want to group.

3.  Set the rule to group findings by fix.

    Findings that share a fix and the same assignment group are grouped into one remediation task. The remediation task rule also has assignment group as a default grouping criterion. When a finding's fix link is cleared, it is removed from the fix-based group.

    For example, for host vulnerable items where **Active** is **true**, group by assignment group and fix so that each remediation task covers one fix for one assignment group.

4.  Save and activate the rule.


## Result

Findings that share a fix and the same assignment group are grouped into a single remediation task, so your team can plan and track the fix as one unit of work. The remediation task appears on the fix, and your team can run the full remediation workflow from the Remediation Task record, including creating a change request, requesting an exception, and starting the investigation. Grouping by fix effectively de-duplicates many findings into one actionable remediation task.

**Parent Topic:**[Using Fix Intelligence for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/using-fix-intel-security-exposure-management.md)

**Related topics**  


[Configuring remediation task rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-configure-remediation-task-rules.md)

[Create remediation task rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-configure-remediation-task-rules.md)

