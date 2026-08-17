---
title: Create and publish an audit plan
description: Use the Store audit playbook in CSM/FSM Workspace to author and publish an audit plan. Publishing automatically creates the Store Audit Cases and Audit Tasks for all selected store locations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-store-audit-t-create-and-generate.html
release: australia
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 2
keywords: [create audit plan, publish audit plan, store audit playbook, plan author]
breadcrumb: [Manage Store Audit, Retail]
---

# Create and publish an audit plan

Use the **Store audit** playbook in CSM/FSM Workspace to author and publish an audit plan. Publishing automatically creates the Store Audit Cases and Audit Tasks for all selected store locations.

## Before you begin

-   Retail Organization records for all stores you want to audit exist on the instance.
-   Role required: `sn_rtl_store_audit.plan_author` assigned alongside `sn_rtl_store_audit.audit_manager` or `sn_rtl_store_audit.location_audit_manager`, and `sn_fsm_planned_wm.planned_work_admin`.

**Note:** Use the `sn_fsm_planned_wm.planned_work_admin` role to avail the one-time and recurring schedule options.

## About this task

The **Store audit** playbook guides you through configuring the full plan in a single session, ending with a Review activity where you publish.

## Procedure

1.  Log in to CSM/FSM Workspace with your Plan Author credentials.

2.  In the application navigator, navigate to the **Store audit** menu and click **New**.

3.  In the plan type picker that opens, select **Store audit** as the plan type.

    The system creates a new `sn_task_plan_template` record and the **Store audit** playbook launches automatically.

4.  In the **Store case** activity, configure the Store Audit Case template item, then click **Next**.

5.  In the **Audit task** activity, configure the Audit Task template item, then click **Next**.

6.  In the **Affected stores** activity, select the Retail Organizations where audit has to be done, then click **Next**.

7.  In the **Schedule options** activity, fill in the mandatory fields and set the generation as immediate, one-time, or recurring, then click **Next**.

8.  In the **Review** activity, confirm the plan summary, edit the details, if required and then click **Publish**.

    For an immediate schedule, the Store Audit Cases and Audit Tasks are created automatically as part of publishing. For a one-time or recurring schedule, they are created later at the scheduled time.


## Result

A published audit plan exists. Click the **Track plan** tab on the plan record to see the generated Store Audit Cases once they exist.

**Parent Topic:**[Manage Store Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-manage.md)

**Related topics**  


[Retail Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-overview.md)

[Audit assignment from workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-t-override-assignment.md)

