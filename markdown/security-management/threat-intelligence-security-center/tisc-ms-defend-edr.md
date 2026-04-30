---
title: Send observables to EDR
description: Send observables to the EDR security tool.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft Defender for EDR Integration, TISC Security Tools Integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
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

    For example, select the implementation associated to Microsoft Defender EDR.

7.  Click **Next**.

8.  Select the run time details such as the **Title** and **Description** of the implementation.

9.  Click **Submit**.

    The selected action is executed and an information message is displayed that Observable Send to EDR execution has started and the results of this execution will be available under the Activity Stream after the execution is complete.

    **Note:** Once the execution is initiated or completed, a work notes is posted on the activity stream of the form view and you can verify the execution progress accordingly.


**Parent Topic:**[Microsoft Defender for EDR Integration](../concept/tisc-ms-defender-integration.md)

