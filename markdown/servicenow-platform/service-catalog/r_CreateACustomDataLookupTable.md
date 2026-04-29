---
title: Custom data lookup
description: You can create a custom table to store lookup data.Creating a catalog data lookup is similar to creating a normal, custom data lookup except when creating the catalog data lookup definition record.If the custom data lookup definition rules are not behaving as expected, check for certain conditions.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service catalog data lookup, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Custom data lookup

You can create a custom table to store lookup data.

The custom table must extend the Data Lookup Matcher Rules \[dl\_matcher\] table.

For example, you can create a Server Offering Lookups table. It stores information about matcher offerings \(bronze, silver, and gold\) and associated setter values \(memory and disk space\) for each matcher offering.

**Parent Topic:**[Service catalog data lookup](../concept/c_ServiceCatalogDataLookup.md)

## Create a custom data lookup

Creating a catalog data lookup is similar to creating a normal, custom data lookup except when creating the catalog data lookup definition record.

1.  Create a custom data lookup table. It must extend the Data Lookup Matcher Rules `[dl_matcher]` table.
2.  Add data lookup values to the data lookup table.
3.  Create a catalog data lookup definition record.
4.  \(Optional\) Create a data lookup module.

## Troubleshooting

If the custom data lookup definition rules are not behaving as expected, check for certain conditions.

If the custom data lookup definition rules are not behaving as expected, check for the following conditions:

-   Ensure that the matcher variable is not read-only. Since users cannot change read-only variables, there cannot be an on form change event for read-only variables.
-   Ensure that the data in the matcher table is correct.
-   If the lookup requires an exact match, verify that there is a matcher table row for each possible combination \(including blank values\). The lookup fails if it cannot find a matching value.
-   If the variable is an option or check box, it always has a value, so you must select **Always replace**.
-   Verify that you have not created a recursive rule, such as:

    If Variable A = 1, then Variable B =2. If Variable B = 2, then Variable A = 2.


