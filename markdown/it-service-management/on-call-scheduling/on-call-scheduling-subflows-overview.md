---
title: On-Call Scheduling subflows
description: Subflows in On-Call Scheduling enable you to build and configure on-call escalation notification flows.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference for on-call scheduling, On-Call Scheduling, IT Service Management]
---

# On-Call Scheduling subflows

Subflows in On-Call Scheduling enable you to build and configure on-call escalation notification flows.

## Using subflows for on-call escalation

A subflow is an automated process consisting of a sequence of reusable actions, data inputs, and outputs. In contrast to flows, subflows do not have a trigger but instead run when called from a flow, from another subflow, or from a script. Compared to workflows, subflows enables you to easily configure channels, and notification and response messages. Maintain, build, and modify your own custom on-call scheduling flows in Workflow Studio with subflows for new instances. The following subflows are available with On-call:

-   On-Call: Assign
-   On-Call: Assign and Notify
-   On-Call: Assign by Acknowledgment
-   On-Call: Assign by Acknowledgement per Rota
-   On-Call: Assign by Acknowledgement Voice
-   On-Call: Check Assignment Response
-   On-Call: Conference Call Escalation
-   On-Call: Escalations by Email
-   On-Call: Escalation By Email per Rota
-   On-Call: Time-off approval

Using Workflow Studio, you can build and configure various components such as subflow inputs, outputs, actions, and flow variables such as escalation levels. You can use the contextual comments in the flow designer to help you configure the subflows. For more information on building and configuring subflows in Workflow Studio, see

Workflow Studio

## Subflows activation and uses

Starting from the Zurich release, for the zBoot or new users, On-Call Scheduling uses subflows and workflows are no longer supported.

For existing or upgrade users, in Zurich, your current workflows continue to be supported along with the subflows.

With the migration from legacy workflow to subflows, each workflow has a corresponding subflow with similar name and functional capabilities.

To activate the subflows, you must navigate to **All** &gt; **On-Call Scheduling** &gt; **Administration** &gt; **Trigger Rules** and select the subflow for a trigger rule to activate and use the subflow. For more information, see [Create an escalation trigger rule](../task/create-trigger-rule-oncall.md).

For using subflows in Service Operations Workspace \(SOW\), SOW version must be 8.0 or later.

-   **[Subflows installed with On-Call Scheduling](subflows-installed-on-call-scheduling.md)**  
Subflows are installed with On-Call Scheduling to support building on-call escalation notification configurable flows.

**Parent Topic:**[Reference for on-call scheduling](../../user-administration/concept/reference-for-on-call-scheduling.md)

