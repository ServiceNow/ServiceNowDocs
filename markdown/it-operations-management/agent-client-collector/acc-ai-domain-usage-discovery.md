---
title: Domain usage discovery and categorization
description: Agent Client Collector for Visibility \(ACC-VC\) domain usage discovery classifies the domains that users visit against a set of admin-defined domain signatures. It enables you to see which websites and services, such as AI tools, are being used across the endpoints in your environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/agent-client-collector/acc-ai-domain-usage-discovery.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [AI domain usage discovery, shadow AI, Agent Client Collector for Visibility Content]
breadcrumb: [ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Domain usage discovery and categorization

Agent Client Collector for Visibility \(ACC-VC\) domain usage discovery classifies the domains that users visit against a set of admin-defined domain signatures. It enables you to see which websites and services, such as AI tools, are being used across the endpoints in your environment.

## Domain usage discovery overview

Domain usage discovery matches the domains that users visit against a set of domain-type signatures, and records a match for each combination of endpoint, domain, and user. You can create categories of any type, such as AI Tools, Productivity, or Security, and map them to the domain URLs in your signatures. Use the resulting data to see which categories of website and services are accessed from your browsers and devices.

**Note:** This capability reuses the existing web usage collection pipeline. No new agent-side data collection module is required.

## Prerequisites

Domain usage discovery depends on the Agent Client Collector for Visibility \(ACC-VC\) VISC Get URL metrics policy. This policy ships turned off, so you must activate it before AI domain usage discovery can classify any domains. For more information, see [Agent Client Collector for Visibility Content default checks and policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-visibility-checks-policies.md).

## Domain signatures

Domain usage discovery relies on how you categorize domains. The system doesn't categorize domains automatically. To identify usage of a website or application, create a domain signature for it and assign the category that you want. Visited domains that match the signature are then reported under that category. For example, to identify usage of an AI application, create a domain signature for it and set its category to AI Tools.

## How domain usage discovery works

Domain usage discovery runs inline as part of existing web usage processing:

-   After the system resolves a visited domain, it checks the domain against the active domain-type signatures.
-   Domain matching is case-insensitive.
-   If the domain matches a signature, the system records the endpoint, domain, user, matching signature, and category.
-   Existing web usage data collection and storage are unaffected. This classification happens in addition to, not instead of, standard web usage tracking.
-   The system records each endpoint, domain, and user combination only one time. It doesn't update or duplicate existing records.
-   The system loads the active domain signatures fresh each time it processes web usage data, so newly activated signatures are detected without requiring a restart.

-   **[Categorize domain usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-discover-ai-domain-usage.md)**  
Group the domains that users visit in your environment by business relevance, such as AI tools, productivity applications, or security services.

**Parent Topic:**[Deploying Agent Client Collector on endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-endpoint-deployment.md)

