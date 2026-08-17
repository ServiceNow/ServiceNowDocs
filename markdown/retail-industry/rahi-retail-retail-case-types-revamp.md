---
title: Retail case types
description: A case type represents the processes, data, and automation needed to resolve a specific type of retail issue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-retail-case-types-revamp.html
release: australia
topic_type: concept
last_updated: "2026-06-28"
reading_time_minutes: 2
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

For more information on extending retail case types, see [Extending the Retail base case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-extending-retail-base-case.md).

-   **[Retail case overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-case.md)**  
The Retail case table stores information about your retail case types and provides the base for retail case creation. This table extends the Customer Service Management case table. All fields utilized through Customer Service Management case remain intact.

**Parent Topic:**[Exploring Retail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-operations-explore.md)

**Related topics**  


[Prebuilt Retail case types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-ootb-case-types.md)

[Extending the Retail base case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-extending-retail-base-case.md)

