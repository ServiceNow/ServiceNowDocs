---
title: Configure ServiceNow Otto for Smart Assessment Engine \(SAE\)
description: Configure ServiceNow Otto for SAE to enable generative AI skills for the assessment response assist workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/configure-servicenow-otto-for-smart-assessment-engine.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [configure]
breadcrumb: [ServiceNow Otto for SAE, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Configure ServiceNow Otto for Smart Assessment Engine \(SAE\)

Configure ServiceNow Otto for SAE to enable generative AI skills for the assessment response assist workflow.

## ServiceNow Otto for SAE Configuration overview

Use the AI Admin Hub console to configure ServiceNow Otto for SAE. This console contains everything that you must install plugins and configure the generative AI skills. For additional information, see [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).

You can access the **Smart Assessment Response Assist** skill from the AI Admin Hub console.

**Note:** Now LLM Service is the sole provider for this ServiceNow Otto® application's skills.

For earlier versions, go to [Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager.md) to upgrade it to a later version.

For information about configuring generative AI skills and prompts, see [Configuring AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-na-landing.md).

After you turn on the Smart Assessment Response Assist skill, you must also enable AI responses on each template category that you want the skill to run on. To enable AI responses for a category and to configure the documents that the skill considers by default, see [Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md).

By default, the skill draws on:

-   Previously completed smart assessments and classic assessments that share the same scope item as the current assessment.
-   Documents that are attached directly to the assessment instance.

To customize these defaults for a template category, implement the Smart Assessment Response Assist scripted extension point. For details, see [Customizing AI Response Assist sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/customizing-ai-response-assist-sources.md).

## Using guided setup to implement ServiceNow Otto for SAE

You can install the ServiceNow Otto for SAE plugin \(com.sn\_smart\_ai\_assist\). This store app has the following dependencies:

-   ServiceNow AI Platform
-   Governance, Risk, and Compliance

For information about the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

**Note:** For more information on Retrieval Augmented Generation \(RAG\) and Retention policies, see [Indexed sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/indexed-sources-ais.md) and [User data usage policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/user-data-usage-policy-now-assist.md).

