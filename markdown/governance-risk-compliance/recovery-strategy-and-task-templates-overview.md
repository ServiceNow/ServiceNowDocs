---
title: Recovery strategy and task templates
description: Business continuity planners often rebuild the same recovery structures each time they author a plan. Reusable templates remove that repetition by capturing standard strategies, tasks, and task groupings once and applying them wherever they are needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/recovery-strategy-and-task-templates-overview.html
release: australia
topic_type: concept
last_updated: "2026-06-03"
reading_time_minutes: 2
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Recovery strategy and task templates

Business continuity planners often rebuild the same recovery structures each time they author a plan. Reusable templates remove that repetition by capturing standard strategies, tasks, and task groupings once and applying them wherever they are needed.

Recovery strategy templates capture the implementation profile of a strategy \(estimated time to implement, maximum duration of use, estimated % of operations achieved, and comments\) so the same strategy can be applied to loss scenarios across plans.

-   Task templates are standalone, reusable tasks that you can add to a recovery task or event task on an adhoc basis. Individual task templates do not carry dependencies.

-   Task template groups bundle multiple task templates and define dependencies between them. A group can apply to all element definitions or to specific ones \(for example, Business service or Linux server\), which scopes the groups offered when you add them from a loss scenario or recovery strategy.


Templates can be associated with plan templates at the plan, loss scenario, and recovery strategy levels, so a plan created from the template generates the full hierarchy in a single operation.

If you are upgrading from a version without templates, you do not have to start from scratch: select existing recovery tasks or event tasks and save them as a new group \(dependencies preserved\), add them to an existing group, or save them as individual task templates."

**Parent Topic:**[Structured workflows for BCPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-tasks-performed-by-bcp-owner.md)

**Related topics**  


[Configure a recovery strategy template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-recovery-strategy-template-uib-ws.md)

[Apply Task templates and Task template groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-reco-task-tem-groups.md)

[Create a business continuity plan from a plan template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-bcp-plan-from-template-in-uib-ws.md)

[Event task creation progress in exercise and crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcm-event-task-template-progress.md)

