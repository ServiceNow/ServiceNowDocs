---
title: Set up AI Risk and Compliance properties
description: Configure AI Risk and Compliance properties to specify which authority documents and policies you want to display on the home page. You can also specify a default RAM to be used for risk assessments of AI systems.
locale: en-US
release: yokohama
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Configure, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Set up AI Risk and Compliance properties

Configure AI Risk and Compliance properties to specify which authority documents and policies you want to display on the home page. You can also specify a default RAM to be used for risk assessments of AI systems.

## Before you begin

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin

## About this task

The authority documents and polices that you configure are used in the compliance overview section of the Risk &amp; compliance dashboard on the AI Risk and Compliance home page.

## Procedure

1.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **AI Risk and Compliance Workspace** &gt; **Administration** &gt; **Properties**.

2.  Configure the `sn_grc_ai_gov.highlighted_authority_document` property to specify which authority documents you want to display on the home page.

    Enter a maximum of 2 authority documents separated by comma in the **Select authority documents for compliance posture reporting** field.

3.  Configure the `sn_grc_ai_gov.highlighted_policy` property to specify which policies you want to display on the home page.

    Enter a maximum of 2 policies separated by comma in the **Select policies for compliance posture reporting** field.

4.  Configure the `sn_grc_ai_gov.aisystem_primary_ram` property to specify a default Risk Assessment Methodology \(RAM\) for AI systems.

    Enter the RAM in the **Default primary RAM for AI system** field.This RAM will be used as the default RAM for all risk assessments.


