---
title: Track the progress of an escalation
description: Use the On-Call Escalation Tracking page for full visibility into the time line of an active or closed escalation as it progresses through its on-call escalation path.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Escalations in On-Call Scheduling, Defining On-Call Scheduling escalation process, On-Call Scheduling, IT Service Management]
---

# Track the progress of an escalation

Use the On-Call Escalation Tracking page for full visibility into the time line of an active or closed escalation as it progresses through its on-call escalation path.

## Before you begin

Role required: Any role that enables the user to read incidents.

## About this task

**Note:**

-   Escalation logging must be enabled to view the On-Call Escalation Tracking page. See the **com.snc.on\_call\_rotation.log\_escalations** property in [System properties for On-Call Scheduling](../reference/on-call-properties.md).
-   An on-call escalation is canceled when the assignment group of the associated task record, for example, an incident, changes to a different group without a matching trigger rule. It ensures that an existing irrelevant escalation workflow is no longer associated with that task record.![An on-call escalation has been cancelled.](../image/canceled-escalation-oncall.png)

## Procedure

1.  Navigate to **Incident** and open the incident.

    The **Assignment group** field includes the On-Call Escalation Tracking icon \(![On-Call escalation tracking icon](../../../product/incident-management/image/icon-esc-tracking-oncall.png)\) that indicates the active status of the escalation. Green indicates an active escalation, and black indicates a finished escalation.

2.  Click the On-Call Escalation Tracking icon.

    The On-Call Escalation Tracking dialog box opens.


## On-call escalation tracking

![On-call escalation tracking dialog box](../image/esc-tracking-popup-accept-annotated.png "On-call escalation tracking dialog box")

1.  The Escalation Path section identifies the escalation with start time, group, and shift that handles the escalation, and Escalation category.
2.  Indicators on the time line show status:
    1.  For active escalations, a green arrow on the path time line indicates the current active response phase.
    2.  Unfilled check mark: Skipped response.
    3.  Filled green check mark: Accepted response.
    4.  Red X: Rejected response.
3.  Click the escalation timestamp for an escalatee or escalatee's name to view timing details. The list on the **Contact Information** tab shows contact times, modes of contact, and responses for the associated escalation phase.

    The dots for the escalation timestamps indicate overall acceptance. Point to a dot to view further information. Color codes of the dots:

    -   Green: At least one escalatee has accepted the escalation.
    -   Orange: At least one escalatee has rejected the escalation.
    -   Red: All escalatees have rejected the escalation.
    **Note:** To enhance the visual differences between dots, use the high-contrast user interface.

4.  Depending on the contact settings, you can call or send a direct message to the person from the escalatee's **Profile** tab.![On-call tracking progress](../image/delegator-escalation-tracking-oncall.png)

    Click ![Info icon](../image/icon-information.png) to view delegator and delegated user's information.


**Parent Topic:**[Escalations in On-Call Scheduling](../concept/escalations-oncall.md)

**Related topics**  


[Designing an escalation process](../concept/designing-escalation-process-oncall.md)

[View details in an escalation log](view-escalation-logs-oncall.md)

