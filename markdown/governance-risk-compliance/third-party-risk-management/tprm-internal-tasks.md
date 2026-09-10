---
title: Create a task for an internal user
description: Create an internal task to assign follow-up work to an internal user, rather than to a third-party contact, as part of your organization's third-party risk processes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-internal-tasks.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-07-16"
reading_time_minutes: 2
breadcrumb: [Assess third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create a task for an internal user

Create an internal task to assign follow-up work to an internal user, rather than to a third-party contact, as part of your organization's third-party risk processes.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor

## About this task

Tasks typically track follow-up work with a third-party contact. For information about creating and managing tasks for third-party contacts, see [Create a task for a third party or engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-task-create.md) and [Manage a task for a third party or engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-task-manage.md). An internal task is a related but separate record type that assigns follow-up work to an internal user instead of a third-party contact. Internal tasks aren't visible to third-party contacts and don't appear in the third-party portal.

Depending on how your organization configures its due diligence and risk processes, the system can automatically generate an internal task and assign it to a specified respondent. For example, the system can assign the task to the person who submitted a request, so the respondent can provide additional information before the process continues.

When an internal task is submitted to a respondent, the system automatically grants the respondent the internal task responder role to manage the elements linked to the task. For more information about this role, see [Roles in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-roles.md).

You can assign an internal task to any internal user in your organization. The respondent completes the task from the **Employee Center**, under **GRC tasks**.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, select the list icon \[Omitted image "ws-list-icon.png"\] Alt text: and then navigate to **Internal tasks** &gt; **All tasks**.

2.  Select **New** and fill in the form.

    For descriptions of all these fields, see [Create new third-party risk task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-create-task-form.md).

3.  Select **Save**.


## What to do next

The assigned respondent completes the follow-up work from the **Employee Center**, under **GRC tasks**, and updates the task state as they progress. To monitor or update the task, see [Manage a task for a third party or engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-task-manage.md).

**Related topics**  


[Create new third-party risk task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-create-task-form.md)

[Roles in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-roles.md)

[Create a task for a third party or engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-task-create.md)

[Manage a task for a third party or engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-task-manage.md)

