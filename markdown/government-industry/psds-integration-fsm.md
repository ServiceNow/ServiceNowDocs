---
title: Integration with Field Service Management
description: The Public Sector Digital Services integration with the ServiceNow Field Service Management application enables you to view work order and work order task information from a public sector case.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate, Public Sector Digital Services \(PSDS\)]
---

# Integration with Field Service Management

The Public Sector Digital Services integration with the ServiceNow® Field Service Management application enables you to view work order and work order task information from a public sector case.

Integrating the Public Sector Digital Services application with the Field Service Management application enables you to create and view all work orders and appointments related to your case, depending on the business needs.

The Field Service Management application users can view the constituent, household, business, and contacts on work orders and work order tasks in the Field Service Management application.

## Product use rights included with this application

With the integration with Field Service Management, Public Sector Digital Services agents can create and view all work orders and appointments related to their cases.

Field Service Management field agents can view relevant Public Sector Digital Services data from work orders with the right roles.

External users with the snc\_external and other relevant Public Sector Digital Services and Customer Service Management \(CSM\) roles can view all case-related work orders and appointments related to their accounts.

## Configuring the integration with Field Service Management

To configure the Public Sector Digital Services application integration with the Field Service Management application, complete these steps:

1.  Activate the Customer Service with Field Service Management plugin. \(com.snc.csm\_fsm\_integration\).
2.  Add UI actions to the PSDS case type tables where needed. Depending on your experience, you can also add some actions to relevant playbooks.
3.  Add the Work orders related list to the PSDS case type tables for all relevant views on Classic UI and or Workspace.
4.  If you're an FSM field agent, you can view the relevant PSDS customer data from the work orders by being assigned with the right customer data viewer roles.

    **Note:** An administrator must assign the appropriate PSDS customer data viewer roles to FSM field agents so that they can view the relevant PSDS customer data from work orders. For more information on roles, see [Roles installed with graPublic Sector Digital Services](../reference/roles-installed-with-public-sector-digital-services.md).


