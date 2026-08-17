---
title: oneExtend LLM skill
description: ServiceNow Otto for Workflow Data Fabric \(WDF\) includes the oneExtend LLM skill that guides you through integration setup.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/recommendation-skill.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Workflow Data Fabric Home, Workflow Data Fabric]
---

# oneExtend LLM skill

ServiceNow Otto for Workflow Data Fabric \(WDF\) includes the oneExtend LLM skill that guides you through integration setup.

**Important:** Some generative AI skills, AI agents, and agentic workflows are turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

The oneExtend LLM skill is included with the ServiceNow Otto for WDF experience. Follow the instructions in [Configure ServiceNow Otto for Workflow Data Fabric \(WDF\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-now-assist-for-workflow-data-fabric.md) to install the plugin.

By default, all skills exist in the global domain. When you use AI in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, AI only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-pickers.md).\)

**Parent Topic:**[Workflow Data Fabric Home Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric-reference.md)

**Related topics**  


[Ask ServiceNow Otto for Workflow Data Fabric \(WDF\) for recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/ask-now-assist-for-recommendation.md)

