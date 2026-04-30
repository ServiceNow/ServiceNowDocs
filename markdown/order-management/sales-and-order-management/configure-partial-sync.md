---
title: Configure Partial sync
description: Explore how to configure Partial sync.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-01-10"
reading_time_minutes: 1
breadcrumb: [Explore Partial sync, Lead to Cash Core, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Configure Partial sync

Explore how to configure Partial sync.

## Prerequisites

-   Ensure that your instance is running the latest primitive framework with Partial sync support.
-   Confirm that the reverse sync flag \(Synced\) is enabled on the quote entity.

## Configuring Partial sync

1.  Identify the Partial sync trigger: Start Partial sync when a **Quote** update affects only Related Party data \(partners, business organizations, and contacts\).
2.  Retrieve the Primitives EP Service for Quote &gt; Opportunity mapping.

    ```
    var service = util.getPrimitivesEPService('sn_l2c_sync_quote_to_opportunity');
    ```

    This ensures data sync is performed using the correct mapping for Quote → Opportunity.

3.  Prepare Partial sync parameters using `additionalParams.allowedContextTypes` to fetch only the Related Party section from the Quote:

    ```
    
    var additionalParams = {
      allowedContextTypes: ["header", "headerRelatedParty"]
    };
    
    ```

    When `allowedContextTypes` includes header and `headerRelatedParty`, `createInstance` returns only the Related Party section of the **Quote** \(plus the header scaffold\). Pass this filtered instance into the reverse‑sync logic so that only partner deltas are processed and updated on the **Opportunity**.

    **Note:**

    -   For header-based Partial sync, the **header** must be included in `allowedContextTypes`. Without the header, `createInstance` can’t build the root structure.
    -   For no-header Partial sync, the **lineItems** must be included in `allowedContextTypes`. Without it, `createInstance` can’t build a valid structure for processing child data.

## Example to invoke CreateInstance for Partial sync

```
/********Invoking createInstance with only allowedContextTypes – Quote to Opportunity**********/
var service = util.getPrimitivesEPService('sn_l2c_sync_quote_to_opportunity'); // WITH HEADER FLOW 
var quoteId = '04ba9004f11f3110f8777d7194f166f6'; 
var additionalParams = { 
       allowedContextTypes: ["header","headerRelatedParty"]  }; 
var quoteInstance = service.createInstance(quoteId, null, false, additionalParams);

```

