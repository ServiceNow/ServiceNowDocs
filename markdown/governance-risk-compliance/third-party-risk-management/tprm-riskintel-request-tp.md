---
title: Request a risk intelligence report
description: Request a risk intelligence report \(RIR\) or score to gain insight on how trustworthy a particular third party can be using the Third-party Risk Management application.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use risk intelligence reports and scores, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Request a risk intelligence report

Request a risk intelligence report \(RIR\) or score to gain insight on how trustworthy a particular third party can be using the Third-party Risk Management application.

## Before you begin

You must set up and register all risk intelligence providers and set up request types so that they’re available as selections in the risk intelligence report form. For more information, see [Register a risk intelligence provider](tprm-riskintelprvdr-register.md), [Set up a risk intelligence provider service](tprm-riskintelprvdr-set-up.md), and [Set up a request type for a provider](tprm-riskintelprvdr-request-type.md).

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

## About this task

You can order different types of risk intelligence reports such as credit risk reports, compliance reports, strategic risk reports, and more for your specific risk management program requirements.

**Note:** There can only be one active request of each type for a third party. For example, if Workfaster has already requested a Level 1 report, they can’t request another Level 1 report while the first one is still being processed.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Third-party Risk Management** &gt; **Risk Intelligence Provider Setup** &gt; **Report Requests**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For descriptions of all these fields, see [Risk intelligence report request form](../../grc-workspace-vrm/reference/tprm-rir-form.md). To create a risk intelligence report request that is associated with a due diligence request, see [Request a risk intelligence report associated with a due diligence request](tprm-riskintel-request-dd.md).

4.  In the Sanction section of the form, enter any sanctions-related information.

    For information on how to track sanctions screening information, see [Track sanctions-related information](tprm-riskintel-track-sanctions.md).

5.  Select **Save**.

    The system opens to the third-party risk RIR request. For each risk intelligence request, the system auto-assigns a unique ID number that starts with the text RIR. Use this ID to track your request. You can add attachments and start a discussion with your team from this page.

6.  Select **Submit request**.

    The RIR request has been submitted to the provider.

    **Note:** You can create a risk intelligence request through the third-party record page with the following actions.

    1.  In Vendor Management Workspace, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **All third parties**.
    2.  Select the relevant third party to get to the third-party record page.
    3.  On the **Risk Intelligence report request** tab, select **New** and specify the **Provider** and **Request type**.
    4.  Select **Save**.
    5.  Select **Submit request**.

        You have submitted the RIR request to the provider.


