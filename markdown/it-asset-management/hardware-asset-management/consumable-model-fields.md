---
title: Consumable model fields
description: Consumable Models form and related list field descriptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/consumable-model-fields.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Hardware Asset Management, IT Asset Management]
---

# Consumable model fields

Consumable Models form and related list field descriptions.

|Field|Description|
|-----|-----------|
|Display name|Name of the model that is dependant on name of the asset and the manufacturer.|
|Model category|Model category of the asset. The type of category depends if the asset is linked to a CI.|
|State|Current state of the asset.|
|Substate|Current substate of the asset.|
|Stockroom|Name of the stockroom where the asset is located if the asset is in stock.|
|Quantity|Number of assets.|

## Vendor Catalog Item related list

|Field|Description|
|-----|-----------|
|Name|Display name of the vendor catalog item.|
|Vendor|Name of the product vendor.|
|Product Model|Product model associated with the vendor catalog item.|
|Out of Stock|Option that indicates if the product is out of stock.|
|Application|Application that contains the product record.|
|Product ID|Manufacturer product ID.|
|List Price|List price of the product before any discounts are applied.|
|Vendor Price|Vendor price of the product.|
|Rank tier|Vendor rank tier.|
|Short Description|Description of the product.|
|General|
|Product Catalog Item|Product catalog item that was created when the item was published.|
|UPC|Universal Product Code \(UPC\) of the product.|
|Description|Description of the product.|
|Picture|Picture of the product.|
|Active|Option that indicates if the product is active or not.|
|Information|
|Specifications|Product specifications that come from the vendor.|
|Features|Product features that come from the vendor.|

## Consumable Model Lifecycles related list

<table id="table_lmg_d1y_cjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model

</td><td>

Name of the model.

</td></tr><tr><td>

Lifecycle type

</td><td>

The model lifecycle type values include:-   **Internal**: The lifecycle date is specific to the customer \(for example, based on their internal policy, based on a custom contract/agreement with the publisher\).
-   **Publisher**: The lifecycle date comes from manufacturer and is not specific to a customer.

</td></tr><tr><td>

Lifecycle phase

</td><td>

Phase of the lifecycle for a consumable model.-   **General Availability**: The date when the model becomes generally available through the manufacturer’s sales channels, including its worldwide subsidiaries, affiliates, and country distributors. The model is considered current/active and receiving support from the manufacturer.
-   **End of Sale**: The last date to order the model through the manufacturer’s sales channels, including its worldwide subsidiaries, affiliates, and country distributors. After end of sale date, the model is no longer available for sale.
-   **End of Support**: The last date upon which the manufacturer provides standard/regular support for the consumable as entitled by active service contracts. After this date, the manufacturer may continue to provide active support for certain issues in a limited capacity, the scope of which may vary across different manufacturers according to their lifecycle and/or support policies.
-   **End of Extended Support**: Up until this date, the manufacturer extends limited support for the consumable \(after standard/regular support expires\), for a defined period according to manufacturer policy.
-   **End of Life**: The date which indicates the consumable is at the end of its useful life \(from the manufacturer’s point of view\). The manufacturer stops marketing, selling, or sustaining the consumable.

</td></tr><tr><td>

Source

</td><td>

Source of the lifecyle of the model.

</td></tr><tr><td>

Description

</td><td>

Description of the lifecycle.

</td></tr><tr><td>

Phase start date

</td><td>

Date the lifecycle phase starts.

</td></tr><tr><td>

Phase end date

</td><td>

This field is intentionally left empty and is not utilized by any hardware models within the Hardware Asset Management application.

</td></tr><tr><td>

Risk

</td><td>

Risk associated with the lifecycle.

</td></tr><tr><td>

Active

</td><td>

Option that indicates the lifecycle of the model is active.

</td></tr></tbody>
</table>**Parent Topic:**[Hardware Asset Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/reference-hardware-asset-management.md)

**Related topics**  


[Create a hardware or consumable model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-hardware-consumable-model.md)

