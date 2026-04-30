---
title: Advanced Shipment Notification \(ASN\)
description: Advanced Shipment Notification \(ASN\) automates the creation of asset records in the In transit state when vendors supply both asset and shipment details before delivery.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-01-28"
reading_time_minutes: 2
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Advanced Shipment Notification \(ASN\)

Advanced Shipment Notification \(ASN\) automates the creation of asset records in the In transit state when vendors supply both asset and shipment details before delivery.

When a purchase order is created for specific models, vendors can provide detailed asset and shipment information ahead of delivery. ASN uses this information to generate asset records in the In Transit state automatically, reducing manual entry, and enhancing tracking accuracy.

Starting with Hardware Asset Management version 15.0.0, you can initiate the ASN workflow with any of the following roles:

-   ham\_admin
-   ham\_user
-   procurement\_admin
-   asset
-   admin \(existing role\)

Starting with Hardware Asset Management version 15.0.0, you can initiate the ASN import process in the Procurement view of the Hardware Asset Workspace.

## ASN Workflow

1.  Download the standardized ASN template \(.xlsx\) and share it with the vendor for completion.
2.  The vendor completes and returns the template with asset and shipment information.
3.  Import the updated ASN template into the system, where:

    1.  A record with a **Pending** status is created in the Shipment Notification Upload \[sn\_itam\_common\_asn\_upload\] table, which initiates the ASN flow.
    2.  Data from the ASN template is populated into an intermediate staging table for field validation.
4.  After the validation, the following changes happen:

    For rows validated successfully:

    -   Asset records are created in the **In Transit** state.
    -   Assets are associated with purchase order line items.
    -   Purchase order statuses are updated to **Pending Delivery**.
    For rows that failed validation:

    -   Records are either ignored or skipped.
    -   Asset records aren't created.

## ASN import validations

The system validates the data in the ASN import template to verify its accuracy before generating asset records.

-   **Purchase Order \(PO\) validations**
    1.  Verifies that any PO provided in the template exists and is valid in the system.
    2.  Requires that valid POs should be in either an **Ordered** or **Pending Delivery** state. Otherwise, the system skips the record.
    3.  The system creates an asset record and adds the **Shipment details** in the template to the **Comments** field, if a PO isn't found.
-   **Location validations**
    1.  Confirms that the location field in the template isn’t empty.
    2.  if no PO is mentioned in the template, validates the provided location.
-   **Model validations**
    1.  Checks that the model is provided and exists in the system.
    2.  Ignores software models automatically, as software licenses aren’t supported through the ASN import.
    3.  Evaluates the asset tracking strategy for the model:
        -   If the strategy is set to **Don't create asset**, asset record isn't created.
        -   If the strategy is set to **Track as Consumable**, unique identifier check isn't performed.
    4.  Tracks serialized assets belonging to a model category linked to a CI class with defined identification rules:
        1.  Retrieves unique identifier fields.
        2.  Validates that all required unique fields are present.
        3.  Verifies that at least one unique field value in the import data is different from the values in existing asset records.
-   **Quantity validations for non-consumable assets**
    1.  Checks that the quantity doesn't exceed 1.
    2.  If the provided quantity exceeds 1, logs an error message in the staging table, resets the quantity to **1**, and creates an asset record.

For more details on ASN import process, see [Use Advanced Shipment Notification](../task/advanced-shipment-notification.md).

