---
title: Application readiness for Now Assist on the ServiceNow AI Platform
description: Now Assist leverages the power of the ServiceNow AI Platform to deliver AI solutions. Ensure that your instance is ready to take advantage of AI capabilities by preparing Platform applications, such as Service Catalog and AI Search.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, agentic AI, AI readiness]
breadcrumb: [ServiceNow AI implementation, Enable AI experiences]
---

# Application readiness for Now Assist on the ServiceNow AI Platform

Now Assist leverages the power of the ServiceNow AI Platform to deliver AI solutions. Ensure that your instance is ready to take advantage of AI capabilities by preparing Platform applications, such as Service Catalog and AI Search.

Installing a Now Assist product such as Now Assist for IT Service Management \(ITSM\) gives you access to AI capabilities in Platform applications as well as capabilities specific to your product workflow. It's important to ensure that the appropriate Platform applications are ready for Now Assist. To prepare your instance for Now Assist, review the following topics:

-   [Knowledge Base readiness for Now Assist on the ServiceNow AI Platform](sn-ai-impl-kb-readiness.md)
-   [Service Catalog readiness for Now Assist on the ServiceNow AI Platform](sn-ai-impl-srvc-catalog.md)
-   [AI Search readiness for Now Assist on the ServiceNow AI Platform](sn-ai-impl-ai-search.md)
-   [Now Assist in Virtual Agent readiness on the ServiceNow AI Platform](sn-ai-impl-nava.md)

After ensuring that your AI policy, your data, and your applications are ready, you can begin to implement Now Assist.

1.  Ensure entitlement for at least one Now Assist application. For a list of available applications, see [Exploring Now Assist Admin](../../now-assist-platform/concept/exploring-now-assist-platform.md).

    **Note:** Some Now Assist products may require other entitlements.

2.  In the ServiceNow Store, check version compatibilities and dependencies for Now Assist apps.

    For more information, see [Evaluating version requirements and dependencies](https://www.servicenow.com/docs/access?context=versions-dependencies&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

3.  Install Now Assist products from the Now Assist Admin console.

    For more information, see [Install Now Assist plugins](../../now-assist-admin/task/install-now-assist-feature-plugins.md).


## Customization and Now Assist

Customizing your ServiceNow instance is often necessary to meet unique business needs, but it can introduce unintended consequences for Now Assist features. Changes to field names, UI actions, workflows, or table structures may disrupt how Now Assist skills and agents operate. For example, modifying field states or labels can interfere with skill conditions and input mapping, while altering default UI actions may prevent agents from triggering correctly. Custom resolution workflows might conflict with the logic embedded in native skills, and table-level variations can affect where and how Now Assist functions across workflows. These customizations can also create upgrade friction, requiring additional testing, rework, or reconfiguration to ensure compatibility with new platform releases.

To mitigate these risks, you can use tools like the Now Assist Readiness Evaluation app to identify high-impact customizations and plan for remediation before deploying or upgrading AI features. For more information, see [Now Assist Readiness Evaluation](../../now-assist-readiness-evaluation/concept/now-assist-readiness-evaluation-landing-page.md).

To maintain compatibility with Now Assist while accommodating custom configurations, several mitigation strategies are available:

-   Duplicate skills before adapting them.
-   Adjust skill inputs and role conditions to reflect organizational processes.
-   Add additional input sources, such as related tables or emails.

For more advanced needs, build custom generative AI skills tailored to your unique business requirements, allowing for deeper integration without compromising core functionality.

For more information about customizing AI solutions, see [How to approach building custom generative AI solutions using Now Assist](https://www.servicenow.com/community/now-assist-articles/how-to-approach-building-custom-generative-ai-solutions-using/ta-p/3006669) in the ServiceNow Community.

