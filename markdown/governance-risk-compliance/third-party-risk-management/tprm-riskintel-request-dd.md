---
title: Request a risk intelligence report associated with a due diligence request
description: Request a risk intelligence report \(RIR\) or score to gain insight on how trustworthy a particular third party can be as part of the due diligence request process by using the Third-party Risk Management application. By associating your RIR request with a due diligence request, all activity, scores, reports, and details are available for you to see.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use risk intelligence reports and scores, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Request a risk intelligence report associated with a due diligence request

Request a risk intelligence report \(RIR\) or score to gain insight on how trustworthy a particular third party can be as part of the due diligence request process by using the Third-party Risk Management application. By associating your RIR request with a due diligence request, all activity, scores, reports, and details are available for you to see.

## Before you begin

You must set up and register all risk intelligence providers and set up request types so that they’re available as selections in the Risk intelligence report request form. For more information, see [Register a risk intelligence provider](tprm-riskintelprvdr-register.md), [Set up a risk intelligence provider service](tprm-riskintelprvdr-set-up.md), and [Set up a request type for a provider](tprm-riskintelprvdr-request-type.md).

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor that is the due diligence request owner, sn\_vdr\_risk\_asmt.vendor\_risk\_manager, or sn\_vdr\_risk\_asmt.contract\_negotiator assigned to the due diligence request.

## About this task

You can order different types of risk intelligence reports such as credit risk reports, compliance reports, strategic risk reports, and more for your specific risk management program requirements.

**Note:** There can only be one active request of each type for a third party. For example, if Workfaster has already requested a Level 1 report, they can’t request another Level 1 report while the first one is still being processed.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**.

2.  Select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Due diligence requests** &gt; **All requests**.

3.  Navigate to the Due diligence request record page by selecting the relevant **DDR** number.

4.  On the **Risk Intelligence report request** tab, select **New** and specify the **Provider** and **Request type**.

    For descriptions of all these fields, see [Risk intelligence report request form](../../grc-workspace-vrm/reference/tprm-rir-form.md).

5.  In the Sanction section of the form, enter any sanction-related information.

    For information on how to track sanctions screening information, see [Track sanctions-related information](tprm-riskintel-track-sanctions.md).

6.  Select **Save**.

    The system opens to the Third-party risk intelligence request. For each risk intelligence request, the system auto-assigns a unique ID number that starts with the text RIR. Use this ID to track your request. You can add attachments and start a discussion with your team from this page.

7.  Select **Submit request**.

    You have submitted the RIR request to the provider.


