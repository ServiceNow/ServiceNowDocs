---
title: Update an entity
description: Update the details of an existing entity.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage entities in Operational Sustainability Management \(formerly ESG Management\), Configure, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Update an entity

Update the details of an existing entity.

## Before you begin

Role required: \(per product\)

-   In Operational Sustainability Management: sn\_esg.program\_manager
-   In GRC: Metrics: sn\_grc\_metric.manager
-   In Risk Management: sn\_risk\_workspace.IT\_risk\_manager and sn\_risk\_workspace.operational\_risk\_manager

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Scoping** &gt; **All entities**.

2.  Click an entity from the list.

3.  On the form, update the fields as necessary.

    |Field|Description|
    |-----|-----------|
    |Tabs|
    |Overview tab|Compliance status and risk status of the entities. Tracking details of the issues, controls, and policy exceptions. This field is automatically set to display the overview of the status and the tracking details.|
    |Details tab|Information on the entity. For more information on the **Details** tab, see [Create an entity](create-entity.md) for more information.|
    |Hierarchy tab|Upstream entities and downstream entities for the selected entity. A parent entity that has the child entities is said to have the downstream entities. Any child entity that has the parent entities is said to have the upstream entities. Select an entity and click **Add** to add an upstream or downstream entity to the parent entity.|
    |Related lists|
    |Entity types|Details of the entity type, description, filter condition for the entity type, and the compliance score in percentage.|
    |Downstream risks|Details of the downstream risk for the selected entity such as number, name, entity, class, risk statement, risk assessment methodology, owner group, and owner of the entity. To add new risk statements, click **Add**. To create a new risk statement, click **New**.|
    |Downstream controls|Details of the downstream controls such as name, number, entity, control objective, state, status, exempt, owner, and description. To add the new downstream controls, click **Add**.|
    |Downstream engagements|Details of the downstream engagements such as name, number, type, parent plan, state, engagement lead, remaining expense budget \(%\), remaining resource budget \(%\), and engagement planned start. To create a new downstream engagement, click **New**.|
    |Downstream issues|Details of the downstream issues, such as name, number, issue source, issue type, state, issue manager, assigned to, priority, and due date. To add a new issue, click **New**.|
    |Downstream tasks|Details of the downstream tasks, such as name, number, parent, state, assigned to, and planned end date.|
    |Policy exceptions|Details of the policy exceptions, such as name, number, state, substate, policy, control objective, issue, reason, requester, valid from, valid to, and risk rating.|
    |Content References|Details of the content references for the entity such as content reference, description, and version. To add new content references, click **Add**.|
    |Goals|Details of the goals for the entity such as the goal, owner, state, status, progress, start date, and end date for the goal. To add a new goal, click **Add**.|

    **Note:** Some related lists display in the entity form only when certain applications are installed. For example, the Downstream risks related list displays only when the Risk Management application is installed. The Downstream engagements related list displays only when the Audit Management application is installed. The Downstream controls, Downstream issues, and Policy exceptions related lists display only if you have the IRM license.

4.  To save the updates to an entity, click **Save**.

5.  To retire an entity, click **Retire**.

6.  To delete an entity, click **Delete**.

7.  To visually explore the relationship between the upstream entities, downstream entities, entity class, and entity type associated with the entity, select **360° view**.


**Parent Topic:**[Manage entities in Operational Sustainability Management \(formerly ESG Management\)](../concept/entities-in-esg.md)

