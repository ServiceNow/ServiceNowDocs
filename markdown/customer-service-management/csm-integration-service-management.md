---
title: CSM integration with IT Service Management overview
description: Customer Service Management provides an integration with the Incident, Problem, Change, and Request Management applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integrate with IT Service Management, Integrate, Customer Service Management]
---

# CSM integration with IT Service Management overview

Customer Service Management provides an integration with the Incident, Problem, Change, and Request Management applications.

## Plugins

Customer Service Management integration with Service Management requires the following plugins:

-   Customer Service with Service Management plugin \(com.sn\_cs\_sm\)
-   Customer Service with Request Management plugin \(com.sn\_cs\_sm\_request\)

For additional information, see [Integrate with Service Management](../task/configure-csm-sm-integration.md).

## Roles

The Service Management integration plugins do not add any roles to the customer service agent \(sn\_customerservice\_agent\) role. To enable the Service Management integration features, you must assign the CSM/ITSM integration roles included with the Incident Management application to the agents who need this capability. For more information, see [Assign CSM/ITSM integration roles](../task/assign-csm-itsm-integration-roles.md#).

## Creating records for a case

The Service Management integration plugins add the following menu items to the Additional Actions menu on the Case form. Agents can use these menu items to create records for a case.

-   Create Incident
-   Create Problem
-   Create Request
-   Create Normal Change
-   Create Standard Change

**Note:** Agents can create or associate one incident, problem, or change record with a case. After a record is created or associated with a case, the corresponding menu items are no longer available on the Additional Actions menu.

For more information, see [Create incident, problem, change, and request records from cases](csm-item-agent-tasks.md#).

## Viewing incident, problem, and change records related to a case

The Service Management integration plugins add the Related Records form section to the Case form. This section includes the following fields:

-   Incident
-   Problem
-   Change Request
-   Caused by Change

When an incident, problem, or change record is created from a case, or an existing record is associated with a case, the record number is added to the corresponding field in the Related Records form section.

## Viewing requests related to a case

When a request is created from a case, or an existing request is associated with a case, the request record number is added to the **Requests** related list on the Case form.

**Note:** Agents can create multiple requests for a case.

## Related records list widget for external customers

When viewing a case on the Customer or Consumer Service Portal, external users can see other records that are associated with the case in the Related Records list widget. These records can include problems, changes, and requests. Users can click a record in the Related Records widget to view additional details in a pop-up window.

**Note:** If a case does not have any related records, the Related Records widget does not appear on the case view page.

From the Customer and Consumer Service Portals, users can view lists of cases and requests by doing one of the following:

-   Clicking **My Lists** in the portal menu header.
-   Clicking **Requests** &gt; **All Requests** in the portal menu header.

For more information, see [View case records from the Customer and Consumer Service Portals](../task/view-related-records-from-portal.md).

## Using case resolution codes

The Service Management integration plugins provide the following case resolution codes.

Agents can select these codes from the **Resolution code** field in the **Resolution Information** section on the Case form.

-   Solved – Fixed by closing related PRB
-   Solved – Workaround provided based on open PRB
-   Solved – Fixed by closing related Change Request
-   Solved – Fixed by closing related Incident
-   Solved – Related Request is Closed Complete

## IT Service Management integration and Major Issue Management

The major issue management feature works with the CSM integration with IT Service Management as follows:

-   A major issue manager with the itil role can create incident, problem, change, and request records from a major case.
-   When a major case candidate with an associated record is accepted as a major case:
    -   A new major case is created and the candidate becomes a child of the major case.
    -   The related record information is copied from the child case to the major case.
    -   For the child case, the options to create related records are removed from the Additional Actions menu.
    -   For the child case, the fields in the Related Records form section are read-only.
    -   Updates to the related records appear in the work notes of the major case. These updates are added to the child case when fields are synchronized from the major case to the child case.
-   A major case and child cases can have different types of related records. This can happen when an existing case with a related incident, problem, change, or request record is added as a child of a major case. When updates are made to the record related to the child case, information about the update is added to the child case work notes.
-   If a major case and child cases have the same related record, updates to that record are added to the major case work notes. These notes are copied from the major case to the child cases if:
    -   The **sn\_customerservice.case\_fields\_to\_sync** property is enabled.
    -   The field in the in the Related Records form section is added to the **sn\_customerservice.case\_fields\_to\_sync** property.
-   If a major case and child cases have different related records of the same type, updates to the records are copied only to the respective cases.

