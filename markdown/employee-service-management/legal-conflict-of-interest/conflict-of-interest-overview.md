---
title: Exploring Legal Conflict of Interest
description: Learn more about the Legal Conflict of Interest application through a sample workflow and review the benefits that it can provide.
locale: en-US
release: zurich
product: Legal Conflict of Interest
classification: legal-conflict-of-interest
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
keywords: [Conflict of interest, Conversational intake for COI, COI employee center, legal requests]
breadcrumb: [Legal Conflict of Interest, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Exploring Legal Conflict of Interest

Learn more about the Legal Conflict of Interest application through a sample workflow and review the benefits that it can provide.

## Legal Conflict of Interest overview

The ServiceNow® Legal Conflict of Interest enables you to manage the disclosure, approval, and registry of conflict of interest that might arise from employees having competing interests or loyalties. Employees can submit disclosures using the conversational interface of Now Assist in Virtual Agent or intake form available in the Employee Center. The Requests are evaluated against predefined risk factors to calculate an overall risk score. Based on this score, requests are routed to the appropriate approval workflow for faster resolution.

**Note:** The conversational intake functionality is available only when you have installed and configured Now Assist for Legal Service Delivery \(LSD\) that is a paid application. For more information, see [Now Assist for Legal Service Delivery \(LSD\)](../../legal-request-management/concept/now-assist-lsd-landing.md).

For more information on how to submit the requests using the two methods, see [Submit COI request form Employee Center](../task/submit-coi-disclosure-request.md) and [Submit COI request using Now Assist conversational intake](../../legal-request-management/task/now-assist-lsd-convi.md)

## Risk assessment

When an employee submits a COI disclosure—either through the Employee Center intake form or via Now Assist in Virtual Agent conversational intake—the risk assessment utility evaluates the submission against a set of predefined risk factors. Each risk factor contributes to an overall risk score, which determines the risk level \(Low, Medium, or High\) and the corresponding approval routing.

The risk level determines whether the request needs approval or can be auto-approved.

-   Low risk — The request is auto-approved, and both the employee and their manager receive notification. No approvers are engaged.
-   Medium risk — The approval chain is triggered. The request is routed to the first-level approvers as determined by the conflict type \(for example, Manager and Legal Compliance for an Outside Employment disclosure\).
-   High risk — The full approval chain is triggered, including escalated approvers. The request is routed through all approvers defined for the conflict type \(for example, Manager, Legal Compliance, and Board Approval for a Board Service fiduciary role\).

Risk factors support three evaluation types that determine how each condition is assessed:

-   Condition: Evaluates the disclosure against rule-based field-value conditions. Use this type for deterministic, field-based evaluations.
-   Skill: Uses an AI skill to analyze the disclosure content and return a risk score. This evaluation type is available only when you have installed and configured Now Assist for Legal Service Delivery \(LSD\), which is a paid application.
-   Subflow: Executes a Flow Designer subflow for complex logic, external integrations, or multi-step processing.

The risk assessment process generates a report that provides legal fulfillers visibility into the evaluation. The report includes request details, risk level and score, detailed risk factor analysis with reasoning, and all submitted request variables. Legal fulfillers can review the report from the Risk Assessment tab of the legal request to take quicker decisions.

A notification is sent to the requesters before the expiry of the validity of their COI disclosure records. If the requesters need an extension, they should review and resubmit a request to get the legal clearance for the extended period.

For more information, see [Configure risk assessment](../task/lsd-coi-config-risk-fac.md).

## Approval workflow

The approvers and the number of approval levels differ based on the conflict type.

Following illustration shows the approvers and number of approval levels for each conflict type. For example, the Outside Employment conflict type has two approval levels. The first-level approver is the manager of the requester, and the second-level approver is the legal compliance group.

![Conflict of Interest approval flow for different conflict types.](../image/lsd-approval-workflow.png "Conflict of Interest approval flow")

The administrator can modify the approval flow in the following ways:

-   Change the number of levels of approval required.
-   Add or modify approvers or approver groups at each level of approval.

For more information, see [Configure flows for Legal Conflict of Interest](../task/configure-coi-flow-designer-flows.md).

## Legal Conflict of Interest users

|User|Description|
|----|-----------|
|Legal conflict of interest Admin|Configures intake forms and approval workflows.|
|Legal conflict of interest fulfiller|Works on fulfilling the COI requests.|
|Legal conflict of interest read|Has read-only access to view all COI disclosure records.|

## Legal Conflict of Interest workflow

1.  The legal user submits a new conflict of interest disclosure request by selecting the appropriate conflict type.
2.  The risk assessment evaluates the request and assigns a risk level \(Low, Medium, or High\) based on the calculated risk score.
3.  The conflict of interest disclosure request enters a predefined approval workflow depending on the risk level.
4.  The conflict of interest fulfiller reviews the risk assessment report.
5.  The conflict of interest fulfiller either approves or rejects the submitted request.
6.  The final decision is communicated to the employee via email notification.
7.  A corresponding record is automatically generated in the system.

## Legal Conflict of Interest benefits

<table id="table_bbk_vxm_nfc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Submit COI request using natural language from the conversational interface of Now Assist in Virtual Agent.This is available only when you have installed and configured Now Assist for Legal Service Delivery \(LSD\) that is a paid application.

</td><td>

[Submit COI request using Now Assist conversational intake](../../legal-request-management/task/now-assist-lsd-convi.md)

</td><td>

Legal user

</td></tr><tr><td>

Submit COI request from the Employee Center

</td><td>

[Submit COI request form Employee Center](../task/submit-coi-disclosure-request.md)

</td><td>

Legal user

</td></tr><tr><td>

Risk assessment with configurable risk factors and score to automate approval workflow

</td><td>

[Configure risk assessment](../task/lsd-coi-config-risk-fac.md)

</td><td>

Legal fulfiller

</td></tr><tr><td>

Risk assessment reports with detailed scoring and analysis enable legal fulfillers to make faster, informed approval decisions.

</td><td>

[View risk assessment details](../task/lsd-coi-view-risk-asmt-dets.md)

</td><td>

Legal fulfiller

</td></tr><tr><td>

Configurable approval flows in accordance with the organization's Conflict of Interest \(COI\) policy.

</td><td>

[Configure flows for Legal Conflict of Interest](../task/configure-coi-flow-designer-flows.md)

</td><td>

Legal administrator

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using Legal Conflict of Interest, see:

-   [Configure Legal Conflict of Interest](legal-coi-administration.md)
-   [Using Legal Conflict of Interest](lsd-coi-use-landing.md)
-   [Legal Conflict of Interest reference](../reference/legal-coi-reference.md)

