---
title: CSM integration with Request Management
description: Integration with the Request ManagementCSM application enables customer service agents to create request records from cases or associate existing request records to cases. It also enables customers to create requests from the Customer and Consumer Service Portals.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Overview, Integrate with IT Service Management, Integrate, Customer Service Management]
---

# CSM integration with Request Management

Integration with the Request ManagementCSM application enables customer service agents to create request records from cases or associate existing request records to cases. It also enables customers to create requests from the Customer and Consumer Service Portals.

With this integration, customer service agents can:

-   Create one or more requests on behalf of a customer from an existing customer service case.
-   Associate an existing request to a case.
-   Remove an associated request from a case.
-   View a list of requests associated with a case in the **Requests** related list.
-   View the following in the case work notes:

    -   Request state changes.
    -   Additional comments added to the request item record.
    **Note:** When creating a request from a case, if the agent chooses a catalog item that is using cart v1 \(the use\_sc\_layout field is not checked\), the case is not set as the parent of the request.


## Plugins

Integration with Request Management requires the Customer Service with Request Management plugin \(com.sn\_cs\_sm\_request\).

## Roles

The following roles enable customer service agents to view and create requests for customer service cases.

-   sn\_request\_read
-   sn\_request\_write

For more information, see [Assign CSM/ITSM integration roles](../task/assign-csm-itsm-integration-roles.md#).

## Enabling the Create Request UI action for case types

To enable the **Create Request** UI action for a case type table that extends the Case \[sn\_customerservice\_case\] table, add an entry for the case type to the Request Parent Mapping \[request\_parent\_mapping\] table. For more information, see [Enable the Create Request UI action for case types](../task/enable-create-request-case-type.md).

## Synchronizing data between the request and the case

Work notes are synchronized from the request to the case when:

-   The request state changes.
-   The request is closed.
-   Additional comments are added to the request.

**Note:** When a request is closed, the case does not automatically move to solution proposed.

## Communicating with the requester

The task fulfiller can communicate with the requester if additional information is needed. Use the **Additional comments** field on the request to communicate with the requester through the case. Information added to the **Additional comments** field on the request is synchronized to the case work notes.

If the case is the parent of the request, notifications to the requester are suppressed when additional comments are added to the request by the fulfiller.

**Related topics**  


[Create a request on behalf of a customer or consumer](../task/agent-create-request-for-customer.md)

[Create a request record from a case](csm-item-agent-tasks.md#)

[Create a request from the Customer and Consumer Service Portals](../task/create-request-from-csp.md)

