---
title: Using ServiceNow Otto for Threat Intelligence Security Center \(TISC\) generative AI skills
description: Threat analysts can generate threat intelligence reports and summarize case management content from within their flow of work with ServiceNow Otto for Threat Intelligence Security Center \(TISC\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/using-now-assist-tisc.html
release: australia
topic_type: concept
last_updated: "2026-05-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Otto for Threat Intelligence Security Center \(TISC\), Security Operations]
---

# Using ServiceNow Otto for Threat Intelligence Security Center \(TISC\) generative AI skills

Threat analysts can generate threat intelligence reports and summarize case management content from within their flow of work with ServiceNow Otto for Threat Intelligence Security Center \(TISC\).

## Skills in global domain reuse

By default, all skills exist in the global domain. When you use AI in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, AI only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-pickers.md).\)

**Important:** Some generative AI skills, AI agents, and agentic workflows are turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

With generative AI skills in ServiceNow Otto for Threat Intelligence Security Center \(TISC\), your threat analysts can summarize threat case management content in a concise, easy-to-read format. See [Summarize a Case using generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/now-assist-tisc-case-summarization.md).

Threat analysts can also generate threat intelligence reports directly from case data and export for stakeholder review. See [Generate a Case Report using generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/na-tisc-generate-ai-reports.md).

