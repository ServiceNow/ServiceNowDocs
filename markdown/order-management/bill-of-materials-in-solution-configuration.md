---
title: Bill of Materials in solution configuration
description: The solution bill of materials consolidates products from all configurations in a session, including child and grandchild configurations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/bill-of-materials-in-solution-configuration.html
release: australia
topic_type: concept
last_updated: "2026-03-26"
reading_time_minutes: 1
breadcrumb: [Solution configurations, CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Bill of Materials in solution configuration

The solution bill of materials consolidates products from all configurations in a session, including child and grandchild configurations.

The solution BOM is a roll-up of all products added across every configuration in a session. It includes products from the solution root and from every child configuration below it, to any depth.

The BOM hierarchy — the parent-child nesting of individual products within the BOM — is controlled by the Parent Product and Unique Identifier properties defined in each product action. This is separate from the solution hierarchy. A child configuration can add products at any level of the BOM, including at the top level of the parent.

When two child products share the same parent product and product ID but should appear as distinct entries in the BOM, each requires a unique Unique Identifier value.

**Related topics**  


[View the solution bill of materials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-solution-bom.md)

[Solution navigation and layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/solution-navigation-layout.md)

[Solution configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/solution-configurations.md)

