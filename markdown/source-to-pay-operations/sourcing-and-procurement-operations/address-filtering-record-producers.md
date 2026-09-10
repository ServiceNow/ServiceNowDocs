---
title: Delivery address filtering in record producers
description: Off-catalog record producer forms include address fields that enable shoppers to specify delivery locations. Removed delivery addresses do not appear in these fields, consistent with Shopping Hub checkout behavior.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/address-filtering-record-producers.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [record producer, address filtering, removed addresses, off-catalog requestors, delivery location]
breadcrumb: [Saved delivery addresses, Shopping Hub, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Delivery address filtering in record producers

Off-catalog record producer forms include address fields that enable shoppers to specify delivery locations. Removed delivery addresses do not appear in these fields, consistent with Shopping Hub checkout behavior.

## Affected record producers

Address filtering applies to all record producers in the Spend catalog that include delivery address fields:

-   Contract renewal for good
-   Contract renewal for service
-   I need a product
-   I need a service
-   I need to submit a quote

## Address filtering behavior

Address filtering in record producers uses the same pattern as Shopping Hub checkout:

-   All address field queries include a `deleted=false` filter
-   In the delivery address table, the Deleted column is set to **true** when a delivery address is removed and **false** when it is available
-   The filter excludes removed addresses from address field results
-   Available delivery addresses appear for selection as normal

## Shopper experience

-   When filling out a record producer form, only available delivery addresses appear for selection.
-   Shoppers can still browse the full organizational address directory when adding a new work address.
-   If a user re-adds a previously removed address from the work directory, the address reappears as an available option in record producer forms.
-   The same delivery addresses that are unavailable at checkout are unavailable in record producers, providing a consistent experience.

**Parent Topic:**[Managing saved delivery addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/address-deletion-overview.md)

