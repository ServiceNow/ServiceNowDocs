---
title: How L1 punchout works
description: In the Level 1 \(L1\) punchout, SPO and the punchout supplier communicate using the cXML protocol.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/level-one-punchout.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Understanding punchout, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# How L1 punchout works

In the Level 1 \(L1\) punchout, SPO and the punchout supplier communicate using the cXML protocol.

## L2 punchout flow

The following figure illustrates the L1 Punchout flow.\[Omitted image "punchout-level-one-flow.png"\] Alt text: L1 punchout flow.

## Communication between SPO and punchout supplier for Level 1 punchout

The following figure illustrates the interaction between SPO and the punchout supplier for a Level 1 Punchout.

**Note:** This flow is also applicable to other Punchout systems; however, the content of the cXML payloads may vary depending on the provider.

\[Omitted image "punchout-spo-site-comm.png"\] Alt text: Communication between SPO and punchout supplier site.

## Cart checkout from the punchout supplier site

The cart checkout flow involves the following:

-   When a user checks out the cart on the punchout supplier site, the punchout supplier \(or other Punchout systems\) sends a PunchoutOrderMessage cXML payload to the REST endpoint exposed by SPO.
-   The details of this endpoint are included in the PunchoutSetupRequest payload, enabling the punchout supplier to know where to send the order request.
-   After SPO receives the PunchoutOrderMessage payload, it processes the information and creates the corresponding SPO cart lines.
-   The user then reviews the cart in SPO and proceeds to checkout. Upon successful checkout, a purchase requisition \(PR\) is created.

The following figure illustrates this flow:

\[Omitted image "punchout-cart-checkout.png"\] Alt text: Cart checkout from punchout system.

## Sending purchase order to punchout system

Sending purchase order information to the punchout supplier system involves the following:

-   When a PR is approved and a PO is created, SPO needs to send OrderRequest cXML payload to the punchout supplier system.
-   The flow action Send Punchout Order Request sends the PO to the punchout system.
-   The punchout supplier creates the order and sends confirmation.

The following figure illustrates this flow:

\[Omitted image "punchout-sending-po.png"\] Alt text: Sending PO to punchout system.

## Processing order confirmation and shipping confirmation from punchout supplier system

The punchout supplier sends the order confirmation payload to the Order Confirmation URL, which is configured in the punchout supplier's system. Similarly, for each order line, the punchout supplier may optionally send a shipping confirmation payload to the Shipping Confirmation URL. For more information, see [Providing Order and Shipping Confirmation URLs to Punchout Suppliers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/punchout-urls.md).

The following figure illustrates this flow:

\[Omitted image "punchout-order-confirmation.png"\] Alt text: Order confirmation from punchout system.

The following figure illustrates this flow:

\[Omitted image "punchout-shipping-confirm.png"\] Alt text: Shipping confirmation from punchout system.

**Parent Topic:**[Understanding punchout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/punchout-overview.md)

