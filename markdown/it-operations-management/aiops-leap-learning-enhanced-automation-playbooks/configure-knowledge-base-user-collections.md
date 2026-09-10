---
title: Knowledge base permissions for LEAP
description: To use a knowledge base with LEAP, the Can Contribute field must be set to allow users with the knowledge role to submit content. If this is not configured correctly, LEAP cannot route articles to the intended knowledge base.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/configure-knowledge-base-user-collections.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 1
keywords: [knowledge base permissions, Can Contribute, KB routing, knowledge base user collections]
breadcrumb: [Reference, Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# Knowledge base permissions for LEAP

To use a knowledge base with LEAP, the Can Contribute field must be set to allow users with the knowledge role to submit content. If this is not configured correctly, LEAP cannot route articles to the intended knowledge base.

LEAP routes knowledge base articles to the knowledge bases configured in LEAP properties. If the Can Contribute permission is not set correctly on a knowledge base, routing fails and the following error is displayed:

`KB creation failed. Verify that the 'Can Contribute' field in the selected knowledge base is set to 'Users with 'knowledge' role'.`

## Knowledge base permission requirements

|Field|Location|Required value|Impact if not set|
|-----|--------|--------------|-----------------|
|Can Contribute|**Knowledge** &gt; **Administration** &gt; **Knowledge Bases** &gt; **Can Contribute tab** &gt; **Collection**|Users with 'knowledge' role|LEAP cannot route articles to the knowledge base and displays a KB creation error.|

Configure this permission on every knowledge base you plan to use in LEAP, including the default knowledge base and any knowledge bases configured in the **Eligible knowledge bases** field. Once configured, proceed to set up knowledge base routing in LEAP properties. See [LEAP settings fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-settings-fields.md).

