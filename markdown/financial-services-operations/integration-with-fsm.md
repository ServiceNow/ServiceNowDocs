---
title: Integrating with Field Service Management
description: Integrating Financial Services Operations with Field Service Management enables you to create and view all work orders and appointments related to your case, depending on your business needs.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate, Financial Services Operations \(FSO\)]
---

# Integrating with Field Service Management

Integrating Financial Services Operations with Field Service Management enables you to create and view all work orders and appointments related to your case, depending on your business needs.

Field Service Management users can view account and contact information on work orders and work order tasks in the Field Service Management application.

## Product use rights included with this application

If you have purchased a subscription for both the  Financial Services Operations \(FSO\)  application and the Field Service Management \(FSM\) application, FSO agents can create and view all work orders and appointments related to their FSO cases, while FSM field agents can view relevant FSO data from Work Orders. External users with the snc\_external and other relevant FSO and CSM roles can view all case-related work orders and appointments related to their accounts.

## Configuring integration with Field Service Management

The recommended implementation of Financial Services Operations application integration with Field Service Management is to complete these initial configuration steps.

-   Activate the Customer Service with Field Service Management plugin \(com.snc.csm\_fsm\_integration\)
-   Add UI actions to FSO case type tables where needed. Depending on your desired experience, you can also add actions to relevant playbooks.
-   Add the Work orders related list to FSO case type tables for all relevant views, such as a workspace.
-   If FSM field agents need to access core FSO data model objects, such as Insurance Policies, add the sold\_product reference field to the work order \[wm\_order\] table.
-   Assign FSO viewer roles to FSM field agents for both the sold\_product extension tables and FSO case type tables.

    **Note:** Financial Services Operations applications have read-only roles, such as sn\_bom.auto\_ins\_policy\_viewer and sn\_bom.b2b\_credit\_card\_account\_viewer, for all objects.


To learn more, see Integration with Industry products.

**Parent Topic:**[Integrate applications](fso-integrate-other-applications.md)

