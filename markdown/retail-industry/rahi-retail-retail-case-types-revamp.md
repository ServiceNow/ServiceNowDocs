---
title: Retail case types
description: A case type represents the processes, data, and automation needed to resolve a specific type of retail issue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-retail-case-types-revamp.html
release: brazil
topic_type: concept
last_updated: "2026-06-28"
reading_time_minutes: 3
keywords: [retail case types, case type, retail implementation]
breadcrumb: [Explore, Retail]
---

# Retail case types

A case type represents the processes, data, and automation needed to resolve a specific type of retail issue.

**Tip:**

For general guidelines on implementing case types, read [Best Practices to Implement Case Types](https://mynow.servicenow.com/now/best-practices/assets/best-practices-to-implement-case-types), which covers:

-   How to identify potential case type candidates
-   How to structure leaf and base-level case types to support scalability
-   How to use service definitions to define processes within case types

You must log in to download the best practices document.

Common use cases in Retail include:

-   A store associate needs to ask headquarters about a store-to-store transfer policy.
-   A customer complains about cleanliness at a store.
-   A food safety manager at HQ needs to drive a product recall across hundreds of locations at once.
-   A point-of-sale break/fix or other retail support issue may need support from groups or departments whose processes don't match traditional out-of-the-box process flows.
-   A point-of-sale break/fix or other retail support issue may require records in different tables. Examples include an Incident or Request for HQ IT teams, or a Work Order for facilities or field maintenance.
-   A monitoring system may create alerts that only require action under specific conditions, requiring dedicated workflows separate from normal resolution patterns to surface actionable alerts to retail agents.

If these retail use cases were built into the same table, it would create significant technical debt. Each optimization to support one process also impacts the other processes running within that case type.

Each example use case requires distinct processes, automation, fulfillers, form requirements, categorization, and access, making each a candidate for its own case type. Optimizations made within one case type remain within that scope, and the impact on other processes running within Retail is negated.

**Note:** Retail implementations should use case types even when you are not starting from one of the prebuilt case types. Even if you have only a single process today, start with one case type instead of working records directly in the base case. This makes it easy to adopt additional case types later, whether from the retail product or from your own custom applications. As of the Zurich Q3 '25 store release, the Retail Case \(`sn_retail_case`\) table is abstract and can no longer store records directly, so a case type extension is required.

For more information on extending retail case types, see [Extending the Retail base case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-extending-retail-base-case.md).

-   **[Prebuilt Retail case types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-ootb-case-types.md)**  
Retail includes four prebuilt case types that extend the retail framework. Each is dependent on its own plugin and is tuned to a common retail scenario, so you can deploy quickly and stay consistent across locations.
-   **[Extending the Retail base case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-extending-retail-base-case.md)**  
Extend the Retail Case \(`sn_retail_case`\) base case to create custom case types that take advantage of prebuilt roles, business rules, workflows, and the Retail data model rather than creating them manually.
-   **[Service definitions in Retail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-service-definitions.md)**  
A service definition describes a service that a retail organization offers to support its stores or customers. Service definitions build on case types to encapsulate different types of request and fulfillment processes within a single case type, without creating a new table for every variation.

**Parent Topic:**[Exploring Retail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-operations-explore.md)

**Related topics**  


[Prebuilt Retail case types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-ootb-case-types.md)

[Extending the Retail base case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-extending-retail-base-case.md)

