---
title: Using Now Assist for Integrated Risk Management \(IRM\) skills
description: Use the generative AI skills that are supported by the Now Assist for Integrated Risk Management \(IRM\) application for quick actions with issues.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Using Now Assist for Integrated Risk Management \(IRM\) skills

Use the generative AI skills that are supported by the Now Assist for Integrated Risk Management \(IRM\) application for quick actions with issues.

Now Assist for IRM leverages generative AI to streamline risk and compliance processes. It provides pre-built skills and supports custom skill development for tasks like summarization, recommendations, and rationalization.

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

These skills are configured via the Now Assist Admin console.

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=domain-separation-in-the-now-assist-admin-console&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://www.servicenow.com/docs/access?context=next-experience-pickers&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).\)

For more information on language support, see [Multilingual service for Now Assist](https://www.servicenow.com/docs/access?context=translation-for-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and [Multilingual support for ServiceNow generative AI products](https://www.servicenow.com/community/now-assist-articles/multilingual-support-for-servicenow-generative-ai-products/ta-p/3099258).

## Modify the instructions for Now Assist for IRM skills

Starting with the Zurich patch 3 release, users who have Now Assist for IRM installed can use the skills powered by Now Assist for IRM.

To modify the prompts for the skills, follow the steps that are mentioned in [KB1806035](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1806035).

