---
title: CSM integration with Change Management
description: Integration with the Change Management application enables customer service agents to create change records from cases or associate existing change records to cases.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Overview, Integrate with IT Service Management, Integrate, Customer Service Management]
---

# CSM integration with Change Management

Integration with the Change Management application enables customer service agents to create change records from cases or associate existing change records to cases.

With this integration, customer service agents can perform the following tasks:

-   Create a change from a case.
-   Associate an existing open change to a case.
-   Remove an associated change from a case.
-   View the following information in the case work notes:
    -   State changes for the change record.
    -   Additional comments added to the change record.

**Note:** A case can be associated with one change. If a case is already associated with a change, the **Create Normal Change** and **Create Standard Change** options do not appear on the Additional Actions menu.

## Plugins

Integration with Change Management requires the Customer Service with Service Management plugin \(com.sn\_cs\_sm\).

## Roles

The following roles enable customer service agents to view and create changes for customer service cases.

-   sn\_change\_read
-   sn\_change\_write

For more information, see [Assign CSM/ITSM integration roles](../task/assign-csm-itsm-integration-roles.md#).

## Synchronizing data between the change and the case

Work notes are synchronized from the change to the case when:

-   The change state or change type is updated.
-   Additional comments are added to the change record.
-   When the change associated with a case is put on hold, the work notes are updated with the hold reason.
-   When a hold on the change associated with a case is removed, the work notes on the case are updated.
-   When the change is resolved or closed.

## Change form related lists

Integration with the Change Management application adds the following related lists to the Change form:

-   Cases Fixed by Change
-   Cases Caused by Change

## Standard change record producer behavior

When a record producer for a standard change or normal change is created and exposed to customer service agents from the Customer or Consumer Service Portals:

-   The record producer only appears in the portal after clicking the **Create Request** UI action.
-   The record producer does not appear as part of Standard Change catalog items.
-   If the agent chooses to create a Standard Change from the normal record producer, the Standard Change is created but the change record is not linked with the case.

