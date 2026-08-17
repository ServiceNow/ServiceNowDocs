---
title: ServiceNow Otto for Third-party Risk Management \(TPRM\)
description: With the ServiceNow Otto for Third-party Risk Management \(TPRM\) application, you can use skills to automate the collection of TPRM risk data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/exploring-now-assist-tprm.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [TPRM, Issue Summarization, Issue Recommendation, Generative AI, ServiceNow Otto]
breadcrumb: [Explore, Third-party Risk Management, Governance, Risk, and Compliance]
---

# ServiceNow Otto for Third-party Risk Management \(TPRM\)

With the ServiceNow Otto for Third-party Risk Management \(TPRM\) application, you can use skills to automate the collection of TPRM risk data.

## ServiceNow Otto for TPRM overview

The following generative AI capabilities are available in ServiceNow Otto for TPRM:

Learn the details of a third-party risk issue from AI-generated summaries, and use AI-driven recommendations to identify potential third-party risk issues based on assessment responses and historical data.

Starting with Australia Patch 5, Now Assist for Third-party Risk Management is now ServiceNow Otto® for TPRM. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## ServiceNow Otto for TPRM skills

ServiceNow Otto for TPRM includes generative AI capabilities that help you interpret and act on TPRM records more efficiently. These capabilities support tasks such as summarizing TPRM issue details and recommending TPRM issues.

**Note:** The TPRM GenAI User \[sn\_tprm\_genai.nowassist\_user\] role is granted to Third-party Assessment reviewers \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] after you install the ServiceNow Otto for TPRM application. For more information about all TPRM roles, see [Roles in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-roles.md).

<table id="table_p1h_lgx_12c"><thead><tr><th>

Skill

</th><th>

Feature

</th><th>

User role

</th></tr></thead><tbody><tr><td>

[TPRM Issue Summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/create-a-summary-of-issue.md)

</td><td>

Uses generative AI to create a quick summary for the third-party risk issue record helping to support organizational efficiency, team coordination, and productivity.

</td><td>

-   sn\_tprm\_genai.nowassist\_user
-   sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer

</td></tr><tr><td>

[TPRM Issue Recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/create-recommendation-tprm-issue.md)

</td><td>

Uses generative AI to generate third‑party risk issue record recommendations, helping to support more efficient reviews and more consistent outcomes across teams.

</td><td>

-   sn\_tprm\_genai.nowassist\_user
-   sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer

</td></tr></tbody>
</table>**Note:** Issue recommendations are available only for assessments that use the Smart Assessment Engine. Historical data \(prior issues and their associated Smart Assessment Engine or Classic assessment questions and responses\) is used to generate recommendations.

**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some AI products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some AI products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some AI products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## Troubleshoot and get help

-   [ServiceNow Community on AI and Intelligence](https://www.servicenow.com/community/ai-intelligence-articles/tkb-p/ai-platform-kb)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. In addition, this application will collect incident data \(for Incident Assist and Knowledge Assist\) and chat transcripts \(for Chat Assist\). Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

For more information, see the [Now Assist documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).

## What to explore next

To learn more about configuring and using ServiceNow Otto for TPRM, see:

-   [Supporting information for ServiceNow Otto for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/supporting-information-now-assist-tprm.md)
-   [Configure AI capabilities in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/configure-now-assist-for-tprm.md)
-   [Activate the TPRM issue summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-summarize-an-issue.md)
-   [Activate TPRM issue recommendation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-recommend-an-issue.md)
-   [TPRM issue summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/issue-summarization-tprm.md)
-   [TPRM issue recommendation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/issue-recommendation-tprm.md)
-   [Generate a summary of a TPRM issue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/create-a-summary-of-issue.md)
-   [Generate issue recommendations for TPRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/create-recommendation-tprm-issue.md)
-   [Create or dismiss issues using recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/manage-recommendation-issue.md)

