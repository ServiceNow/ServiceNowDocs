---
title: Configure a recovery strategy template
description: Configure a reusable recovery strategy template so business continuity planners can apply a pre-defined strategy to loss scenarios without re-entering the implementation details each time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/configure-recovery-strategy-template-uib-ws.html
release: australia
topic_type: task
last_updated: "2026-05-16"
reading_time_minutes: 1
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure a recovery strategy template

Configure a reusable recovery strategy template so business continuity planners can apply a pre-defined strategy to loss scenarios without re-entering the implementation details each time.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## About this task

Recovery strategy templates capture the implementation profile of a strategy \(estimated time to implement, maximum duration of use, estimated % of operations achieved, and supporting comments\) so that the same strategy can be applied to multiple loss scenarios across plans. When a plan is created from a plan template that references a recovery strategy template, the strategy and its associated task template groups are pre-populated on the loss scenario without manual re-entry.

\[Omitted image "recovery-strategy-template-form.png"\] Alt text: Recovery strategy template form showing Name, Description, and Implementation Details section.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Plan configuration** &gt; **Recovery strategy templates**.

2.  Select **New**.

3.  Enter a **Name** and **Description** for the template.

4.  In the **Implementation Details** section, enter **Estimated time to implement**, **Maximum duration of use**, and **Estimated % of operations achieved**.

5.  Add **Comments** that planners should see when they apply this strategy.

6.  On the **Task template groups** and **Task templates** related lists, add the groups and templates that should be applied with this recovery strategy.

    The tasks from these groups and templates are created when the recovery strategy template is applied to a loss scenario. For field-level details, see [Recovery strategy template form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/recovery-strategy-template-form.md).

7.  Select **Save**.

    For more information on the fields, see [Recovery strategy template form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/recovery-strategy-template-form.md).


## Result

The recovery strategy template is now available to plan templates and to ad-hoc selection on a loss scenario through the **Add recovery strategy template** control on the **Recovery strategies** tab.

-   **[Recovery strategy template form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/recovery-strategy-template-form.md)**  
Use the Recovery strategy template form to define a reusable implementation profile that planners can apply to loss scenarios in business continuity plans.

**Parent Topic:**[Structured workflows for BCPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-tasks-performed-by-bcp-owner.md)

