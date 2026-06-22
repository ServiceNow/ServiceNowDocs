---
title: Configure Now Assist for Smart Assessment Engine
description: If you have the admin role, you can configure Now Assist for SAE so that your agents can use the generative AI skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/configure-now-assist-for-smart-assessment-engine.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [configure]
breadcrumb: [Now Assist, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Configure Now Assist for Smart Assessment Engine

If you have the admin role, you can configure Now Assist for SAE so that your agents can use the generative AI skills.

## Now Assist for SAE Configuration overview

Use the Now Assist Admin console to configure Now Assist for SAE. This console contains everything that you must install plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/configuring-now-assist.md).

You can access the **Smart Assessment Response Assist** skill from the Now Assist Admin console.

**Note:** Now LLM Service is the sole provider for this Now Assist application's skills.

For earlier versions, go to [Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/application-manager.md) to upgrade it to a later version.

For information about configuring generative AI skills and prompts, see [Configuring Now Assist Admin features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/configuring-na-landing.md).

After you turn on the Smart Assessment Response Assist skill, you must also enable AI responses on each template category that you want the skill to run on. To enable AI responses for a category and to configure the documents that the skill considers by default, see [Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md).

By default, the skill draws on:

-   Previously completed smart assessments and classic assessments that share the same scope item as the current assessment.
-   Documents that are attached directly to the assessment instance.

To customize these defaults for a template category, implement the Smart Assessment Response Assist scripted extension point. For details, see [Customizing AI Response Assist sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/customizing-ai-response-assist-sources.md).

## Using guided setup to implement Now Assist for SAE

You can install the Now Assist for SAE plugin \(com.sn\_smart\_ai\_assist\). This store app has the following dependencies:

-   Now Assist Platform
-   Governance, Risk, and Compliance

For information about the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/install-now-assist-feature-plugins.md).

**Note:** For more information on Retrieval Augmented Generation \(RAG\) and Retention policies, see [Indexed sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/indexed-sources-ais.md) and [User data usage policy for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/user-data-usage-policy-now-assist.md).

