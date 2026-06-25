---
title: Solution configurations
description: Solution configurations let you link multiple blueprints together so buyers complete related product configurations in a single, connected session.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/solution-configurations.html
release: australia
topic_type: concept
last_updated: "2026-03-26"
reading_time_minutes: 2
keywords: [solution configuration, CPQ, blueprints, solution root]
breadcrumb: [CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Solution configurations

Solution configurations let you link multiple blueprints together so buyers complete related product configurations in a single, connected session.

A solution configuration combines two or more blueprints into a coordinated configuration session. When a buyer reaches a product that requires additional configurable components, each component opens in its own child configuration — linked to the parent through configurable product actions. The result is a unified session with a consolidated bill of materials \(BOM\).

Solution configurations suit complex products that span multiple independent blueprints, such as a platform product that includes separately configurable hardware and software components. Each blueprint can be deployed and updated independently, and the same blueprint can participate in multiple solutions.

A configuration becomes a solution when at least one child configuration is added. The product that a buyer starts from is the solution root. From the root, any number of child configurations — and child-of-child configurations — can be created based on rules defined in the admin.

**Note:** Solution configuration is an environment-level feature that is off by default. Contact Support to enable it for your environment by using the [ServiceNow Support portal](https://support.servicenow.com). For step-by-step instructions, see [Create a case on Now Support for CPQ \(Logik.ai\) Customers](https://support.servicenow.com/kb?sys_kb_id=d67d3e71475d7a90f64de825126d4326&id=kb_article_view).

## Key concepts

-   Solution root: the top-level configurable product a buyer launches. All other configurations in the session are descendants of the root.
-   Solution hierarchy: the parent-child relationship between configurable products in a session. The hierarchy is independent of the BOM hierarchy and supports a maximum depth of four levels, including the root.
-   Solution BOM: the consolidated bill of materials that rolls up all products added across every configuration in the session.
-   Field mapping: a mechanism for passing field values from a parent blueprint to a child blueprint when a child configuration is created or when a mapped source field changes.

## When to use solution configurations

Solution configurations work well when you need to manage complex products as separate, independently deployable blueprints while keeping the buyer experience connected. For simpler scenarios, consider these alternatives:

-   Sets: use when managing large numbers of rows that may have different configurations within the same blueprint.
-   Product Pickers: use for lightly configurable products that do not require a separate blueprint.
-   Multiple independent configurations: use when downstream systems require separate, unlinked configuration outputs.

**Related topics**  


[Enable solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/enable-solution-configuration.md)

[Solution configuration terminology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Solution configuration limits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Field mapping supported field types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

