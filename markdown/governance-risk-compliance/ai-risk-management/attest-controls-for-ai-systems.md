---
title: Create control attestations for an AI asset
description: Create control attestations for AI assets to document the existence, implementation, and effectiveness of controls that govern behavior, data usage, performance, and risk posture. Attestations serve as formal evidence that the AI asset meets regulatory, ethical, security, and operational standards.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/attest-controls-for-ai-systems.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [control attestation, AI asset, attest controls, governance controls, AI Risk and Compliance, build and test, control compliance]
breadcrumb: [Manage controls, Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Create control attestations for an AI asset

Create control attestations for AI assets to document the existence, implementation, and effectiveness of controls that govern behavior, data usage, performance, and risk posture. Attestations serve as formal evidence that the AI asset meets regulatory, ethical, security, and operational standards.

## Before you begin

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst \(AI Risk and Compliance Workspace\), sn\_ai\_asset\_mgmt.ai\_asset\_owner \(AI Control Tower workspace\)

## About this task

Creating a control attestation is the first step in a two-role process. The AI Risk and Compliance Analyst creates the attestation record and assigns it to the AI asset owner. The AI asset owner then performs the attestation to confirm that the control is implemented and operating as intended.

Controls available for attestation are mapped to the AI asset during the assessment phase. Each control represents a governance requirement that must be verified before the AI system can advance to pre-deployment review. If a control is not yet implemented or only partially implemented, the AI asset owner documents the gap during attestation, which may generate an issue requiring remediation.

## Procedure

1.  Navigate to one of the following locations:

    In the AI Risk and Compliance Workspace:

    **All** &gt; **AI Risk and Compliance** &gt; **AI Risk and Compliance Workspace**

    In the AI Control Tower workspace:

    **All** &gt; **AI Control Tower** &gt; **AI Control Tower Workspace**

2.  Select the AI asset for which you need to create control attestations using one of the following options.

<table id="choicetable_ftl_1bl_hjc"><thead><tr><th align="left" id="d365457e144">

Option

</th><th align="left" id="d365457e147">

Description

</th></tr></thead><tbody><tr><td id="d365457e153">

**Create a control attestation using AI Risk and Compliance Workspace**

</td><td>

Select the list icon \[Omitted image "list-icon-airc-ws.png"\] Alt text: and select the AI asset for which you need to create control attestations.

</td></tr><tr><td id="d365457e169">

**Create a control attestation using AI Control Tower**

</td><td>

1.  Navigate to the **AI asset inventory - Managed** list.
2.  Select the **Risk &amp; Compliance** tab.


</td></tr></tbody>
</table>3.  Navigate to **Applies to** &gt; **Controls**.

4.  Select a control from the list.

5.  Select **Attest**.

    When you select one or more controls, the button label updates to show the number of selected controls, for example, **Attest \(2\)**.

    **Note:** Attestations can only be created for controls in the Draft or Monitor state.

6.  Select **Create**.

    The control attestation record is created and assigned to the AI asset owner. The AI asset owner receives a notification with the attestation details and due date.


## Result

The control attestation record is created and assigned to the AI asset owner. The attestation appears in the AI asset owner's task queue. You can monitor attestation status from the **Controls** list on the AI asset record.

## What to do next

After creating the control attestation, next steps vary depending on your role.

AI Risk and Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\]: Your task is complete. The AI asset owner receives the attestation in their task queue. Monitor attestation status from the Controls list on the AI asset record. If an attestation is not completed by the due date, follow up with the AI asset owner or reassign the attestation.

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]: You receive the control attestation in your task queue. Complete each attestation to confirm that the assigned controls are implemented and operating as intended. If a control is not yet implemented, document the gap in your response.

**Parent Topic:**[Manage controls using AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/manage-controls-in-airc.md)

**Related topics**  


[Add controls from control objective](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/add-controls-from-control-objective-airc.md)

[Manage controls using AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/manage-controls-in-airc.md)

