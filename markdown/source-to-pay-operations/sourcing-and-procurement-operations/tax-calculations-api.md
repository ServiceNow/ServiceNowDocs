---
title: Tax calculation API
description: A tax calculation API is created to provide specific parameters to a tax calculator engine, SAP in this case.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Tax calculations, Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Tax calculation API

A tax calculation API is created to provide specific parameters to a tax calculator engine, SAP in this case.

The following parameters are to be used in a tax calculation generic API:

-   Cart line:
    -   Delivery location \(from the checkout cart line\)
    -   System date
    -   Purchase quantity \(from the checkout cart line\)
    -   Total line amount \(from the checkout cart line\)
    -   Currency \(from the **Fx Currency** field in the cart line\)
-   Supplier record:
    -   Street address, City, State, County, Zip, Country, Region \(from the vendor's supplier record\)
    -   Legal name \(from the vendor's supplier record\)
-   Supplier product record: Model category \(from the product model\)
-   Product model: Unit \(from the cart line\)

A staging table is also created that includes the following output parameters for the API:

-   Tax amount
-   Tax jurisdiction
-   Tax type/description
-   Tax percentage

**Parent Topic:**[Tax calculations](tax-calculations.md)

