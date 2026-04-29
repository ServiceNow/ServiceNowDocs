---
title: Group similar workplace cases under a parent case
description: Categorize cases that have similar issues and that require the same resolution under a single parent case. Reduce the time spent on resolving multiple workplace cases.
locale: en-US
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Group similar workplace cases under a parent case

Categorize cases that have similar issues and that require the same resolution under a single parent case. Reduce the time spent on resolving multiple workplace cases.

## Before you begin

Role required: sn\_wsd\_case.admin or sn\_wsd\_case.manager or sn\_wsd\_case\_workplace\_agent

## About this task

Assign a workplace case to a parent workplace case. The resolution provided to the parent case will also be applied to the child case.

You can also assign a case to a parent case even if the **State** field of the parent is set as Canceled or Closed Complete. When the case is assigned, the state of the child case is automatically updated as Canceled or Closed complete.

The following scenarios can occur when you assign a parent case:

-   You can view all the cases associated to a parent case in the **Related Cases** tab.
-   The child case is updated whenever the parent case is updated. Updates like comments, work notes, and state changes are automatically applied to the child case. If the state of the child case is set as Canceled, the updates will no longer be applied. If you do not want to copy the comments, work notes and state changes to the child cases, you can set the **Update Child Case - Work Notes &amp; Comments** to **False**.
-   State changes in the parent case are copied to the child case, except for state changes to Awaiting acceptance.
-   Any updates individually made on the child case will not be applied to the parent case.

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Cases**.

2.  Select one of the following modules:

    -   All
    -   Open - Unassigned
    -   Open
    -   Assigned to my group
    -   Assigned to me
3.  Select the workplace case to which you want to assign a parent workplace case.

4.  In the **Parent case** field, select the workplace case that you want to assign as a parent.

    **Important:** Do not select a child case as a parent case. Otherwise, the case will encounter looping. For example, if WCASE0001001 is parent of WCASE0001002 and WCASE0001003, then WCASE0001002 and WCASE0001003 can't be parent of WCASE0001001.

5.  Click **Save**.


## Result

The workplace case is assigned to a parent case.

**Important:** The case selected in the **Parent case** field and the case displayed in the **Parent** field are different. The workplace case displayed in the **Parent** field is generated from the workplace service to which the case is associated. A parent is assigned automatically if the **Activity type** of the workplace service is **Task** or **Child case**.

**Parent Topic:**[Configuring Workplace Case Management](../concept/workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management](install-workplace-case-mgmt.md)

[Create a Workplace case template](wsd-case-template.md)

[Create a Workplace task template](wsd-task-template.md)

[Smart Assessment for Workplace Case and Task](smart-assessment-for-workplace-case-and-task.md)

[Automating seat assignment for new hires](../concept/auto-assign-new-hires.md)

[Configure Approval options](config-approval-optns.md)

[Configure a Record producer](wsd-create-record-producer.md)

[Configuring a record producer for request edit](../concept/config-case-edit-rp.md)

[Configuring a record producer for reservation](../concept/config-reservation-rp.md)

[Create an SLA Definition](create-sla-defn-case-mgmt.md)

[Create a Workplace service](create-workplace-service.md)

[Add a workplace service item to a workplace service](add-workplace-service-items.md)

[Create a workplace template configuration](create-workplace-template-confguration.md)

[Create a workplace field mapping](create-workplace-field-mapping.md)

[Configure an escalation rule](configure-escalation-rule.md)

[Add Fulfillment instructions](add-fulfillment-instructions.md)

