---
title: Purchase requisition line-level questions in Shopping Hub
description: Line-level questions let procurement admins capture product-specific information during checkout, improving data accuracy and enabling flexible purchase requisition workflows.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-11-17"
reading_time_minutes: 2
breadcrumb: [My purchases on Shopping Hub, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase requisition line-level questions in Shopping Hub

Line-level questions let procurement admins capture product-specific information during checkout, improving data accuracy and enabling flexible purchase requisition workflows.

## Key benefits

Capture essential information during request intake to minimize back-and-forth communication between the requester, fulfiller, and supplier.

## How to configure

Role required: sn\_shop.procurement\_administrator

Plugin required: Shopping Hub \(sn\_spend\_uib\)

For more information about creating configurable, line-level questions for shoppers, see [Configure purchase requisition line-level questions in ShoppingHub](../task/configure-additional-information-prl.md).

## How it works

Learn how shoppers can access and enter additional product information at the line level when creating or reviewing purchase requisitions.

The additional information or questions added in the record producer for a specific product, product model, or product category appear during checkout in Shopping Hub.

If the questions are configured as mandatory, selecting**Add to cart** or **Request to buy** expands the Additional information section, where you must provide your responses. You can submit the purchase only after answering all mandatory purchase requisition line-level questions for the selected product.

![Product details page in Shopping Hub.](../image/sh-display-addl-line-level.png "Additional Information section in Shopping Hub")

**Note:** Edits to additional questions require shoppers to create a case for a fulfiller to update the responses. Shoppers can also request updates by posting a message in the purchase’s activity stream.

If you select **Add to cart** or **Request to buy** without completing mandatory fields in the Additional Information section, a message prompts you to fill them first.

![Message to fill in mandatory fields.](../image/sh-display-line-error.png "Fill mandatory fields message in Additional Information section")

After a purchase requisition is created for your request, the fulfiller can view the additional information in the Variables section of the purchase requisition line record in the ServiceNow AI Platform.

**Note:** The **Variables** input field is not available by default in the Outbound Order \[sn\_spend\_intg\_outbound\_purchase\_order\] staging table. To integrate with an ERP system, you must add the **Variables** field.

![Variables section of a PRL record in the ServiceNow AI Platform.](../image/sh-display-addl-variables.png "Variables section of a PRL record in ServiceNow AI Platform")

Additionally, the fulfiller can view this information on the **Details** tab of the purchase requisition line record in the Source-to-Pay Workspace.

**Note:** Fulfillers can update the response in the Variables section on the PRL record. The fulfiller can modify responses until the POL moves to the Ordered state. When the POL is in Revision state, the Variables section becomes editable again.

![Details tab of a PRL record in the Source-to-Pay Workspace](../image/sh-display-addl-prl.png "Details tab of a PRL record in Source-to-Pay Workspace")

**Note:** Fulfillers can update the response in the Variables section on the PRL record’s **Details** tab in the Source-to-Pay Workspace. The fulfiller can modify responses until the POL moves to the Ordered state. When the POL is in Revision state, the Variables section becomes editable again.

The additional information also appears on the Purchase details page under My purchases in Shopping Hub.

![Purchase details page in My purchases](../image/sh-my-purchases-add-info.png "Purchase details page in My purchases")

**Parent Topic:**[My purchases on Shopping Hub](my-purchases.md)

