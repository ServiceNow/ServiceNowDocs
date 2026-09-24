---
title: On-Call Scheduling subflows
description: On-Call Scheduling subflows are reusable automated processes for on-call escalation and notification.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/on-call-scheduling/on-call-scheduling-subflows-overview.html
release: brazil
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: reference
last_updated: "2026-09-19"
reading_time_minutes: 1
breadcrumb: [Reference for on-call scheduling, On-Call Scheduling, IT Service Management]
---

# On-Call Scheduling subflows

On-Call Scheduling subflows are reusable automated processes for on-call escalation and notification.

## Using subflows for on-call escalation

A subflow consists of a sequence of reusable actions, data inputs, and outputs. In contrast to flows, subflows don't have a trigger but instead run when called from a flow, from another subflow, or from a script. The subflows enables you to easily configure channels, and notification and response messages. The following subflows are available for On-call:

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

Using Workflow Studio, you can build and configure various components such as subflow inputs, outputs, actions, and flow variables such as escalation levels. You can use the contextual comments in the flow designer to help you configure the subflows. For more information on building and configuring subflows in Workflow Studio, see [Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio.md).

## Subflows activation and uses

Starting from the Zurich release, for the zBoot or new users, On-Call Scheduling uses subflows. Workflows are no longer supported.

For those upgrading from previous releases, existing workflows continue to be supported in the Zurich release. Each workflow has a corresponding subflow with similar name and functionality.

To activate the subflows, you must navigate to **All** &gt; **On-Call Scheduling** &gt; **Administration** &gt; **Trigger Rules** and select the subflow for a trigger rule to activate and use the subflow. For more information, see [Create an escalation trigger rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/on-call-scheduling/create-trigger-rule-oncall.md).

**Note:** To avoid configuration mismatches, any change you make to a trigger rule's subflow configuration must be also updated in the corresponding Notify Voice/SMS configuration for the preferred channel.

For using subflows in Service Operations Workspace \(SOW\), SOW version must be 8.0 or later.

-   **[Subflows installed with On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/on-call-scheduling/subflows-installed-on-call-scheduling.md)**  
Subflows are installed with On-Call Scheduling to support building on-call escalation notification configurable flows.

**Parent Topic:**[Reference for on-call scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/on-call-scheduling/reference-for-on-call-scheduling.md)

