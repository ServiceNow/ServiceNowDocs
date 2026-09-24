---
title: Create an AI issue in the AI Risk and Compliance workspace
description: Identify and manage issues related to the impacted areas for the reported AI case in the AI Risk and Compliance workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/create-ai-issue-in-the-ai-risk-and-compliance-workspace.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [create AI issue, control failure, AI Risk and Compliance workspace]
breadcrumb: [Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Create an AI issue in the AI Risk and Compliance workspace

Identify and manage issues related to the impacted areas for the reported AI case in the AI Risk and Compliance workspace.

## Before you begin

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst or sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager

## About this task

An AI issue represents an identified control failure, compliance gap, or unacceptable risk level associated with an AI asset. Creating an issue enables you to formally track the problem, assign ownership, and drive remediation through a defined workflow. Issues can be created from the AI cases dashboard at any point during the AI asset life cycle and are typically raised when a control attestation reveals a gap, a risk assessment identifies an unacceptable exposure, or an AI case investigation uncovers a compliance concern.

An AI issue transitions through the following states: New, Analyze, Respond, Review, Closed Complete, and Closed Incomplete. For information about the issue management life cycle, see [Manage issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/manage-issues-common-core.md).

## Procedure

1.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **AI Risk and Compliance Workspace**.

2.  On the AI cases dashboard, on the **AI cases** tab, select **Create issue**.

3.  On the form, fill in the fields.

    For a description of the field values on the Create New Issue, see [Create New AI Issue form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/create-new-ai-issue-form.md).

4.  Select **Save**.

    The form is saved and an AI issue is created.


## Result

The created AI issue is assigned to the owner of the control. An AI issue transitions through: New, Analyze, Respond, Review, Closed Complete, or Closed In complete states. A user with the sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst role can work on the AI issue and oversee its closure.

## What to do next

After the AI issue is created, the assigned control owner receives a notification and the issue enters the **New** state. To track remediation progress and close the issue, see [Remediate an issue in AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/remediate-an-issue-in-airc.md). To initiate an assessment on the related AI asset, see [Initiate AI assessment on an AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/initiate-assessment-on-an-ai-asset.md).

-   **[Create New AI Issue form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/create-new-ai-issue-form.md)**  
Use the Create New Issue form to identify and manage issues related to the impacted areas for the reported AI case.

**Parent Topic:**[Using AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/using-ai-risk-and-compliance.md)

**Related topics**  


[Remediate an issue in AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/remediate-an-issue-in-airc.md)

[Create an AI case in the AI Risk and Compliance workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/create-ai-case-in-the-ai-risk-and-compliance-workspace.md)

[AI cases and inquiries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/airc-cases-inquiries.md)

