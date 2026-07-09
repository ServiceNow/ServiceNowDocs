---
title: Create a Quote via Self-Service for Channel Partners
description: Use the Quote Self-Service plugin \(com.sn\_quote\_self\_service\) to create and submit a configured quote directly from the Partner portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/create-a-self-service-quote.html
release: australia
topic_type: task
last_updated: "2026-05-15"
reading_time_minutes: 2
keywords: [create quote, channel partner, quote self-service plugin, PRM]
breadcrumb: [Partner Relationship Management, Use, Sales Customer Relationship Management]
---

# Create a Quote via Self-Service for Channel Partners

Use the Quote Self-Service plugin \(com.sn\_quote\_self\_service\) to create and submit a configured quote directly from the Partner portal.

## Before you begin

Role required: sn\_prm\_qm.quote\_partner\_ui along with one of the following roles:

-   sn\_prm.external\_partner\_manager
-   sn\_prm.partner\_sales\_manager
-   sn\_prm\_sales.partner\_b2b\_sales\_rep
-   sn\_prm\_sales.partner\_b2c\_sales\_rep

## Procedure

1.  Navigate to the Partner portal.

2.  From the portal header, select **Create**, then select **Create Quote** from the drop-down, or select **Catalog &gt; All Services &gt; Create Quote**.

3.  On the quote form, review the following tabs and fill in the required fields:

    -   **Quote details** tab: Enter customer and quote-level information.
    -   \[Omitted image "create-quote.png"\] Alt text: Quote details form showing customer and quote information fields
    -   **Additional details** tab: Specify billing and shipping addresses.
    -   \[Omitted image "self-service-quote-additional-details.png"\] Alt text: Additional details tab showing address fields
    -   \[Omitted image "self-service-quote-additional-details1.png"\] Alt text: Additional details address form
    -   **Product offerings catalog** tab: Browse and select products to include in the quote.
    -   \[Omitted image "self-service-quote-product-offerings.png"\] Alt text: Product offerings catalog showing available products
    -   **Line items** tab: Confirm selected products and quantities.
    -   \[Omitted image "self-service-quote-line-items.png"\] Alt text: Line items form showing selected products with quantities and pricing
    -   **Review and submit** tab: Review the complete quote details before submission.
    -   \[Omitted image "self-service-quote-review-submit.png"\] Alt text: Review and submit tab showing full quote summary
    For field descriptions and additional information about the quote creation form, see [Quote creation via Self-Service fields for Channel Partners](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-creation-fields.md).

4.  On the **Review and Submit** tab, verify the quote details, then select **Review and Submit**.

    The system creates the quote with your associated account or consumer information, channel partner details, and selected line items. A confirmation screen displays. \[Omitted image "quote-submitted.png"\] Alt text: Quote creation confirmation screen

5.  **Download the quote**, or select **Edit quote** to reopen it for further editing.

    \[Omitted image "edit-quote.png"\] Alt text: Edit quote option in quote details screen

6.  After creating a quote, use the overflow menu \(⋮\) to perform any of the following actions:

    -   Edit a quote
    -   Submit a quote for review
    -   Download a quote
    -   Create a revision of a quote
    -   Cancel a quote
    -   Delete a quote

## Result

You can view the list of all quotes, along with quotes in **Draft** and **Submitted** states, on the Partner portal home page.

The Partner portal displays quotes in the following states: **Draft**, **In review**, **Completed**, and **Accepted**.

**Parent Topic:**[Using Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-partner-relationship-management.md)

**Related topics**  


[Quote creation via Self-Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/self-service-quote_generic.md)

[Using Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-partner-relationship-management.md)

