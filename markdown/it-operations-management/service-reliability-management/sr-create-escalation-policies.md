---
title: Set up escalation policies for your team in SRM
description: Set up an escalation policy for your team to ensure that alerts or incidents are resolved in a timely manner by the appropriate team member.
locale: en-US
release: yokohama
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Working with SRM teams, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Set up escalation policies for your team in SRM

Set up an escalation policy for your team to ensure that alerts or incidents are resolved in a timely manner by the appropriate team member.

## Before you begin

Before creating an escalation policy, you must create an on-call shift for your team.

**Note:** Only the responder who created the team or the manager of the team can set up an escalation policy for that team.

Role required: Responder, Manager, or Administrator

## About this task

An escalation policy is a set of guidelines that outlines how and when incidents should be elevated to higher levels of authority. It delineates clear procedures and responsibilities for escalation to help responders promptly address problems. It defines the order in which notifications should be escalated if an alert or incident isn’t acknowledged or resolved within a defined amount of time. If no one responds, the escalation is based on your defined policies until someone responds. After a team member responds, the escalation policy stops escalating and no further notifications are sent.

**Note:** Escalation workflow is triggered only if there’s an active shift.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  From the primary navigation, select the **Teams** icon \(![Teams.](../image/icon-sr-teams.png)\).

3.  Select the **Escalation triggers and policies** tab.

4.  Under **Escalation policies** in the left panel, select **Create policy**.

5.  On the Escalation policy form, fill in the fields.

    For more information, see [Set up escalation policies form in SRM](../reference/sr-set-up-escalation-policies-form.md)

6.  Select **Add escalation step** to define the additional steps for escalation and escalation path.

    For more information on the Add escalation step form, see [Set up escalation policies form in SRM](../reference/sr-set-up-escalation-policies-form.md).

7.  Select **Save changes**.

8.  Add another escalation policy to the team for another category of alert or incident by selecting **Add a policy**.


-   **[Create an escalation trigger for an SRM team](sr-trigger-escalation-policy.md)**  
Define conditions that trigger a team's escalation policy in Service Reliability Management \(SRM\).

**Parent Topic:**[Working with SRM teams](../concept/sr-work-teams.md)

