---
title: Purchasing from punchout or third-party suppliers
description: Shoppers who are part of the punchout group can navigate to punchout or external third-party supplier sites from Shopping Hub or Employee Center and make purchases. They can view the third-party purchases in the My purchases page on Shopping Hub, and also view the shipment records received from the third-party sites.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Using Shopping Hub, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchasing from punchout or third-party suppliers

Shoppers who are part of the punchout group can navigate to punchout or external third-party supplier sites from Shopping Hub or Employee Center and make purchases. They can view the third-party purchases in the My purchases page on Shopping Hub, and also view the shipment records received from the third-party sites.

## External suppliers on Shopping Hub

Shoppers who are part of the punchout group can view punchout or external third-party supplier sites from the following tabs or widgets in Shopping Hub Home after navigating to **All** &gt; **ShoppingHub** &gt; **ShoppingHub Home**.

-   **Suppliers** &gt; **Supplier sites** tab: Shoppers can select the **Supplier site** check box to filter their search for external or punchout suppliers.
-   **Purchase directly from the supplier site** widget: Shoppers can view up to four external supplier cards here. If there are more than four external suppliers, they can view all by going to the complete list.

For more information on punchout groups and how to configure them as an admin, see [Configure punchout for third-party site purchases](../task/configure-supplier-punchout.md).

## External suppliers on Employee Center

Shoppers who are part of the punchout group can also view punchout or external third-party supplier sites from the following tabs in Employee Center after navigating to **All** &gt; **Employee Center**.

-   **Purchase and Expense** &gt; **Quick links** &gt; **Purchase directly from supplier sites**.
-   **Purchase and Expense** &gt; **Browse all** &gt; **Quick links** &gt; **Purchase directly from supplier sites**.

For more information on Employee Center, see [Sourcing and Procurement Operations integration with Employee Center](employee-center-integration-psm.md).

## Checkout from external supplier sites or Shopping Hub

The shoppers can search for all products, including the ones offered by external suppliers, from within Shopping Hub.

The configuration of the punchout supplier's Order API determines whether the shoppers can place orders for products within the Shopping Hub or on the supplier's external website.

All products from punchout or third-party suppliers are shown on the Products and Services page within Shopping Hub. If a supplier has configured the Order API, the shopper is no longer redirected to the supplier's external website to view products and add them to the cart. The shopper can do this directly within Shopping Hub and then proceed with the usual quick or full checkout process.

However, if a supplier hasn't configured the Order API, a notification message appears, informing shoppers that they are leaving the Shopping Hub application and are being redirected to the supplier's external website. After the shopper selects **Confirm**, they are navigated to the supplier's external website to add items to the cart and place the order. The shopper is subsequently redirected to Shopping Hub where they can continue with the checkout process.

For more information, see [Configure punchout for third-party site purchases](../task/configure-supplier-punchout.md).

For more information see [Order a product with quick checkout](../task/order-a-product.md) and [Complete your checkout](../task/complete-your-checkout.md).

## Post checkout from external supplier sites or Shopping Hub

After successfully completing a checkout from either an external third-party supplier site or from within Shopping Hub, a shopper can view the third-party purchase requisition in the My purchases page ​from Shopping Hub Home. The purchase requisition record contains details of the third-party supplier, purchase lines with product names, and the associated approvals, contracts, and cases.

Once the necessary approvals are received and the associated cases are completed, a purchase order is created by the procurement specialist. The same purchase order can also be viewed by the procurement admin in the external site in their order logs. The order confirmation and shipment confirmation details are received from the external supplier site as and when the order is processed. Shipment details are captured in the Shipment Details table by purchase lines.

In case of an update to the order quantity or price at the external supplier end, the same is sent as a revision during order confirmation to SPO, which is then updated in SPO as a revision purchase requisition. For more information on purchase revision scenarios, see [Purchase revision flows](purchase-revision-flows.md).

For information on emails triggered by the system, see [Alerts and email notifications from Shopping Hub](../reference/alerts-messages-email-notifications.md).

## Troubleshooting errors

-   In case of any failures in creating purchase requisitions, check the import logs or transform history records.​ Check the flow actions 'Send Punchout Setup request' and 'Send punchout order request' context executions for connection setup failures and order confirmation failures​. Check the 'Punchout Edit/Cancel flow' context executions for punchout revision flow failures​.
-   An error code of 500 would indicate an invalid credential record or a missing punchout configuration in the third-party registration for supplier​.
-   If a purchase order or purchase requisition is stuck in the Pending Supplier Confirmation status, review the system logs for any potential errors and resolve them to allow further processing of the purchase order or purchase requisition.

**Parent Topic:**[Using Shopping Hub](../reference/use-shoppinghub-portal.md)

