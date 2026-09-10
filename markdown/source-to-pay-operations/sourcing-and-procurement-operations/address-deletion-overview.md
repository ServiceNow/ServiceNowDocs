---
title: Managing saved delivery addresses
description: Shopping Hub enables end users to save multiple delivery addresses for convenient checkout and purchasing workflows. Over time, users may need to remove addresses they no longer use, such as former work locations, temporary addresses, or duplicate entries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/address-deletion-overview.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [address deletion, delivery location, Shopping Hub, saved addresses]
breadcrumb: [Shopping Hub, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Managing saved delivery addresses

Shopping Hub enables end users to save multiple delivery addresses for convenient checkout and purchasing workflows. Over time, users may need to remove addresses they no longer use, such as former work locations, temporary addresses, or duplicate entries.

The address deletion feature provides a safe, auditable way to manage saved delivery addresses.

-   Delete individual saved addresses from the Shopping Preferences interface
-   Remove multiple addresses in bulk using a multi-select modal
-   Replace default delivery addresses when deleting the currently active default
-   Retain deleted addresses for auditing and recovery
-   Automatically hide deleted addresses at checkout and on off-catalog record producer forms

## Address deletion scenarios

-   Single address removal: When you delete a work address you no longer use, a success notification confirms the deletion.
-   Default address replacement: You delete your current default delivery address and select a new default using the Manage saved addresses modal.
-   Bulk deletion: You can remove multiple addresses at once using the Manage saved addresses modal. You can't delete all addresses at once and must keep at least one saved address.
-   Address re-addition: You can re-add a previously deleted address from the work address picker to restore it to your saved list.

**Note:** Deleted addresses aren't permanently removed; instead, they are marked with a deleted flag in the `sn_shop_delivery_location` table, enabling auditability and potential future restore operations.

\[Omitted image "spo-delivery-locations-table.png"\] Alt text: Delivery Locations list with the Deleted column highlighted, showing records marked true or false.

-   **[Delivery address filtering at checkout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/delivery-address-filtering-checkout.md)**  
When a shopper removes a saved delivery address, the Deleted column in the Delivery locations table is set to **true** for that address record. The Shopping Hub checkout flow automatically filters out all addresses where the Deleted column is **true**, so those addresses do not appear as options during checkout.
-   **[Delivery address filtering in record producers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/address-filtering-record-producers.md)**  
Off-catalog record producer forms include address fields that enable shoppers to specify delivery locations. Removed delivery addresses do not appear in these fields, consistent with Shopping Hub checkout behavior.

**Parent Topic:**[Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/shopping-hub-overview.md)

**Related topics**  


[Delete a saved address](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/address-deletion-delete-single.md)

[Address deletion permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/address-deletion-access-control.md)

