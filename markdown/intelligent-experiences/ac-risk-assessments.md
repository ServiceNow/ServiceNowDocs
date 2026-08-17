---
title: Risk assessments
description: Complete a risk assessment that AI Control Tower generates automatically for a managed AI asset, evaluating its inherent, control, and residual risk.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ac-risk-assessments.html
release: australia
topic_type: concept
last_updated: "2026-07-17"
reading_time_minutes: 1
keywords: [risk assessment, inherent risk, residual risk]
breadcrumb: [Manage tasks and approvals, Address action items, AI Control Tower, Enable AI experiences]
---

# Risk assessments

Complete a risk assessment that AI Control Tower generates automatically for a managed AI asset, evaluating its inherent, control, and residual risk.

Unlike a case, an issue, or a policy exception, you don't create a risk assessment. AI Control Tower generates a risk assessment automatically and assigns it to the asset's steward or owner to complete. For more information about how risk is assessed across your AI portfolio, see [AI risk posture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-airc-risk-posture.md).

## How risk assessments are generated

AI Control Tower generates a risk assessment when a managed AI asset is onboarded, and again whenever someone edits the asset's use and purpose details, since a change in how an asset is used can change its risk profile. AI Control Tower doesn't surface the specific reason for a re-triggered assessment on the Risk assessments tab itself; that reason appears in the asset's work notes.

To respond, open the risk assessment from Activity Center, or select **New assessment** from the asset's own record. Both paths take you to an assessment response view, where you evaluate the asset's inherent risk, the effectiveness of its controls, and its resulting residual risk. Some assessments also require a target assessment, or a risk response describing whether you plan to accept, avoid, mitigate, or transfer the risk, before you submit the assessment for approval.

## Risk assessment lifecycle

A risk assessment moves from new to in progress as you work through it, to awaiting approval once you submit it for review, and then to completed once an approver signs off. A completed assessment can later be archived, and an assessment can be canceled at any point if it's no longer needed.

## Where risk assessments appear

-   **Activity Center**

    Risk assessments appear on the **Risk assessments** sub-tab of the **Team** and **Assigned to you** tabs, depending on assignment.

-   **The asset record**

    You can start or continue a risk assessment for a specific asset directly from that asset's own record, using the **New assessment** action.


