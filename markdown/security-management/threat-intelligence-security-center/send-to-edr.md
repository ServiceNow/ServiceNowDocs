---
title: Send observables to EDR
description: Send observables to the EDR security tool.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/threat-intelligence-security-center/send-to-edr.html
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-08-15"
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

7.  Select **Next**.

8.  Select the run time details such as the **Action Type** and **Description** of the implementation.

    \[Omitted image "tisc-send-to-edr-runtime.png"\] Alt text: Send observable to CrowdStrike - Runtime details

    The available options for the CrowdStrike during implementation run time details are:

    -   **No Action \(Save indicator in IOC management, but take no action.\)**: The observable is saved in CrowdStrike IOC management and no detection or block action is applied.
    -   **Detect Only \(Show as a detection and take no other action.\)**: The observable is shown as a detection in CrowdStrike Falcon EDR and no other action is applied.
    -   **Block \(Block and show as detection. Applies only to MD5 and SHA256 observable types.\)**: The observable is blocked and shown as a detection.
    -   **Block, hide detection \(Block and detect but hide from Activity &gt; Detections. Applies only to MD5 and SHA256 observable types.\)**: The observable is blocked and detected, and the detection isn't shown in **Activity** &gt; **Detections** in the CrowdStrike Falcon console.
    **Important:**

    When an observable has no threat severity, the severity low is sent for the **Detect Only** and **Block** actions.

9.  Select **Submit**.

    The selected action is executed and the information message Observable Send to EDR execution has started is displayed.

    **Note:**

    -   After the execution is initiated or completed, a work note is posted on the activity stream of the form.
    -   **Send to EDR** action is also available on the observables list under **Artifacts** tab for a case record. For more information, see [Add artifacts to cases or case tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/add-artifacts-to-a-case-s.md).

**Parent Topic:**[CrowdStrike Falcon EDR integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/crowdstrike-edr-integration.md)

