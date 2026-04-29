---
title: Manage a proactive case created from an alert
description: Work on a proactive case and resolve the proactive case as you would other customer service cases.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Proactive Customer Service Operations, Automate and optimize, Use, Customer Service Management]
---

# Manage a proactive case created from an alert

Work on a proactive case and resolve the proactive case as you would other customer service cases.

## Before you begin

Role required:

-   sn\_customerservice\_agent
-   evt\_mgmt\_admin and evt\_mgmt\_operator have read-only access to a case created from an alert and can add work notes, as required.

## About this task

**Note:** This task only applies if you are using Event Management integration on CSM Agent Workspace or the ServiceNow AI Platform interface.

Review proactive cases created from alerts using Agent Workspace. Identify customers, their corresponding install base items affected by the issue causing the alert as well as the service health for each affected install base item. Depending on the number of customers affected, you can propose a proactive case as a major case.

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home** &gt; **Lists** &gt; **Cases**.

    Alternatively, accept a proactive case from your Agent Workspace inbox.

2.  Click the case you want to work on.

3.  You can perform the following actions from the Case form.

<table id="table_izm_tqr_whb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Click **Refresh Install Base Health**.

</td><td>

Update the health status of the affected install base items to see the real-time service status of the account’s install base items.​**Note:** To see this UI action, there must be an account assigned to the case and at least one install base item attached to the case or account.

</td></tr><tr><td>

Click **Affected Install Base Items**.

</td><td>

View accounts and their corresponding install base items affected by the alert. If you don't see this option, click **more**.

</td></tr><tr><td>

Click **Add** or **Remove**.

</td><td>

Add or remove an affected install base item.

</td></tr><tr><td>

Click **Details**.

</td><td>

View the sold product associated to the case as well as the alert that the case was created from.

</td></tr><tr><td>

Click **Propose Major Case**.

</td><td>

Propose a major case when multiple customers are affected. **Note:** If you don't see this option, click the More UI Actions icon \(![More UI Actions icon.](../image/agent-workspace-more-ui-actions-icon.jpg)\).

</td></tr></tbody>
</table>4.  Resolve and close proactive cases in the same way as other customer service management cases.

    **Note:** If an alert is closed, a case is not automatically closed.


**Related topics**  


[Propose a case as a major case candidate](propose-major-case-candidate.md)

[Close a customer service case](t_CloseACase.md)

[AWA for CSM](../concept/awa-csm-overview.md)

