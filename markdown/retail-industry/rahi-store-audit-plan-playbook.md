---
title: Audit plan and playbook
description: An audit plan defines what is audited, at which store locations, and when. Plan Authors create and configure audit plans through the Store audit playbook, which launches automatically from the CSM/FSM Workspace Record Generator.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-store-audit-plan-playbook.html
release: australia
topic_type: concept
last_updated: "2026-06-30"
reading_time_minutes: 2
keywords: [audit plan, store audit playbook, task plan template, record generator, affected stores]
breadcrumb: [Retail Store Audit Operations, Explore, Retail]
---

# Audit plan and playbook

An audit plan defines what is audited, at which store locations, and when. Plan Authors create and configure audit plans through the **Store audit** playbook, which launches automatically from the CSM/FSM Workspace Record Generator.

Audit plans are authored using the ServiceNow Task Plan Templates platform feature \(`sn_task_plan_template`\). The application ships a default Store Audit Plan Configuration and associated Template Item Configurations as out-of-the-box seed data, providing a ready-to-use audit structure immediately after installation.

## Plan authoring entry point

Plan Authors create a new audit plan using the Record Generator in CSM/FSM Workspace. The Record Generator creates a new `sn_task_plan_template` record and fires the **Store audit** playbook automatically on insert. The connection chain is:

1.  The Store Audit Plan Configuration \(`sn_task_plan_config` OOB seed data\) references the Record Generator via the `playbook_record_generator` field.
2.  The Record Generator \(`sys_playbook_experience_record_generator`\) references the **Store audit** playbook via `process_definition` and targets the `sn_task_plan_template` table.
3.  The playbook fires on every new `sn_task_plan_template` insert where `task_plan_config` matches the Store Audit Plan Configuration.

## Playbook structure

The **Store audit** playbook contains a single **Plan** stage with five sequential activities. All activities must be completed in order.

|Order|Activity|Purpose|
|-----|--------|-------|
|1|Store case|Configure Store Audit Case template items—one per Retail Organization scope.|
|2|Audit task|Configure Audit Task template items for each Store Case using the Create Template Items subflow.|
|3|Affected stores|Select the Retail Organization locations in scope. Selections are persisted via `sn_case_creation_service_org` and used during case generation.|
|4|Schedule options|Configure audit timing—start date and due date.|
|5|Review|Review the full plan summary before publication.|

**Warning:** Retail Organization locations are selected exclusively through the **Affected stores** activity \(Activity 3\). The Template Item form presents no standalone Retail Organization related list.

## Plan states

-   **Draft**

    The plan is being configured. The playbook is active.

-   **Published**

    The Plan Author has completed the playbook and clicked **Publish**. The **Generate Cases/Tasks** button becomes visible on the plan record.

-   **Cases generated**

    Store Audit Cases and Audit Tasks have been created. The **Track plan** tab lists all generated cases.


**Parent Topic:**[Retail Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-overview.md)

**Related topics**  


[Data model and case generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-generation-flow.md)

[Create an audit plan and generate cases and tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-t-create-and-generate.md)

