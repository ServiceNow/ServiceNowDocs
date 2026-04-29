---
title: Assigning non-Admin user permissions for CPQ in Salesforce
description: You need to apply certain user permissions in Salesforce in order to use CPQ properly.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Assigning non-Admin user permissions for CPQ in Salesforce

You need to apply certain user permissions in Salesforce in order to use CPQ properly.

To use CPQ, users need access to certain objects and fields in Salesforce. These can be assigned using permission sets or by going to Profiles &gt; Select Desired Profile &gt; Object Settings. Users need read/edit access in the Field Permissions section to the following objects:

For Configuration Attribute:

-   Id
-   Name
-   Target Field Product
-   Row Order
-   Column Order
-   Position \(edited\)

For Product Feature:

-   Id
-   Name
-   Option Selection Method Configured SKU
-   Number
-   Min Option Count
-   Position \(edited\)

For Product2:

-   Configuration Type
-   Has Configuration Attribute Externally Configurable

For QuoteLine:

-   Configuration Id
-   Committed Configuration Id BomData
-   Product
-   Incomplete
-   DynamicOptionId Quantity
-   ListPrice
-   OptionLevel

For Product Option:

-   Configuration Id
-   Committed Configuration Id Bom Data

**Note:** Users will also need read/edit access in Object Permissions for the Product Option itself.

For issues specifically with reconfiguration, make sure that the user has the correct field level security for both the “Configuration Id” \(CI\) AND the “Committed Configuration Id” \(CCI\) fields from the object from which they are entering the configuration. We store the previous CI in the CCI in case the user cancels from their configuration and needs to revert their changes. These fields are part of the following objects:

-   Configuration Line Item Quote Line
-   Product Option

To check whether the user has the necessary permissions for these fields, go to Settings &gt; Object Manager &gt; \[Object\] &gt; Fields &amp; Relationships &gt; \[Committed Configuration ID/Configuration ID\] &gt; Set Field-Level Security and check whether the "Visible" checkbox is checked for Field-Level Security for Profile of the user.

![Product Options](../images/cpq-product-option-page.png)

The full list of objects and fields contained in the CPQ packages can be found by navigating to SFDC Setup and searching for "Installed Packages". "CPQ Managed Package" is used for parts of our SFDC Integration and custom objects, while CPQ Extension for Salesforce CPQ" contains the fields used in the standard user flow.

Selecting one of these packages and clicking "View Components" will show a list of SFDC objects and fields created by that package along with their name, type, and parent object \(if any\). Specifically, the fields in **Logik Extension for Salesforce CPQ** are the fields a user will need to have access to in order to properly configure and reconfigure CPQ - enabled products in Salesforce CPQ.

