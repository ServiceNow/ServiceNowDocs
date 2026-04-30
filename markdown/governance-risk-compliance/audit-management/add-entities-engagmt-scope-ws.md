---
title: Add entities to an engagement scope and validate the engagement
description: Add entities related to the selected auditable units to the engagement. In addition, you can also add entities other than the ones created for auditable units to the engagement.
locale: en-US
release: zurich
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Audit Supervisor Workspace, Audit Workspace, Audit Management, Governance, Risk, and Compliance]
---

# Add entities to an engagement scope and validate the engagement

Add entities related to the selected auditable units to the engagement. In addition, you can also add entities other than the ones created for auditable units to the engagement.

## Before you begin

Role required: sn\_audit.manager, sn\_audit\_ws.supervisor

## About this task

During the **Scope** state, as an audit supervisor you can define which entities are involved in the audit engagement. For example, for a financial audit, you can include all business services that the finance department relies on and the finance department itself.

When you add an entity to an engagement, the corresponding risks, controls, test plans, and indicator results of the entity are also added to the engagement.

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Workspace**.

2.  Click the lists icon \(![List icon.](../image/ListsIcon.jpg)\).

3.  Click **All engagements** or **My engagements** in the Execution list.

    You can scope entities to an engagement that is in **Scope** state.

4.  Click the link to the engagement record in the **Name** column.

    The engagement record details open in the **Overview** tab.

5.  Click the Entities related list.

6.  Click the **Add auditable units** button.

7.  In the Auditable units pop-up, select the desired entities that are included in the audit engagement.

    These auditable units are those that have entities already created.

8.  Click **Add**.

    If there are risks and controls, test plans, and indicator results associated with an entity then they appear in their respective sections.

    Risks, controls, and test plans are automatically added if the engagement is already in the **Validate** state. Other related items are added only when you click **Validate** or **Validate and plan** button.

    **Note:** If you do not have GRC: Advanced Audit application installed, only then the **Validate** button appears, otherwise the **Validate and plan** button appears.

    After adding the auditable units as entities to the audit engagement, you can validate and plan the engagement.

9.  To add entities other than the ones created for auditable units, click the **Add other entities** button.

    **Note:** If you have GRC: Advanced Audit application installed, only then the **Add auditable units** and **Add other entities** fields appear. Otherwise, an **Add** button appears in the page.

10. Click the **Validate and plan** button.

    After an engagement has moved to the **Validate** state, all the risks, controls, and test plans associated with the entities in the engagement's scope are associated with the audit. Only direct controls and risk for the entities will get scoped in the audit when the engagement moves to Validate state. Indicator results that were collected during the audit period of the engagement are also associated with the audit.

    As an audit supervisor, you can review the risks, controls, test plans, and indicator results, and update the scope of the engagement, if necessary. You can also begin creating and planning audit tasks for the engagement.


