---
title: Applying the CSDM guidelines to Hardware Asset Management
description: Hardware Asset Management manages \(contributes data to\) CSDM tables. Hardware Asset Management also uses data from CSDM tables that other applications generate. Several ServiceNow products, therefore, benefit from and add value to Hardware Asset Management.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Hardware Asset Management, IT Asset Management]
---

# Applying the CSDM guidelines to Hardware Asset Management

Hardware Asset Management manages \(contributes data to\) CSDM tables. Hardware Asset Management also uses data from CSDM tables that other applications generate. Several ServiceNow products, therefore, benefit from and add value to Hardware Asset Management.

## Implementing the CSDM data framework

The CSDM is the data framework that you follow when you set up ServiceNow products and applications. You adhere to the CSDM guidelines when you define the configuration items \(CIs\) and the relationships between CIs in the CMDB. This process makes sure that your data resides in the appropriate CMDB tables so that you get the maximum value from your ServiceNow AI Platform applications.

Using a CSDM standard and consistent set of terms and definitions helps to track the assets effectively through their life cycle transitions.

**Note:** To set up CSDM for Hardware Asset Management, see [Implementing the CSDM framework in stages](https://www.servicenow.com/docs/access?context=csdm-implementation-stages&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

## Tables adhering to the CSDM guidelines managed by Hardware Asset Management

1.  Product Model table \[cmdb\_model\]: The Asset Management application manages and contributes data to this table.
2.  Asset table \[alm\_asset\]: The Asset Management application manages this table containing asset details.

## CSDM table used by Hardware Asset Management

Configuration Item table \[cmdb\_ci\]: CMDB manages this table. The Hardware Asset Management application references configuration item \(CI\) data from this table.

## CSDM life cycle mappings for Hardware Asset Management

The base system contains the Life cycle mapping \[life\_cycle\_mapping\] table that stores the life cycle mapping values. A mapping record specifies how to map legacy life cycle field values of a class such as asset or product model, to the CSDM **Life cycle stage** and **Life cycle stage status** fields. You can get the mapping details of the Asset \[alm\_asset\] and the Product Model \[cmdb\_model\] tables in the Life cycle mapping table.

|Product Model Status field|CSDM Life cycle stage and Life cycle stage status fields|
|--------------------------|--------------------------------------------------------|
|Retired|End of Life \| Retired|
|Build|Design \| Build|
|Sold|End of Life \| Sold|
|In Production|Operational \| In Use|

|Asset State and Substate fields|CSDM Life cycle stage and Life cycle stage status fields|
|-------------------------------|--------------------------------------------------------|
|Retired \| RMA|End of Life \| RMA|
|Retired|End of Life \| Retired|
|Retired \| Vendor Credit|End of Life \| Vendor Credit|
|In stock \| Reserved|Inventory \| Reserved|
|In stock \| Legal hold|Inventory \| Legal Hold|
|In stock \| Pending transfer|Deploy \| Pending Transfer|
|Missing \| Lost|Missing \| Lost|
|In stock \| Pending resale|End of Operation \| Pending Resale|
|Retired \| Pending resale|End of Operation \| Pending Resale|
|Retired \| Lease return|End of Life \| Lease Return|
|Missing \| Stolen|Missing \| Stolen|
|Retired \| Donated|End of Life \| Donated|
|In transit \| Available|Deploy \| In Transit|
|In transit \| Pending donation|End of Operation \| In Transit|
|In transit|Deploy \| In transit|
|In transit \| Pre-allocated|Purchase \| Pre Allocated|
|Build|Design \| Build|
|In use|Operational \| In Use|
|In transit \| Pending resale|End of Operation \| In Transit|
|Retired \| Sold|End of life \| Sold|
|Retired \| Buy out|End of Life \| Buy Out|
|In transit \| Defective|Defective \| In transit|
|In stock|Inventory \| Available|
|Retired \| Disposed|End of Life \| Disposed|
|In stock \| Pending install|Deploy \| In Stock|
|In stock \| Pending evaluation|End of Operation \| Pending evaluation|
|In stock \| On hold|End of Operation \| On Hold|
|In stock \| Pending disposal|End of Operation \| Pending Disposal|
|On order|Purchase \| On Order|
|In use \| Pending fulfillment|Operational \| Pending Fulfillment|
|Retired \| Obsolete|End of Life \| Obsolete|
|In stock \| Test|Deploy \| Test|
|In maintenance|Operational \| In Maintenance|
|Retired \| Pending disposal|End of Operation \| Pending Disposal|
|In use \| End of support|Operational \| End of Support|
|In stock \| Pending repair|Inventory \| Pending Repair|
|In stock \| Defective|Defective \| In Stock|
|In stock \| Available|Inventory \| Available|
|In transit \| Pending disposal|End of Operation \| In Transit|
|In transit \| Pending install|Deploy \| In Transit|
|In stock \| Pre-allocated|Inventory \| Pre Allocated|
|In transit \| Reserved|Deploy \| Reserved|
|In stock \| Pending return|End of Operation \| Pending Return|
|In use \| Pending retirement|Operational \| Pending Retirement|
|In stock \| Quarantine|Inventory \| Quarantine|
|Missing|Missing \| Lost|
|In stock \| Pending certificate|End of Operation \| Pending Certificate|
|In stock \| Pending donation|End of Operation \| Pending Donation|

## CSDM life-cycle fields on the forms

The synchronization between the legacy fields and the CSDM life-cycle fields is bi-directional for both product model and asset. However, note the following points about the availability of the CSDM fields on the forms:

-   On the Model form, both **Life cycle stage** and **Life cycle stage status** fields are shown.
-   On the Asset form, the CSDM life-cycle fields aren't shown.

## Synchronization of CSDM life-cycle fields between asset and CI

If you have opted-in to CSDM in the releases before Xanadu, synchronization of the CSDM life-cycle fields between the asset and CI happens through the legacy fields. However, when you upgrade to Xanadu, you can also opt in to directly synchronize the CSDM life-cycle fields between the asset and CI.

From the Xanadu release onward, when you opt in to CSDM, the life-cycle fields are directly synchronized between the asset and CI.

For more details on synchronization of life-cycle fields, see [How life-cycle values for Asset, CI, and IBI are synced](https://www.servicenow.com/docs/access?context=cmdb-asset-CI-IBI-sync-options&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

