---
title: Submit multi-product sourcing requests
description: Requesters can submit sourcing requests with multiple products in a single sourcing intake form. When a sourcing request form contains multiple products, the third-party sourcing solution automatically creates individual sourcing events for each product.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Sourcing Procurement Operations integration third-party, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Submit multi-product sourcing requests

Requesters can submit sourcing requests with multiple products in a single sourcing intake form. When a sourcing request form contains multiple products, the third-party sourcing solution automatically creates individual sourcing events for each product.

## Before you begin

Role required: sn\_shop.shopper

## About this task

When a requester submits a sourcing intake form with multiple products, the third-party sourcing solution automatically:

-   Creates individual sourcing request for each product.
-   Maps each sourcing request to its own sourcing event.
-   Links all sourcing requests to a single purchase record.
-   Synchronizes data to the third-party tool, generating a separate Request for Quote \(RFQ\) for each sourcing request.
-   Updates third-party RFQ data, such as RFx ID, RFx status, and RFx URL, in the corresponding sourcing request and sourcing event.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  Select the **Purchases and expenses** drop-down list and select **Purchase request**.

3.  Select the **I need a product** record producer.

    ![Purchase requests displayed.](../image/multi-prod-3p-step3.png)

4.  Select your request details.

    ![Select your requirement for the request.](../image/multi-prod-3p-step4.png)

5.  Select your preferred supplier.

    ![Add existing supplier in the system.](../image/multi-prod-3p-step5.png)

    To add an existing supplier:

    1.  Select **Existing suppliers in the system** &gt; **Add**.
    2.  In the **Existing supplier** drop-down list, select your preferred supplier.
    3.  Select **Add**.
    To add an external supplier:

    1.  Select **External suppliers** &gt; **Add**.
    2.  Enter the supplier details, such as supplier name, job title, and email.
    3.  Select **Add**.
6.  Select your delivery address and delivery date.

    ![Selected a saved address for delivery address and as soon as possible for delivery date.](../image/multi-prod-3p-step6.png)

7.  Under **Products** section, select **Add**.

    You can add up to 50 different products in a single request.

8.  For each product, enter the product name, quantity or budget, delivery address, and delivery date.

    ![Form to add product details.](../image/multi-prod-3p-step8.png)

9.  Enter the reason why you need these products.

    ![Enter the reason to request the products.](../image/multi-prod-3p-step9.png)

10. Select **Submit**.

    ![Multiple sourcing requests are created for the same purchase requisition.](../image/multi-prod-3p-result.png)


## Result

Multiple sourcing requests are created and linked to the same purchase record. All related requests are visible and manageable in the Source-to-Pay Workspace, and each sourcing request has its own sourcing event and RFQ identifier.

**Parent Topic:**[Sourcing and Procurement Operations integration with third-party sourcing solutions](../concept/psm-integration-third-party-sourcing.md)

