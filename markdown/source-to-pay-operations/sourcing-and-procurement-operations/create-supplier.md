---
title: Add a supplier
description: Add suppliers and their products to populate your primary data.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Setting up primary data Shopping, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Add a supplier

Add suppliers and their products to populate your primary data.

## Before you begin

Role required: sn\_shop.shopping\_hub\_admin or sn\_shop.procurement\_administrator

## About this task

You can add a supplier to the primary data and add products under that supplier. The suppliers that you add, appear on the Shopping Hub portal under Suppliers.

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **Primary Data** &gt; **Suppliers**.

    You can also navigate to **Sourcing and Purchasing Automation** &gt; **Primary Data** &gt; **Supplier**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_hjz_1fd_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier for the supplier.

</td></tr><tr><td>

Legal name

</td><td>

Legal name of the supplier that corresponds to its operating location.

</td></tr><tr><td>

ERP supplier code

</td><td>

Company code of the supplier in the ERP system.

</td></tr><tr><td>

Parent entity

</td><td>

Parent organization of the supplier.

</td></tr><tr><td>

Global company

</td><td>

Global company that the supplier is linked to.

</td></tr><tr><td>

Punchout

</td><td>

Whether the supplier is a third-party punchout.**Note:** This option is only available for Procurement Specialists using the Purchasing view.

</td></tr><tr><td>

Industry

</td><td>

Industry to which the supplier belongs.

</td></tr><tr><td>

Image

</td><td>

Image of the supplier’s logo.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the supplier.

</td></tr></tbody>
</table>4.  To add an image of the supplier’s logo, select **Select to add…**.

5.  Select the **Relationship Summary** tab and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Onboarded|Status of whether the supplier is onboarded into the ERP system. The options are **Yes** or **No**.|
    |Valid NDA|Status of whether the supplier has a valid non-disclosure agreement. The options are **Yes** or **No**.|
    |Valid risk assessment|Status of whether a valid risk assessment has been performed for the supplier. The options are **Yes** or **No**.|
    |Tiering assessment needed?|Whether a tiering assessment is required for the supplier.|
    |Customer number|Unique identifier for the organization to the supplier.|
    |On-boarded by|The person responsible for onboarding the supplier.|
    |On-boarded date|Onboarding date of the supplier.|
    |Off-boarded date|Termination date of the supplier from the organization.|
    |Relationship manager|Person responsible for managing the relationship with this supplier.|
    |Relationship status|Business relationship that is designated to the supplier. The options are **Strategic**, **Valued**, **Tactical**, or **Excluded**.|
    |Preferred|Whether the supplier is preferred. The options are **Yes** or **No**.|

6.  Select the **Contact Information** tab and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Street address|Street where the supplier is located.|
    |PO box number|Post office box number where the supplier correspondence and payments are made.|
    |City|City where the supplier is located.|
    |State/Province|State or province where the supplier is located.|
    |County/District|County or district where the supplier is located.|
    |Zip/Postal code|Zip code or postal code where the supplier is located.|
    |Country|Country where the supplier is located.|
    |Region|Region where the supplier is operating. Options are **AMS**, **APAC**, **EMEA**, or **LATAM**.|
    |Primary phone number|Phone number of the primary contact from the supplier side.|
    |Fax number|Number to which documents can be faxed to the supplier.|
    |Website|Website of the supplier.|

7.  Select the **Purchasing Automation** tab and fill in the fields.

<table id="table_uwl_13d_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Shipping time in days

</td><td>

Estimated number of days to ship products to the delivery location. For more information, see [Lead time calculations](../reference/lead-time-calculations.md).

</td></tr><tr><td>

Shipping estimates for products from this supplier \(percent of negotiated price\)

</td><td>

Default shipping estimate from the supplier.

</td></tr><tr><td>

Incoterm

</td><td>

Set of 11 internationally recognized rules that define the responsibilities of sellers and buyers. It specifies who is responsible for paying for and managing the shipment, insurance, documentation, customs clearance, and other logistical activities. Select one of these options:

 -   **Carriage and Insurance Paid to \(CIP\)**
-   **Carriage Paid to \(CPT\)**
-   **Cost and Freight \(CFR\)**
-   **Cost, Insurance, and Freight \(CIF\)**
-   **Delivered at Place \(DAP\)**
-   **Delivered at Terminal \(DAT\)**
-   **Delivered Duty Paid \(DDP\)**
-   **Ex Works \(EXW\)**
-   **Free Alongside Ship \(FAS\)**
-   **Free Carrier \(FCA\)**
-   **Free on Board \(FOB\)**


</td></tr><tr><td>

Goods shipped from

</td><td>

Location from where the supplier ships out the products.

</td></tr><tr><td>

Supplier delivers to

</td><td>

Approved shipping countries for the supplier.

</td></tr><tr><td>

Purchasing entities

</td><td>

Purchasing entities that are allowed to purchase from this supplier.

</td></tr><tr><td>

Legal entities

</td><td>

Legal entities that are allowed to buy from this supplier.

</td></tr></tbody>
</table>8.  Select the **Accounting Details** tab and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Payment term|Agreed time and conditions for paying the supplier.|
    |Tax jurisdiction|Taxation authority that imposes the taxes.|
    |Accepted purchasing currency|Currency value in which purchase orders for this supplier must be created.|
    |General ledger account|Accounts payable reconciliation account for this supplier.|

9.  Select **Submit**.


## What to do next

-   Use the related lists of the supplier form to view the supplier products and contracts that are associated with this supplier.
-   Add a supplier product. For more information, see [Add a supplier product](add-supplier-product.md).

**Parent Topic:**[Setting up primary data for ShoppingHub](../reference/set-up-master-data-shopping-hub.md)

