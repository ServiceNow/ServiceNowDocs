---
title: Data Privacy for Now Assist
description: Set up and configure how to discover and anonymize sensitive data from generative AI prompts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/now-assist-for-data-privacy-landing.html
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Privacy, Platform Privacy]
---

# Data Privacy for Now Assist

Set up and configure how to discover and anonymize sensitive data from generative AI prompts.

## Get started

<table id="table_tpg_p4l_ydc" class="nav-card presentation"><tbody><tr><td>

[Explore\[Omitted image "bus-explore.svg"\] Alt text:Learn more about Data Privacy for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-privacy-classic/explore-now-assist-data-privacy.md)

</td><td>

[Configure\[Omitted image "bus-sdlc.svg"\] Alt text:Configure Data Privacy for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-privacy-classic/configure-now-assist-data-privacy.md)

</td></tr></tbody>
</table>**Note:**

Data Privacy for Now Assist detects and masks sensitive data based on Regex and Named Entity Recognition \(NER\) data patterns. Enabling NER data patterns requires customers to have a Vault license as well as an additional $0 SKU associated with the Vault license. Also, customers must have the latest version of the GenAI Controller \(`sn.generative.ai`\) installed on their instance \(which requires the admin role\).

There are associated rate limits on how much data can be processed when using Named Entity Recognition \(NER\) data patterns for Now Assist. Once these limits are exceeded, any applicable Regex based data masking that was configured will apply for all Now Assist prompts, skills, and agentic executions.

**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some Now Assist products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some Now Assist products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some Now Assist products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

