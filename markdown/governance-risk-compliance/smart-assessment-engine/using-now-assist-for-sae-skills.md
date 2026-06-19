---
title: Using Now Assist for Smart Assessment Engine skills
description: Use the generative AI skills that are supported by the Now Assist for SAE application for quickly drafting the assessment responses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/using-now-assist-for-sae-skills.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [use]
breadcrumb: [Now Assist, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Using Now Assist for Smart Assessment Engine skills

Use the generative AI skills that are supported by the Now Assist for SAE application for quickly drafting the assessment responses.

Now Assist for SAE leverages generative AI to speed up routine SAE tasks. It provides prebuilt skills for tasks like drafting automatic responses for assessment. These skills are activated and configured via the Now Assist Admin console.

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see . \(Note that global domain is not the same as global scope. For more information, see .\)

## Modify the instructions for Now Assist for IRM skills

To modify the prompts for the skills, follow the steps that are mentioned in [KB1806035](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1806035).

