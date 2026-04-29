---
title: Components installed with Workplace Case Management
description: Several types of components are installed with activation of the Workplace Case Management application, including tables, user roles, and business rules.
locale: en-US
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Case Management

Several types of components are installed with activation of the Workplace Case Management application, including tables, user roles, and business rules.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Group roles: Workplace Event Planners

</td><td>

AI agentic workflow autonomously assigns emergency maintenance request and change event request submitted by a workplace user. For more information, see [Manage temporary space closures agentic workflow](../../now-assist-wsd/concept/maintenance-meeting-room-agent-ai.md) and [Help manage workplace reservations agentic workflow](../../now-assist-wsd/concept/manage-workplace-reservations-agent-ai.md).

</td><td>

-   sn\_wsd\_case.case\_writer
-   sn\_wsd\_rsv.reservation\_planner

</td></tr><tr><td>

Workplace Case Management admin\[sn\_wsd\_case.admin\]

</td><td>

-   Sets up data related to workplaces services.
-   Creates workplace services.
-   Has complete access to the application.

</td><td>

sn\_wsd\_case.manager

</td></tr><tr><td>

Workplace case Manager\[sn\_wsd\_case.manager\]

</td><td>

-   View all cases.
-   Manage cases.
-   Create, read, update, and delete Case templates.
-   Create, read, update, and delete Task templates.
-   Create, read, update, and delete Workplace Services.
-   Create, read, update, and delete Workplace Service Activities.
-   Create, read, update, and delete Approval options.
-   Create, read, update, and delete an Escalation rule.
-   Create, read, update, and delete Fulfillment instructions.
-   Perform agent-related actions.

</td><td>

-   template\_editor\_global
-   sn\_wsd\_case.workplace\_agent

</td></tr><tr><td>

Workplace case agent\[sn\_wsd\_case.workplace\_agent\]

</td><td>

In addition to all the permissions of a Workplace case writer,-   Can view flow executions.
-   Can write knowledge base articles.

</td><td>

-   sn\_wsd\_case.case\_writer
-   sn\_wsd\_core.kb\_writer
-   flow\_operator

</td></tr><tr><td>

Workplace case writer\[sn\_wsd\_case.case\_writer\]

</td><td>

-   Create, read, update, and delete Workplace Tasks.
-   Read Task templates.
-   Create, read, update, and delete Workplace cases.
-   Read the following:
    -   Escalation rules
    -   Fulfillment instructions

</td><td>

-   sn\_wsd\_core.task\_writer
-   sn\_wsd\_case.case\_reader

</td></tr><tr><td>

Workplace case reader\[sn\_wsd\_case.case\_reader\]

</td><td>

Has read permissions to access all -   Workplace tasks
-   Workplace cases

</td><td>

sn\_wsd\_core.task\_reader

</td></tr><tr><td>

Workplace reservation admin sn\_wsd\_case.bypass\_services\_limitation

</td><td>

With this role, user can see all the service items while creating a reservation, even which are in the lead time.

 User can remove an added service item for an existing reservation, even if it is

-   Already arranged
-   In lead time of ordering
-   When the **Restrict cancellation of requested services** is enabled true.

 Can configure **Lead time of ordering** at service item or service item location.

</td><td>

sn\_wsd\_case.bypass\_services\_limitation

</td></tr></tbody>
</table><table id="table_bdk_pts_x2c"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Workplace user\[sn\_wsd\_core.workplace\_user\]

</td><td>

From Workplace Case Management version 1.21.0, this role has write access to the Workplace Case \[sn\_wsd\_case\_workplace\_case\] table.

</td><td>

None

</td></tr></tbody>
</table>## Tables

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workplace Case\[sn\_wsd\_case\_workplace\_case\]

</td><td>

Extends Workplace Task \[sn\_wsd\_core\_workplace\_task\] table. Stores information about all the Workplace cases in the application.: If **WSD: Archive old workplace tasks** archival rule is applied then Workplace Case \[sn\_wsd\_case\_workplace\_case\] table is also archived. For more information, see [Apply the archive rule](../../workplace-service-delivery/task/wsd-tables-purge-policy.md).

</td></tr><tr><td>

Workplace Service\[sn\_wsd\_case\_workplace\_service\]

</td><td>

Extends the Application File table. Stores information about all the Workplace Services in the application.

</td></tr><tr><td>

Workplace Service Activity\[sn\_wsd\_case\_workplace\_service\_activity\]

</td><td>

Extends the Application File table. Stores information about all the Workplace Service Activities in the application.

</td></tr><tr><td>

Case Tier Escalationsn\_wsd\_case\_tier\_definition

</td><td>

Stores information about all the workplace case escalation rules created in the application.

</td></tr><tr><td>

Fulfillment Instructionsn\_wsd\_case\_fulfillment\_instruction

</td><td>

Stores information about all the fulfillment instructions created for workplace services in the application.

</td></tr><tr><td>

Request Service Items\[sn\_wsd\_case\_service\_item\_request\]

</td><td>

Stores information about all the workplace service items requested using a workplace service.**Note:** If **WSD: Archive old workplace tasks** archival rule is applied then Request Service Items \[sn\_wsd\_case\_service\_item\_request\] table is also archived. For more information, see [Apply the archive rule](../../workplace-service-delivery/task/wsd-tables-purge-policy.md).

</td></tr><tr><td>

Workplace Service Item Location\[sn\_wsd\_case\_m2m\_service\_item\_location\]

</td><td>

Extends the Workplace Service Location table. Stores information about all the workplace service item locations added in the application.

</td></tr><tr><td>

Workplace Service Location\[sn\_wsd\_case\_m2m\_service\_location\]

</td><td>

Stores information about all the workplace service locations.

</td></tr><tr><td>

Workplace Field Mapping\[sn\_wsd\_case\_workplace\_field\_mapping\]

</td><td>

Stores information about all the workplace field mappings created in the application.

</td></tr><tr><td>

Workplace Service Item\[sn\_wsd\_case\_workplace\_service\_item\]

</td><td>

Stores information about all the workplace service items created in the application.

</td></tr><tr><td>

Workplace Template Configuration\[sn\_wsd\_case\_workplace\_template\_configuration\]

</td><td>

Stores information about all the workplace template configurations created in the application.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Case Management references](../concept/workpalce-case-mgmt-references.md)

**Related topics**  


[Properties installed with Workplace Case Management](properties-installed-with-workplace-case-mgmt.md)

[Workplace Service form](workplace-service-form.md)

[Workplace Location Assignment service](location-assignment-service.md)

