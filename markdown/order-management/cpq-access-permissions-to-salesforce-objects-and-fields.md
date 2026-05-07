---
title: Assigning access permissions to Salesforce objects and fields
description: Configure permissions for non-Admin users in Salesforce to enable configuration and reconfiguration with Logik.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Assigning access permissions to Salesforce objects and fields

Configure permissions for non-Admin users in Salesforce to enable configuration and reconfiguration with Logik.

To configure using CPQ, users need access to certain objects and fields in Salesforce. You can assign permissions by using permission sets or by navigating to Profiles &gt; Select Desired Profile &gt; Object Settings. Make sure that the user also has read or edit access for the product option itself \(in the Object Permissions section\).

Users must have read or edit access to the following objects. You can assign these permissions in the Field Permissions section.

## Configuration attribute

-   Id
-   Name
-   Target field
-   Product
-   Row order
-   Column order
-   Position \(edited\)

## Product feature

-   Id
-   Name
-   Option selection method
-   Configured SKU
-   Number
-   Min option count

## Product2

-   Configuration type
-   Has configuration attribute
-   Externally configurable

## QuoteLine

-   Configuration Id
-   Committed configuration id
-   BomData
-   Product
-   Incomplete
-   DynamicOptionId
-   Quantity
-   ListPrice
-   OptionLevel

## Product option

-   Configuration Id
-   Committed configuration id
-   BomData

## Field level security

When reconfiguring, make sure that the user has the correct field level security for both the configuration ID \(CI\) and the committed configuration ID \(CCI\) fields for the object from which they are entering the configuration. CPQ stores the previous CI in the CCI in case the user cancels their configuration and needs to revert the changes. These fields are part of the following objects:

-   Configuration line item
-   Quote line
-   Product option

To check whether the user has the correct permissions for both of these fields, go to Settings &gt; Object Manager &gt;\[Object\] &gt; Fields &amp; Relationships &gt; \[CI or CII\] &gt; Set Field-Level Security and confirm that the field-level security for the user's profile is set to Visible.

The full list of objects and fields contained in the Logik packages can be found by navigating to SFDC Setup and searching for "Installed Packages". "CPQ Managed Package" is used for parts of our SFDC Integration and custom objects, while CPQ Extension for Salesforce CPQ" contains the fields used in the standard user flow.

Selecting one of these packages and clicking **View Components** shows a list of SFDC objects and fields created by the package, along with their name, type, and parent object \(if any\). Specifically, the fields in "Logik Extension for Salesforce CPQ" are the fields a user must have access to in order to properly configure and reconfigure CPQ-enabled products in Salesforce CPQ.

