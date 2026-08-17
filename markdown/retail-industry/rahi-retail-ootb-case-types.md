---
title: Prebuilt Retail case types
description: Retail includes four prebuilt case types that extend the retail framework. Each is dependent on its own plugin and is tuned to a common retail scenario, so you can deploy quickly and stay consistent across locations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-ootb-case-types.html
release: australia
topic_type: concept
last_updated: "2026-06-28"
reading_time_minutes: 2
keywords: [prebuilt retail case types, retail case types, case type comparison]
breadcrumb: [Retail case types, Explore, Retail]
---

# Prebuilt Retail case types

Retail includes four prebuilt case types that extend the retail framework. Each is dependent on its own plugin and is tuned to a common retail scenario, so you can deploy quickly and stay consistent across locations.

\[Omitted image "retail-ootb-case-types-erd.svg"\] Alt text: ERD showing the four prebuilt retail case types, their base tables, and associated task tables.

|Case type|Purpose|Dependent on|
|---------|-------|------------|
|[Store Inquiry Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-retail-store-services.md)|Allows store associates and managers to raise operational questions, information requests, or issues to headquarters for fulfillment.|Retail Store Services plugin|
|[Retail Customer Complaint Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-retail-customer-complaint.md)|Captures, classifies, routes, resolves, and measures complaints about a store experience—supporting back-office transparency and efficiency.|Retail Customer Complaint plugin|
|[In-Store Operations Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-retail-in-store-operations.md)|Allows store teams to report and track in-store operational work—routine or cyclical—so execution is documented and monitored.|Retail In-store Operations plugin|
|[HQ Communications Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-retail-hq-operations.md)|Coordinates with store teams by sending communications from HQ and, with the multi-store task plan capability, drives work from HQ to many stores at once.|Retail HQ Operations plugin|

**Note:** As of the Zurich Q3 '25 store release, the Retail Case \(`sn_retail_case`\) table is abstract. Cases must be created in a case type extension, not directly in the base table.

**Related topics**  


[Extending the Retail base case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-extending-retail-base-case.md)

[Service definitions in Retail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-service-definitions.md)

