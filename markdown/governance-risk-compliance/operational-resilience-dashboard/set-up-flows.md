---
title: Set up the flows in Workflow Studio
description: Set up the flows and conditions for Digital resilience incident reporting in Workflow Studio. As administrators of the Operational Resilience application, you can update \(customize\) the flow configurations to meet your organizational requirements.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Configure, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Set up the flows in Workflow Studio

Set up the flows and conditions for Digital resilience incident reporting in Workflow Studio. As administrators of the Operational Resilience application, you can update \(customize\) the flow configurations to meet your organizational requirements.

## Before you begin

Role required: sn\_oper\_res.admin, sn\_dri\_inc\_rptg.digital\_resilience\_incident\_admin

## About this task

The Workflow Studio lists the preconfigured flows and conditions for Digital resilience incident reporting.

## Procedure

1.  Navigate to **All** &gt; **Flow Designer** and open the Digital resilience incident reporting flows.

    The following flows used from previous releases of the Digital resilience incident reporting application have been deprecated:

    1.  Digital Resilience Incident Flow
    2.  Digital Resilience SIR Flow
    3.  DRI Business service Trigger
    **Note:** To use the previously deployed flows, you must deactivate the new flows \(listed in this section\) and then activate the Digital Resilience Incident Flow, Digital Resilience SIR Flow, and DRI Business Service Trigger Flow.

    The following flows in Digital resilience incident reporting are still active.

    1.  Digital Resilience Incident Approval Flow
    2.  DRI case create/update on incident update
    3.  DRI case create/update on security incident update
    4.  DRI case creation on incident entity insert
    5.  DRI case creation on SIR entity insert
    New flows are introduced in Digital resilience incident reporting for action task management, regulation management, and trigger conditions for multiple regulators as shown in the example.

    1.  Action task automation for regulation addition
    2.  Action task automation on action task update
    3.  Action task automation on DRI case updates
    4.  Action task automation on regulation updates
    5.  DRI Business Service Trigger For Multiple Regulators
    ![Digital resilience incident reporting flows. For the text description, refer to the text that precedes this image.](../image/trigger-flows-wf-studio.png)

    **Note:** If the Security Incident Response application is installed in your instance, flows related to security incidents \(SIR\) are listed in the Flows list view.

2.  To update \(customize\) the flow configurations to meet your organizational requirements, select **Edit flow** in the desired flow, update the conditions, and select **Done**.

    A sample condition for the "DRI Business Service Trigger For Multiple Regulators" flow is shown in the example.

    ![Example for modifying the flow conditions. For the text description, refer to the text that precedes this image.](../image/flow-conditions.png)

3.  To publish the flow, choose the flow from the list and select **Publish**.

    Published flows are available to the users of the Digital resilience incident reporting application.


