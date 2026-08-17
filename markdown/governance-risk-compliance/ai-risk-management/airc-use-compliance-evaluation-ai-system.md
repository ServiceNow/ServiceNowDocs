---
title: Use a compliance evaluation on an AI system record
description: Map a control objective to an AI system, run its compliance evaluation, and review evaluation results, supporting data, and automatically created issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/airc-use-compliance-evaluation-ai-system.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-07-26"
reading_time_minutes: 1
breadcrumb: [Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Use a compliance evaluation on an AI system record

Map a control objective to an AI system, run its compliance evaluation, and review evaluation results, supporting data, and automatically created issues.

## Before you begin

A compliance evaluation configuration must exist for the control objective you want to monitor. For more information on configuring an evaluation configuration, see [Create a compliance evaluation configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/airc-compliance-evaluation-configuration.md).

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager

## Procedure

1.  Open the target AI system record and map the control objective to it.

    Mapping the control objective to the AI system creates a control and a linked compliance evaluation record on that AI system, for example, Compliance evaluation: AI toxicity evaluation.

2.  On the compliance evaluation record, select **Execute** to run the evaluation on demand, or wait for it to run at the configured frequency.

3.  Select **Evaluation results** to review the outcome of the evaluation.

4.  Select **View supporting data** to see the trace, session, or span record that caused a failure.

    Supporting data gives the auditor or risk manager visibility into why a control was considered compliant or non-compliant. Selecting a record opens the related session, trace, or span record from the evaluation framework.

5.  If the evaluation fails, open the AI system record and select **Issues** to review the issue that was automatically created.

    The issue links to the control and the evaluation results. The AI system compliance score decreases while the control remains non-compliant, and increases again after the control becomes compliant.


## What to do next

The compliance evaluation now runs automatically at the configured frequency, continuously monitoring the AI system and raising or resolving issues as its controls become non-compliant or compliant.

**Parent Topic:**[Using AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/using-ai-risk-and-compliance.md)

