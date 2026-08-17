---
title: Using ServiceNow Otto for Smart Assessment Engine \(SAE\) skills
description: Use the generative AI skills that are supported by the ServiceNow Otto for SAE application for quickly drafting the assessment responses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/using-servicenow-otto-for-sae-skills.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [use]
breadcrumb: [ServiceNow Otto for SAE, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Using ServiceNow Otto for Smart Assessment Engine \(SAE\) skills

Use the generative AI skills that are supported by the ServiceNow Otto for SAE application for quickly drafting the assessment responses.

## ServiceNow Otto for SAE skills overview

ServiceNow Otto for SAE uses generative AI to speed up routine SAE tasks. It provides prebuilt skills for tasks like drafting automatic responses for assessment. These skills are activated and configured via the AI Admin Hub console.

By default, all skills exist in the global domain. When you use AI in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, AI only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-pickers.md).\)

## Modify the instructions for ServiceNow Otto for SAE skills

To modify the prompts for the skills, follow the steps that are mentioned in [KB1806035](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1806035).

