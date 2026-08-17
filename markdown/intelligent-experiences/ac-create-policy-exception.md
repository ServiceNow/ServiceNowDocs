---
title: Create a policy exception
description: Request an approved, time-bound deviation from a policy or control objective that applies to an AI asset, supported by a justification and a risk assessment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ac-create-policy-exception.html
release: zurich
topic_type: task
last_updated: "2026-07-16"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Policy exceptions, Manage tasks and approvals, Address action items, AI Control Tower, Enable AI experiences]
---

# Create a policy exception

Request an approved, time-bound deviation from a policy or control objective that applies to an AI asset, supported by a justification and a risk assessment.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward or sn\_ai\_asset\_mgmt.ai\_asset\_owner

## About this task

A policy exception documents why an AI asset can't currently meet a control objective and requests approval to operate outside that control for a defined period. The exception routes to an approver, who reviews your justification and risk assessment before approving or rejecting the request.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Activity Center** &gt; **Work** &gt; **Assigned to you**.

2.  Select the **Policy exceptions** sub-tab.

3.  Select **New**.

4.  Fill in the fields that describe the exception.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the policy exception.|
    |Requester|User requesting the exception. Defaults to you.|
    |State|Current state of the exception. Defaults to **New**.|
    |Reason|Reason for requesting the exception.|
    |Priority|Priority of the exception request.|
    |Justification|Justification for requesting the exception.|

    **Note:** The **Substate** field populates automatically as the exception moves through review, such as **Under review** or **Pending risk assessment**, and isn't set when you create the exception.

5.  In the Source section, identify the policy or control the exception applies to.

    |Field|Description|
    |-----|-----------|
    |Source type|Type of source the exception applies to.|
    |Policy|Policy that the exception applies to.|
    |Control objective|Control objective that the exception applies to. When **Source type** is set to **Control objective**, select the control objective first, then select the specific controls from the impacted controls list.|

6.  In the Schedule section, set how long the exception is valid for.

    |Field|Description|
    |-----|-----------|
    |Valid from|Date and time the exception takes effect.|
    |Valid to|Date and time the exception expires.|

    **Note:** The **Duration** field is calculated automatically from the **Valid from** and **Valid to** dates and isn't set directly.

7.  In the Assignment section, specify who should review the exception.

    |Field|Description|
    |-----|-----------|
    |Watch list|Users who want to stay informed about the exception.|
    |Approval group|Group responsible for approving the exception.|
    |Approver|User responsible for approving the exception.|

8.  In the Risk assessment section, document the risk that the exception introduces.

    |Field|Description|
    |-----|-----------|
    |Method|Method used to determine the risk rating.|
    |Risk rating|Risk rating assigned to the exception.|
    |Risk description|Description of the risk associated with the exception.|
    |Analysis of risk and impact|Analysis of the risk and its potential impact.|
    |Risk mitigation plan|Plan for mitigating the risk while the exception is in effect.|

9.  In the Confidentiality section, restrict visibility of the exception if needed.

    |Field|Description|
    |-----|-----------|
    |Confidential|Restricts visibility of the exception to confidential users and members of confidential user groups.|
    |Allowed users|Users who can access the exception if it's marked confidential.|
    |Allowed groups|Groups who can access the exception if it's marked confidential.|

10. In the Comments section, add any supporting notes.

    |Field|Description|
    |-----|-----------|
    |Work notes \(Private\)|Internal notes about the exception that aren't visible to the customer.|
    |Additional comments \(Customer visible\)|Comments about the exception that are visible to the customer.|

11. In the Settings section, specify the functional domain that the exception belongs to.

    |Field|Description|
    |-----|-----------|
    |Functional domain|Functional domain that the exception belongs to, such as **AI Risk and Compliance** or **IT risk and compliance**.|

12. Save the policy exception.


## Result

The policy exception is created and routes to the assigned approver for review. The exception appears in the **Policy exceptions** sub-tab, where you can track its status.

