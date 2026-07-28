---
title: Create an audit plan and generate cases and tasks
description: Use the Store audit playbook in CSM/FSM Workspace to author and publish an audit plan, then click Generate Cases/Tasks to create Store Audit Cases and Audit Tasks for all selected store locations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-store-audit-t-create-and-generate.html
release: australia
topic_type: task
last_updated: "2026-06-30"
reading_time_minutes: 3
keywords: [create audit plan, generate cases, generate tasks, store audit playbook, plan author]
breadcrumb: [Manage Store Audit, Retail]
---

# Create an audit plan and generate cases and tasks

Use the **Store audit** playbook in CSM/FSM Workspace to author and publish an audit plan, then click **Generate Cases/Tasks** to create Store Audit Cases and Audit Tasks for all selected store locations.

## Before you begin

-   Retail Organization records for all stores you want to audit exist on the instance.
-   The default Store Audit Plan Configuration and Template Item Configurations are present \(installed as out-of-the-box seed data\).
-   Role required: `sn_rtl_store_audit.plan_author` alongside `sn_rtl_store_audit.audit_manager` or `sn_rtl_store_audit.location_audit_manager`.

## About this task

Creating an audit plan and generating its cases and tasks is a two-phase process. In the first phase, the **Store audit** playbook guides you through configuring the full plan structure in a single session. In the second phase, you publish the plan and explicitly trigger record creation. This separation lets you review the plan before committing to case generation.

## Procedure

1.  Phase 1: Author the audit plan
2.  Log in to CSM/FSM Workspace with your Plan Author credentials.

3.  In the Workspace, locate the Record Generator for Store Audit Plans and click **Create Audit Plan**.

    The system creates a new `sn_task_plan_template` record and launches the **Store audit** playbook automatically.

4.  In Activity 1 \(**Store case**\), configure the Store Audit Case template items, then click **Next**.

    Each template item defines the structure for one store-level case.

5.  In Activity 2 \(**Audit task**\), configure the Audit Task template items for each Store Case using the Create Template Items subflow, then click **Next**.

    Each task template item represents one Audit Task generated per Store Audit Case.

6.  In Activity 3 \(**Affected stores**\), select the Retail Organization locations to include in this audit plan, then click **Next**.

    You can select multiple Retail Organizations. Selections are saved to `sn_case_creation_service_org` and used during generation. This is the only place to associate stores with a plan—the Template Item form has no standalone store selector.

    The selected Retail Organizations are persisted and available for case generation.

7.  In Activity 4 \(**Schedule options**\), set the audit start date, due date, and any other scheduling parameters, then click **Next**.

8.  In Activity 5 \(**Review**\), confirm the plan summary—template items, affected stores, and schedule—then click **Publish**.

    The plan state changes to Published. The **Generate Cases/Tasks** button becomes visible on the plan record.

9.  Phase 2: Generate Store Audit Cases and Audit Tasks
10. On the published plan record, verify the **Track plan** tab is empty, then click **Generate Cases/Tasks** in the action bar.

    The button is visible only on Published plans and only to users with the `sn_rtl_store_audit.plan_author` role.

    The system synchronously creates:

    -   One Store Audit Case per selected Retail Organization, in state New.
    -   One or more Audit Tasks per Store Audit Case, based on the Template Item Configurations.
    -   One Work Order per Audit Task \(created by a before-insert Business Rule\).
    Platform assignment rules route all generated cases and tasks to Auditors automatically.

11. Click the **Track plan** tab to verify the generated Store Audit Cases.

    The tab lists all generated Store Audit Cases with case number, created date, due date, and state.


## Result

A published audit plan exists with Store Audit Cases and Audit Tasks created for all selected store locations. Cases are in state New and automatically routed to Auditors via assignment rules.

**Parent Topic:**[Manage Store Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-manage.md)

**Related topics**  


[rahi-store-audit-plan-playbook]

[Override audit assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-t-override-assignment.md)

