---
title: Lead-to-Cash Process Management
description: The ServiceNow Lead-to-Cash Process Management application empowers sales teams by providing a consolidated view of all critical sales data and activities.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Order operations, Explore, Sales Customer Relationship Management]
---

# Lead-to-Cash Process Management

The ServiceNow® Lead-to-Cash Process Management application empowers sales teams by providing a consolidated view of all critical sales data and activities.

## Lead-to-Cash Process Management overview

Lead-to-Cash Process Management is a centralized, real-time command center that aggregates information from various sources like Customer Relationship Management \(CRM\) and Enterprise Resource Planning \(ERP\) platforms into a dynamic dashboard.

## Lead-to-Cash Process Management users

<table id="table_p3f_gyt_vfc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sales admin

 Contract admin

</td><td>

Define and create the sales process and relationships between the sales entities to be monitored using Lead-to-Cash Process Management.

</td></tr><tr><td>

Sales process manager

</td><td>

Create sales process records for an account and monitor, manage, and follow-up on tasks.

</td></tr></tbody>
</table>## Lead-to-Cash Process Management workflow

The following illustration describes the tasks involved in configuring and using Lead-to-Cash Process Management to monitor the end-to-end sales process from a single interface.

![Infographic showing how sales admins set up business objects and sales process managers use the app for monitoring sales processes. For details, refer to the following description.](../image/lead-to-cash-process-management-landing.svg "Lead-to-Cash Process Management workflow")

1.  Sales admins create a business object group in the Next Experience UI, is a logical entity that defines your business process and the entities involved. For example, order-to-cash.
2.  Create business entities \(business object type\) you want to monitor in your sales process and define relationships between them.
3.  Add the business entities as members of the business object group.
4.  The sales process manager creates sales process records in the CSM Configurable Workspace.
5.  Sales process managers create sales process records for monitoring a customer account. A dashboard is created that contains the hierarchical node map view of the opportunities, quotes, orders, and other related entities.
6.  Manage tasks, status, documents, and emails related to the business entities, and follow up with respective teams to expedite the process.
7.  Track other tasks at the sales process record level by creating business process records.

## Lead-to-Cash Process Management benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Create a hierarchical relationship between sales entities using built-in or custom business objects that mirror your organization’s structure and strategic goals.|[Create business objects and set up relationships between the entities](../task/create-business-object-group-define-entity-relationship.md)|Sales admin|
|Customize the number of levels and tile content on the node map, enhancing clarity and control so that the sales process managers can focus on relevant data and navigate through complex sales processes effectively.|[Customize the sales process dashboard](customizing-sales-process-dashboard.md)|Sales admin|
|Select parent entities \(such as Opportunity, Quote, or Order\) and child entities \(such as Quote lines or Order lines\) to create a customized view of the sales life cycle that reflects the structure and needs of each account. This capability helps you track only relevant records, reducing noise and improving focus.|[Create account-specific sales process records](../task/create-sales-process-record.md)|Sales process manager|
|Gain end-to-end visibility of the defined sales process through a consolidated view that provides a real-time snapshot of opportunities, quotes, orders, and related entities. The ability to see an entity's details eliminates the need to toggle between systems.|[Consolidated view and nodal hierarchy for monitoring a sales process](navigating-sales-process-dashboard.md)|Sales process manager|
|Adjust which entities are actively tracked by linking and delinking records or changing how records are linked to focus on relevant sales activities.|[Link and delink records](navigating-sales-process-dashboard.md)|Sales process manager|
|Streamline communication, task management, and documentation, which accelerates decision-making and improves cross-functional alignment and collaboration without having to leave the workspace.|[View consolidated emails and tasks, create checklists and attachments, and use integrated chat](navigating-sales-process-dashboard.md)|Sales process manager|

## Related links

The following topics provide more information about configuring and using Lead-to-Cash Process Management:

-   [Configuring Lead-to-Cash Process Management](configuring-lead-cash-process-management.md)
-   [Using Lead-to-Cash Process Management](using-lead-cash-process-management.md)
-   [Lead-to-Cash Process Management reference](../reference/lead-cash-process-management-reference.md)

