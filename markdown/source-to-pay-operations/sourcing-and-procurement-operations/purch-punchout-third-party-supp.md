---
title: Purchasing from punchout or third-party suppliers
description: Shoppers who are part of the punchout group can navigate to punchout or external third-party supplier sites from ShoppingHub or Employee Center and make purchases. They can view the third-party purchases in the My purchases page on ShoppingHub, and also view the shipment records received from the third-party sites.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Shopping Hub, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchasing from punchout or third-party suppliers

Shoppers who are part of the punchout group can navigate to punchout or external third-party supplier sites from ShoppingHub or Employee Center and make purchases. They can view the third-party purchases in the My purchases page on ShoppingHub, and also view the shipment records received from the third-party sites.

## External suppliers on ShoppingHub

Shoppers who are part of the punchout group can view punchout or external third-party supplier sites from the following tabs or widgets in ShoppingHub Home after navigating to **All** &gt; **ShoppingHub** &gt; **ShoppingHub Home**.

-   **Suppliers** &gt; **Supplier sites**: Shoppers can select the **Supplier site** check box to filter their search for external or punchout suppliers.
-   **Purchase directly from the supplier site** widget: Shoppers can view up to four external supplier cards here. If there are more than four external suppliers, they can view all by going to the complete list.

For more information about the checkout experiences for shoppers based on whether they have installed Employee Center, Shopping Hub, or both, see [Shopper checkout experiences based on installed applications](../reference/ec-sh-checkout-flow.md).

For more information on punchout groups and how to configure them as an admin, see [Configure punchout for third-party site purchases](../task/configure-supplier-punchout.md).

## External suppliers on Employee Center

Shoppers who are part of the punchout group can also view punchout or external third-party supplier sites from the following tabs in Employee Center after navigating to **All** &gt; **Employee Center**.

-   **Purchase and Expense** &gt; **Quick links** &gt; **Purchase directly from supplier sites**.
-   **Purchase and Expense** &gt; **Browse all** &gt; **Quick links** &gt; **Purchase directly from supplier sites**.

Shoppers are redirected to the Supplier sites page, with all the punchout suppliers listed there. They can sort and search the list for specific suppliers. Selecting a supplier tile takes them to the external site for making the purchase. For more information about the checkout experiences for shoppers based on whether they have installed Employee Center, Shopping Hub, or both, see [Shopper checkout experiences based on installed applications](../reference/ec-sh-checkout-flow.md).

For more information on Employee Center, see [Sourcing and Procurement Operations integration with Employee Center](employee-center-integration-psm.md).

## Post checkout from external supplier sites

After successfully completing a checkout at an external third-party supplier site, a shopper can view the third-party purchase requisition in the My purchases page ​from ShoppingHub Home. The purchase requisition record contains details of the third-party supplier, purchase lines with product names, and the associated approvals, contracts, and cases.

Once the necessary approvals are received and the associated cases are completed, a purchase order is created by the procurement specialist. The same purchase order can also be viewed by the procurement admin in the external site in their order logs. The order confirmation and shipment confirmation details are received from the external supplier site as and when the order is processed. Shipment details are captured in the Shipment Details table by purchase lines.

In case of an update to the order quantity or price at the external supplier end, the same is sent as a revision during order confirmation to SPO, which is then updated in SPO as a revision purchase requisition. For more information on purchase revision scenarios, see [Purchase revision flows](purchase-revision-flows.md).

For information on emails triggered by the system, see [Alerts and email notifications from ShoppingHub](../reference/alerts-messages-email-notifications.md).

## Troubleshooting errors

In case of any failures in creating purchase requisitions, check the import logs or transform history records.​ Check the flow actions 'Send Punchout Setup request' and 'Send punchout order request' context executions for connection setup failures and order confirmation failures​. Check the 'Punchout Edit/Cancel flow' context executions for punchout revision flow failures​.

An error code of 500 would indicate an invalid credential record or a missing punchout configuration in the third-party registration for supplier​.

