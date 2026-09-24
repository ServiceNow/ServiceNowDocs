---
title: Initiate risk assessment on AI asset
description: Initiate risk assessment to enable the risk assessor to perform risk assessments on AI systems, evaluating the likelihood and impact of potential risks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/initiate-risk-assessment-on-ai-systems.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [initiate risk assessment, risk assessor, AI asset risk]
breadcrumb: [Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Initiate risk assessment on AI asset

Initiate risk assessment to enable the risk assessor to perform risk assessments on AI systems, evaluating the likelihood and impact of potential risks.

## Before you begin

Role required: sn\_ai\_asset\_mgmt.ai\_asset\_owner or sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst

## About this task

A risk assessment evaluates the likelihood and impact of individual risks mapped to an AI asset. It is initiated after an impact assessment has been completed and risk statements have been attached to the AI system. Use this task to assign an assessor and send the risk assessment, which puts it into the assessor's task queue. For information about how risks are mapped to an AI system through the impact assessment, see [Risk assessment methodologies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/airc-rams.md).

To assess risks across multiple AI assets simultaneously using a project-based workflow, see [Create bulk risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/create-bulk-risk-assessment-airc.md).

## Procedure

1.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **AI Risk and Compliance Workspace**.

2.  Select the list icon\[Omitted image "list-icon-airc-ws.png"\] Alt text: .

3.  From the List, open the AI asset for which you want to initiate risk assessments.

4.  Navigate to **Assessments** &gt; **Risk assessments**.

5.  Select **Assess risk**.

6.  On the Specify assessor and approver dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Related entity|Entity that needs to be assessed. This field is automatically set to the AI system's related entity.|
    |Risk assessment methodology|Risk assessment methodology \(RAM\) that you use to assess risks.|
    |Risk assessor|Person who is responsible for assessing the risk.|
    |Approver|Person who is responsible for approving the assessment.|

7.  Select **Send assessment**.


## Result

The risk assessment is sent to the assigned assessor and appears in their task queue. The risk assessment state changes to **Assigned**.

## What to do next

After the assessment is sent, the assigned assessor receives the risk assessment in their task queue. To complete the assessment, see [Perform risk assessments on AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/perform-risk-assessments-on-ai-systems.md).

**Parent Topic:**[Using AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/using-ai-risk-and-compliance.md)

**Related topics**  


[Perform risk assessments on AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/perform-risk-assessments-on-ai-systems.md)

[Initiate risk assessment on AI asset's risks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/request-risk-assessments-for-ai-systems.md)

[Risk assessment methodologies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/airc-rams.md)

