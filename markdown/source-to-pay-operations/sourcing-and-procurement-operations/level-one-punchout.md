---
title: How L1 punchout works
description: In the Level 1 \(L1\) punchout, SPO and the punchout supplier communicate using the cXML protocol.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Understanding punchout, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# How L1 punchout works

In the Level 1 \(L1\) punchout, SPO and the punchout supplier communicate using the cXML protocol.

## L2 punchout flow

The following figure illustrates the L1 PunchOut flow.![L1 punchout flow.](../image/punchout-level-one-flow.png)

## Communication between SPO and punchout supplier for Level 1 punchout

The following figure illustrates the interaction between SPO and the punchout supplier for a Level 1 PunchOut.

**Note:** This flow is also applicable to other PunchOut systems; however, the content of the cXML payloads may vary depending on the provider.

![Communication between SPO and punchout supplier site.](../image/punchout-spo-site-comm.png)

## Cart checkout from the punchout supplier site

The cart checkout flow involves the following:

-   When a user checks out the cart on the punchout supplier site, the punchout supplier \(or other PunchOut systems\) sends a PunchOutOrderMessage cXML payload to the REST endpoint exposed by SPO.
-   The details of this endpoint are included in the PunchOutSetupRequest payload, enabling the punchout supplier to know where to send the order request.
-   After SPO receives the PunchOutOrderMessage payload, it processes the information and creates the corresponding SPO cart lines.
-   The user then reviews the cart in SPO and proceeds to checkout. Upon successful checkout, a purchase requisition \(PR\) is created.

The following figure illustrates this flow:

![Cart checkout from punchout system.](../image/punchout-cart-checkout.png)

## Sending purchase order to punchout system

Sending purchase order information to the punchout supplier system involves the following:

-   When a PR is approved and a PO is created, SPO needs to send OrderRequest cXML payload to the punchout supplier system.
-   The flow action Send Punchout Order Request sends the PO to the punchout system.
-   The punchout supplier creates the order and sends confirmation.

The following figure illustrates this flow:

![Sending PO to punchout system.](../image/punchout-sending-po.png)

## Processing order confirmation and shipping confirmation from punchout supplier system

The punchout supplier sends the order confirmation payload to the Order Confirmation URL, which is configured in the punchout supplier's system. Similarly, for each order line, the punchout supplier may optionally send a shipping confirmation payload to the Shipping Confirmation URL. For more information, see [Providing Order and Shipping Confirmation URLs to Punchout Suppliers](punchout-urls.md).

The following figure illustrates this flow:

![Order confirmation from punchout system.](../image/punchout-order-confirmation.png "Processing order confirmation from punchout system")

The following figure illustrates this flow:

![Shipping confirmation from punchout system.](../image/punchout-shipping-confirm.png "Processing shipping confirmation from punchout system")

**Parent Topic:**[Understanding Punchout](punchout-overview.md)

