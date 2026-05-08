---
title: Service Catalog readiness for Now Assist on the ServiceNow AI Platform
description: A well-structured Service Catalog is essential to unlocking the full potential of Now Assist. As the backbone of many self-service workflows, the catalog enables Now Assist to interpret user requests accurately, present the right options, and minimize friction in the experience.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, agentic AI, AI readiness]
breadcrumb: [Application readiness, ServiceNow AI implementation, Enable AI experiences]
---

# Service Catalog readiness for Now Assist on the ServiceNow AI Platform

A well-structured Service Catalog is essential to unlocking the full potential of Now Assist. As the backbone of many self-service workflows, the catalog enables Now Assist to interpret user requests accurately, present the right options, and minimize friction in the experience.

When catalog items are clearly defined and conversationally enabled, Now Assist in Virtual Agent can surface them more effectively, leading to higher self-service rates and better issue deflection.

However, catalogs that are cluttered, inconsistent, or overly complex make it difficult for AI to parse and respond appropriately. That’s why auditing your existing catalog is a critical first step. By identifying which items are AI-ready and optimizing those that aren’t, you ensure that Now Assist can deliver intelligent, context-aware responses.

## High-level checklist

-   **1. Install the Catalog Conversational Coverage \(sn\_catalog\_con\_cov\) plugin**

    This plugin gives you access to the conversational catalog overview dashboard.

    See: Install an application or plugin

-   **2. Review your catalog inventory**

    Use the conversational catalog overview dashboard to review all active catalog items. From this list, determine which are most requested and the percentage that are conversational.

    Why? To focus improvement efforts on the catalog items with the highest impact.

    See:

    -   Catalog Conversational Coverage
    -   Conversational catalog overview dashboard
-   **3. Determine which catalogs can be made conversational**

    Identify catalog items with fewer than 15 variables. \(Items with more than 15 variables are better suited to be submitted as pop-up links to forms.\)

    **Note:** Conversational catalog items require Now Assist in Virtual Agent. For details, see [Now Assist in Virtual Agent readiness on the ServiceNow AI Platform](sn-ai-impl-nava.md).

    Why? These are easier to convert and provide quick AI wins.

    See: Service catalog variables

-   **4. Analyze catalog item metadata**

    Ensure catalog items have clear, user-friendly names, tooltips, metadata, and categories. Using templates can help with this as well.

    Why? This prevents LLM confusion and improves conversational flow.

    See:

    -   Service Catalog properties
    -   Edit a catalog item in Catalog Builder
    -   Create a catalog item using a template
-   **5. Review advanced configurations**

    Review UI policies, client scripts, and user criteria.

    Why? User criteria determines who can request an item, but policies and scripts are ignored by Virtual Agent.

    See:

    -   Service catalog UI policy
    -   Set security for items and categories
    -   Create a user criteria record in Service Catalog
    -   Create a Service Catalog client script

## Tips

-   Use Now Assist in Catalog Builder to generate catalog items.
-   Limit the number of variables. Fewer is better.
-   For form-based requests, select the Make item non-conversational in VA check box.
-   Provide clear context for the LLM with distinct names, labels, and tooltips.
-   Minimize the use of custom variable types. Use the service catalog variables included on the platform instead.
-   Limit client-side scripting and use regular expressions for validation.
-   Avoid complex dependencies. Simplify variable relationships to ensure a smooth conversation flow.
-   Test and iterate: make changes based on feedback.

For more information about conversational catalogs in AI, see the following ServiceNow Community articles:

-   [Guidance for making catalog items conversational](https://www.servicenow.com/community/intelligence-ml-articles/now-assist-in-conversational-catalog-request-guidance-for-making/ta-p/2987560)
-   [How to request catalog items in Now Assist in Virtual Agent](https://www.servicenow.com/community/virtual-agent-nlu-articles/how-to-request-catalog-items-in-now-assist-in-virtual-agent/ta-p/2747811)

