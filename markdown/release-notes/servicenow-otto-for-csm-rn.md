---
title: ServiceNow Otto for CSM
description: The ServiceNow Otto for Customer Service Management \(CSM\) application is an AI-powered suite that brings generative and agentic AI to customer service channels- voice, chat, email, and web. Agents resolve issues faster with intelligent recommendations. Managers optimize team performance. Admins configure and govern AI workflows. ServiceNow Otto for CSM was enhanced and updated in the Brazil release. See the following sections for release notes by version.The Live Agent Assist AI agent is renamed to Live interaction recommendations AI agent. You can now view the live interaction recommendation sources directly in the ServiceNow Otto panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/servicenow-otto-for-csm-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-07"
reading_time_minutes: 4
breadcrumb: [Customer Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# ServiceNow Otto for CSM

The ServiceNow Otto for Customer Service Management \(CSM\) application is an AI-powered suite that brings generative and agentic AI to customer service channels- voice, chat, email, and web. Agents resolve issues faster with intelligent recommendations. Managers optimize team performance. Admins configure and govern AI workflows. ServiceNow Otto for CSM was enhanced and updated in the Brazil release. See the following sections for release notes by version.

## About ServiceNow Otto for CSM

-   Handle cases, accounts, and contacts from email, voice, chat, and social channels on a single screen. ServiceNow Otto for CSM intelligently routes and prioritizes work based on urgency and customer history.
-   Work on multiple cases and tasks within a single browser window. ServiceNow Otto for CSM suggests next best actions, auto-populates case details, and handles routine tasks, letting agents focus on complex customer needs.
-   Quickly access a complete customer 360° view with interaction history, product entitlements, active cases, and AI-generated insights, so agents have everything needed to resolve issues on first contact.

See [ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/now-assist-csm.md) for more information.

## Activation and other requirements

-   **Activation information**

    Customer Service Management is available with activation of the Case Management Core \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/t_ActivateCustomerService.md).

    Gen AI features are available with activation of the ServiceNow Otto for CSM plugin. For more information, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

    Starting with Vancouver Patch 4, ServiceNow Otto for CSM is supported. Beginning Q2 FY26, all CSM Advanced or Prime SKUs already include ServiceNow Otto. Licensing depends on your current base package entitlements within the native AI SKU structure.

    Starting with Zurich Patch 7, Customer Service Management AI agent collection is supported.

    **Important:** The ServiceNow Otto for CSM application is available in ServiceNow Store as ServiceNow Otto for CSM \(sn\_csm\_gen\_ai\).

-   **Upgrade information**

    Before enabling ServiceNow Otto for CSM, verify that your environment and licensing meet the prerequisites, and that all required components are properly installed. Validate that your instance meets version and licensing requirements for each installed feature, and you have the latest versions installed per that release.

-   **Browser requirements**

    Based on current ServiceNow platform standards for workspaces and applications:

    -   **Google Chrome** \(latest public release and two previous versions\)
    -   **Mozilla Firefox** \(latest public release and two previous versions\)
    -   **Microsoft Edge Chromium** \(latest public release and two previous versions\)
    -   **Apple Safari** \(12.0 and later versions on macOS\)
    **Important:** ServiceNow workspaces don't support internet Explorer or legacy Microsoft Edge. If on older releases using these browsers, you must migrate to Edge Chromium before upgrading to recent releases.

-   **Additional requirements**

    Check your entitlements to determine whether you have access to the ServiceNow Otto for Customer Service Management \(CSM\) application.

    For plugins information, navigate to **System Definition** &gt; **Plugins** in your ServiceNow instance. Search for and install the following \(in order where dependencies apply\):

    -   ServiceNow products&gt; Case Management Core
    -   ServiceNow Otto for CSM
    -   AI Search
    -   The following plugins are the dependencies of ServiceNow Otto for Customer Service Management \(CSM\), so auto installed.
        -   Group Action Framework \(for grouping of records and taking smart actions in this data\)
        -   Knowledge Graph for agentic use in semantic indexing
        -   Generative AI Controller
    Validate that the instance meets version and licensing requirements for each installed feature and you have the latest versions installed per that release.


## Accessibility and localization

-   **Accessibility information**

    ServiceNow Otto integrates with ServiceNow's Next Experience accessibility preferences, including keyboard support, dark theme, and focus indicators, creating a more inclusive environment. Voice input and Smart Documents skills are key components that reduce cognitive effort and support multiple input preferences.

-   **Localization information**

    **Language Support:** Officially, support is completely limited to English. While the LLM may summarize content in different languages, quality has not been formally verified for non-English inputs.

    **Regional Availability Considerations:** Not all model providers are available for customers with in-country SKUs, and some AI products/features are currently unavailable for in-country customers. Some AI products/features are currently unavailable for customers in FedRAMP, NSC DOD IL5, Australia IRAP-Protected data centers, self-hosted customers, or other restricted environments. Some AI products and skills aren't available in Regulated Markets.

    For specific regional availability and in-country data handling, consult the ServiceNow support documentation or contact your ServiceNow representative.


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/customer-service-mgmt-rn-landing.md)

## Version 1.0

The Live Agent Assist AI agent is renamed to Live interaction recommendations AI agent. You can now view the live interaction recommendation sources directly in the ServiceNow Otto panel.

### What's changed

-   **[Live Agent Assist AI agent renamed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/live-agent-assist-renamed-entities.md)**

    The Live Agent Assist AI agent is renamed to Live interaction recommendations AI agent. All related references, including skill names, AI Search Profile name, and knowledge graph tags are updated to match the new name.

-   **[In-context recommendation source display in Live interaction recommendations AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-live-agent-assist.md)**

    View recommendation sources directly within the ServiceNow Otto panel without leaving your workspace. The source information follows horizon-aligned presentation patterns, so you can validate a recommendation in place before acting on it.

-   **[Selectable clarification options in Live interaction recommendations AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-live-agent-assist.md)**

    Select a clarification option directly instead of typing a response. When the Live interaction recommendations AI agent presents a multi-question clarification, select an option from a list instead of typing text such as "Option 1" or "Option 2". The underlying AI agent behavior remains unchanged.


### What's deprecated or removed

-   **Now LLM Service deprecation**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


