---
title: Set up AI Risk and Compliance properties
description: Configure AI Risk and Compliance properties to specify which authority documents and policies you want to display on the home page. You can also specify a default automated risk classification assessment RAM for AI systems and specify a default RAM to be used for risk assessments of AI systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/configure-airc-properties.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [AIRC properties, authority documents, RAM configuration]
breadcrumb: [AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Set up AI Risk and Compliance properties

Configure AI Risk and Compliance properties to specify which authority documents and policies you want to display on the home page. You can also specify a default automated risk classification assessment RAM for AI systems and specify a default RAM to be used for risk assessments of AI systems.

## Before you begin

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin

## About this task

Use these properties to configure how authority documents and policies are displayed in the compliance overview section of the Risk &amp; Compliance dashboard on the AI Risk and Compliance home page.

You can also specify default Risk Assessment Methodologies \(RAMs\) used for automated risk classification during AI system intake and as the default RAM for AI system risk assessments.

## Procedure

1.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **General Administration** &gt; **Properties**.

2.  Configure the `sn_grc_ai_gov.highlighted_authority_document` property to specify which authority documents you want to display on the home page.

    Enter a maximum of 2 authority document Sys IDs separated by a comma in the **Select authority documents for compliance posture reporting** field.

    Each value represents the Sys ID of an authority document record.

3.  Configure the `sn_grc_ai_gov.ai_system_automated_risk_classification_asmt_ram` property to specify the default Risk Assessment Methodology \(RAM\) used for automated regulatory risk classification of AI systems at intake.

    Enter the RAM Sys ID in the **Default automated risk classification assessment RAM for AI system** field. This RAM is used to automatically classify AI systems during intake based on configured use‑and‑purpose screening questions.

4.  Configure the `sn_grc_ai_gov.highlighted_policy` property to specify which policies you want to display on the home page.

    Enter a maximum of 2 policy Sys IDs separated by a comma in the **Select policies for compliance posture reporting** field.

    Each value represents the Sys ID of a policy record.

5.  Configure the `sn_grc_ai_gov.aisystem_primary_ram` property to specify a default Risk Assessment Methodology \(RAM\) for AI systems.

    Enter the RAM Sys ID in the **Default primary RAM for AI system** field. This RAM is used as the default RAM for all risk assessments.


## Result

After you apply these property settings, the system uses the configured values in the AI Risk and Compliance workspace.

-   AI Risk and Compliance Workspace: The compliance overview section displays the selected authority documents and policies.
-   AI system intake: New AI systems are automatically classified using the specified automated RAM.
-   Risk assessment records: When creating a risk assessment, the default RAM is preselected.

Changes apply to newly created or updated records. Existing records continue to use previously assigned values.

## What to do next

After configuring properties, verify that the AI Risk and Compliance Workspace home page displays the selected authority documents and policies in the compliance overview section. To configure additional workspace settings, see [Configure AI Risk and Compliance Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configure-airc-workspace.md).

**Related topics**  


[Configure AI Risk and Compliance Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configure-airc-workspace.md)

[Risk assessment methodologies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/airc-rams.md)

[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configuring-ai-risk-and-compliance.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configuring-ai-risk-and-compliance.md)

