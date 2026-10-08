---
title: Renewal insight engine skill in ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)
description: Analyzes the renewal likelihood and expansion potential of an engagement or contract and generates recommended actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/renewal-insight.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Manage engagements, Customer success, Use, Customer Success Management]
---

# Renewal insight engine skill in ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)

Analyzes the renewal likelihood and expansion potential of an engagement or contract and generates recommended actions.

## Before you begin

Role required: `sn_acct_lc.customer_success_agent`

## About this task

The Renewal insight engine skill evaluates individual product metrics, health metrics, health score trends, usage trends, and value scores to generate renewal assessments. The skill provides a granular analysis by evaluating data at the product level rather than using aggregated scores. It's automatically triggered by the Support renewals and expansion workflow \(see [ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) Support renewals and expansion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/now-assist-tmt-renewal-analyzer.md)\) and runs in two modes:

-   **Engagement mode:** analyzes all products and health metrics for the overall engagement and generates renewal likelihood, expansion potential, and up to three recommended actions for the engagement.
-   **Contract mode:** analyzes contract-specific products while also considering overall engagement health and non-contract products, generating the same outputs for the contract.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  Select **Activate** in the Renewal Insight Engine card.

3.  Select the user role that can use this skill and select **Save** to activate the skill.

    The skill is automatically triggered when the Support renewals and expansion agentic workflow runs. When the workflow completes, it generates:

    -   **Renewal likelihood:** an assessment \(Very High, High, Moderate Risk, At Risk, or Critical Risk\) and the key factors that influenced it.
    -   **Expansion potential:** an assessment \(Strong, Moderate, or Limited\), the probability, and target products identified for expansion.
    -   **Recommended actions:** up to three actions as internal or customer plays, each with a target product, priority, and reasoning. The renewal assessment report is automatically added to the work notes of the generated internal play records.

**Parent Topic:**[Manage engagements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-manage-engage.md)

