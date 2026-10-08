---
title: Application readiness for AI on the ServiceNow AI Platform
description: ServiceNow Otto uses the ServiceNow AI Platform to deliver AI solutions. Ensure that your instance is ready to use AI capabilities by preparing Platform applications, such as Service Catalog and AI Search.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sn-ai-impl-app-readiness.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Now Assist, agentic AI, AI readiness]
breadcrumb: [Assessing your AI readiness, Getting started with AI, Enable AI Experiences]
---

# Application readiness for AI on the ServiceNow AI Platform

ServiceNow Otto uses the ServiceNow AI Platform to deliver AI solutions. Ensure that your instance is ready to use AI capabilities by preparing Platform applications, such as Service Catalog and AI Search.

Installing a product such as ServiceNow Otto for IT Service Management \(ITSM\) gives you access to AI capabilities in Platform applications and capabilities specific to your product workflow. Ensure that the appropriate Platform applications are ready for AI. To prepare your instance, review the following topics:

-   [Knowledge Base readiness for AI on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/sn-ai-impl-kb-readiness.md)
-   [Service Catalog readiness for AI on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/sn-ai-impl-srvc-catalog.md)
-   [AI Search readiness for AI on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/sn-ai-impl-ai-search.md)
-   [ServiceNow Otto for Virtual Agent readiness on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/sn-ai-impl-nava.md)

After ensuring that your AI policy, your data, and your applications are ready, you can implement AI.

1.  Ensure entitlement for at least one ServiceNow Otto application. For a list of available applications, see [Exploring AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/exploring-now-assist-platform.md).

    **Note:** Some ServiceNow Otto products may require other entitlements.

2.  In the ServiceNow Store, check version compatibilities and dependencies for ServiceNow Otto apps.

    For more information, see [Evaluating version requirements and dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/versions-dependencies.md).

3.  Install ServiceNow Otto products from the AI Admin Hub console.

    For more information, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).


## Customization and AI

Customizing your ServiceNow instance is often necessary to meet unique business needs, but it can introduce unintended consequences for AI features. Changes to field names, UI actions, workflows, or table structures may disrupt how generative AI skills and agents operate. For example, modifying field states or labels can interfere with skill conditions and input mapping, while altering default UI actions may prevent agents from triggering correctly. Custom resolution workflows might conflict with the logic embedded in native skills, and table-level variations can affect where and how ServiceNow Otto functions across workflows. These customizations can also create upgrade friction, requiring additional testing, rework, or reconfiguration to confirm compatibility with new platform releases.

To mitigate these risks, you can use tools like the AI Readiness Evaluation app to identify high-impact customizations and plan for remediation before deploying or upgrading AI features. For more information, see [AI Readiness Evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-readiness-evaluation/now-assist-readiness-evaluation-landing-page.md).

To maintain compatibility with ServiceNow Otto while accommodating custom configurations, several mitigation strategies are available:

-   Duplicate skills before adapting them.
-   Adjust skill inputs and role conditions to reflect organizational processes.
-   Add input sources, such as related tables or emails.

For more advanced needs, build custom generative AI skills tailored to your unique business requirements, enabling deeper integration without compromising core functionality.

For more information about customizing AI solutions, see [How to approach building custom generative AI solutions using Now Assist](https://www.servicenow.com/community/now-assist-articles/how-to-approach-building-custom-generative-ai-solutions-using/ta-p/3006669) in the ServiceNow Community.

