---
title: Send observables to EDR
description: Send observables to the EDR security tool.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Falcon EDR integration, TISC Security Tools integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Send observables to EDR

Send observables to the EDR security tool.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click the **Threat Intel Library** icon.

3.  Go to **Observables** &gt; **All Observables**.

4.  Open any observable record.

5.  Select **Send to EDR**.

    The Send to EDR **Implementations** modal screen is displayed.

6.  Select the required implementation from the list.

    ![Send observable to CrowdStrike - Implementation](../image/tisc-send-to-edr.png)

7.  Click **Next**.

8.  Select the run time details such as the **Action Type** and **Description** of the implementation.

    ![Send observable to CrowdStrike - Runtime details](../image/tisc-send-to-edr-runtime.png)

    The available options for the CrowdStrike during implementation run time details are:

    -   **No Action \(Save the indicator for future use, but take no action\)**: In the Observable form view, the threat severity of the observable is optional for CrowdStrike Falcon EDR.
    -   **Detect \(Enable detections for the indicator at record's threat severity\)**: In the Observable form view, the threat severity is mandatory for CrowdStrike Falcon EDR. The threat severity of the observable shouldn’t be empty for that selected observable.
9.  Click **Submit**.

    The selected action is executed and an information message is displayed that Observable Send to EDR execution has started.

    **Note:**

    -   Once the execution is initiated or completed, a work notes is posted on the activity stream of the form view.
    -   **Send to EDR** action is also available on the observables list under **Artifacts** tab for a case record. For more information, see [Add artifacts to case\(s\) or case task\(s\)](add-artifacts-to-a-case-s.md).

**Parent Topic:**[CrowdStrike Falcon EDR integration](../concept/crowdstrike-edr-integration.md)

