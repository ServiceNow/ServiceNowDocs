---
title: Search for punchout products in Employee Center
description: You can search for punchout products directly in Employee Center using the AI search bar.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/ec-search-punchout-products.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Sourcing Procurement Operations integration Employee, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Search for punchout products in Employee Center

You can search for punchout products directly in Employee Center using the AI search bar.

## Before you begin

Role required: sn\_shop.shopper

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  In the search bar, search for any punchout product that you want to buy.

    \[Omitted image "ec-punchout-search.png"\] Alt text: Employee Center search bar

3.  The punchout products that match your search criteria are listed in the **Supplier site catalog** tab.

    \[Omitted image "ec-punchout-search-results.png"\] Alt text: Supplier site catalog tab in Employee Center

    **Important:** Only cXML punchout products are displayed in the **Supplier site catalog** tab. The punchout products uploaded via API are not listed.

4.  Select a product to purchase.

    You are redirected to the supplier site to add items to the cart. Depending on your setup, the following occurs:

    -   If you've installed Shopping Hub, you are redirected back to Shopping Hub from the supplier site to complete the checkout process.
    -   If you haven't installed Shopping Hub, you must complete the checkout process and place the order on the supplier site.
    For more information about the checkout experiences for shoppers based on whether they have installed Employee Center, Shopping Hub, or both, see [Shopper checkout experiences based on installed applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/ec-sh-checkout-flow.md).


**Parent Topic:**[Sourcing and Procurement Operations integration with Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/employee-center-integration-psm.md)

