---
title: Explore Partial sync
description: Partial sync in the primitives framework enables selective synchronization of data between Quote and Opportunity entities in ServiceNow Order Management \(SOM\). Rather than processing the entire data structure, Partial sync allows you to synchronize only the portions that have changed, significantly improving performance and reducing unnecessary data processing.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-01-10"
reading_time_minutes: 1
breadcrumb: [Lead to Cash Core, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Explore Partial sync

Partial sync in the primitives framework enables selective synchronization of data between **Quote** and **Opportunity** entities in ServiceNow Order Management \(SOM\). Rather than processing the entire data structure, Partial sync allows you to synchronize only the portions that have changed, significantly improving performance and reducing unnecessary data processing.

## Partial sync as a solution

Partial sync introduces delta-based, selective synchronization with these key capabilities:

-   Selective processing:
    -   Callers specify which child types to process using the `allowedContextTypes` parameter
    -   Only requested sections are populated and synchronized
    -   Full structure skeleton maintained for consistency
-   Related party support:
    -   Automatic synchronization of from quotes to opportunities
    -   Works when the `Synced` flag is enabled on a quote
    -   Maintains data consistency across both entities
-   Performance optimization:
    -   Processes only what changed, not the entire structure
    -   Reduced payload sizes
    -   Faster execution times
    -   Lower resource consumption
-   Structural integrity:
    -   Maintains consistent JSON structure
    -   Empty arrays preserved when types aren't included
    -   No downstream errors from missing data structures
    -   Recursive filtering at all hierarchy levels

## Key concepts

`allowedContextTypes`

The `allowedContextTypes` parameter is an array that controls which sections of the data structure get populated during synchronization.

Example:

```
json
{
  "allowedContextTypes": ["header", "lineitems"]
}
```

## Entities involved

-   `sn_quote_mgmt_core_quote_related_party`: Table for related channel partners on quotes.
-   `sn_bus_org_opptym_related_business_organization`: Table for related channel partners on opportunities.

