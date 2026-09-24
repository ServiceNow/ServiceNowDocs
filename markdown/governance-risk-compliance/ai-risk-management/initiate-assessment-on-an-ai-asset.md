---
title: Initiate AI assessment on an AI asset
description: Initiate an AI assessment on an AI asset to send an assessment questionnaire to the assigned user, enabling structured evaluation of the asset against published assessment templates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/initiate-assessment-on-an-ai-asset.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [AI assessment, initiate assessment, AI asset, AI Risk and Compliance, send assessment]
breadcrumb: [Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Initiate AI assessment on an AI asset

Initiate an AI assessment on an AI asset to send an assessment questionnaire to the assigned user, enabling structured evaluation of the asset against published assessment templates.

## Before you begin

Assessment templates must be published before you can initiate an assessment.

Role required: sn\_ai\_asset\_mgmt.ai\_asset\_owner or sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst

## About this task

An AI assessment sends a questionnaire to the user assigned to the AI asset, enabling structured evaluation against a published assessment template. Initiating an assessment is the first step in the impact assessment workflow. After the assigned user completes and submits the questionnaire, the AI Risk and Compliance analyst reviews the responses and closes the assessment, which triggers automatic mapping of risks and controls to the AI asset.

## Procedure

1.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **AI Risk and Compliance Workspace**.

2.  Select the list icon \[Omitted image "list-icon-airc-ws.png"\] Alt text:.

3.  From the list, open the AI asset for which you want to initiate an AI assessment.

4.  Select the more icon \[Omitted image "more-options.png"\] Alt text: and select **Initiate assessment**.

5.  In the Send AI assessment dialog box, fill in the fields.

<table id="table_l35_zwl_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment template

</td><td>

Assessment template used to perform the AI assessment. The list displays all published assessment templates.

</td></tr><tr><td>

Related entity

</td><td>

Entity analyzed for the impact assessment. This field is automatically set to the AI asset's related entity.

</td></tr><tr><td>

Assigned to

</td><td>

User to whom the assessment is assigned. This field is automatically set to the business owner responsible for the AI asset.

</td></tr><tr><td>

Due date

</td><td>

Date by which the assessment must be completed.

</td></tr><tr><td>

Title

</td><td>

Title of the AI assessment.

</td></tr><tr><td>

Description

</td><td>

Description of the AI assessment.

</td></tr></tbody>
</table>6.  Select **Send**.


## Result

The assessment is sent to the assigned user, who receives it in their task queue. The assessment state changes to **Assigned**.

## What to do next

The assigned user completes the impact assessment questionnaire. To complete the assessment, see [Perform impact assessment on an AI use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/perform-impact-assessment-of-ai-use-case.md).

**Parent Topic:**[Using AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/using-ai-risk-and-compliance.md)

**Related topics**  


[Perform impact assessment on an AI use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/perform-impact-assessment-of-ai-use-case.md)

[Assessment templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/airc-assessment-templates.md)

