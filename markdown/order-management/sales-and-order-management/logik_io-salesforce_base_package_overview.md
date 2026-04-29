---
title: CPQ and Salesforce base package overview
description: The CPQ and Salesforce base package lets the user use Salesforce Product2 records as configurable products in CPQ, launch the CPQ Admin from Salesforce, and integrate the two applications in other useful ways.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Capturing data from a configuration when amending a subscription contract, CPQ with other apps, Integrate, Sales and Order Management]
---

# CPQ and Salesforce base package overview

The CPQ and Salesforce base package lets the user use Salesforce Product2 records as configurable products in CPQ, launch the CPQ Admin from Salesforce, and integrate the two applications in other useful ways.

The base package provides the minimum components and configuration for CPQ interacting with Salesforce. This package allows the user to:

-   Enable Salesforce Product2 records to be a CPQ configurable product through custom fields added to the Product2 record. For detailed steps, see [Configurable products](configurable-products-explore.md).
-   Launch the CPQ Admin from Salesforce, from enabled Product2 records
-   Embed the CPQ configuration UI in other Salesforce pages or applications outside CPQ using Visualforce. See [Use case: Embed CPQ UI in a Salesforce VisualForce page](use_case_embed_logik_io_ui_in_salesforce_visualforce_page.md).
-   Access CPQ admin APIs using Salesforce tokens. For detailed steps, see [Admin APIs: Authentication using a Salesforce-connected app](admin-apis-authentication-via-salesforce-connected-app.md).

## Product2 integration

The base package includes the Logik Enabled checkbox and a link View CPQ Setup that will be populated with a link to the CPQ Admin page when the Logik Enabled checkbox is checked.

## Configuration line item field mapper

A flow is available that checks for user-created custom fields on the configuration line item \(LGK\_ConfigurationLineItem\_c\), and compares it to data in the Extended Information and Pricing Information fields on the record. If there are name matches, write the data from the Extended Information or Pricing Information to the custom fields.

Name comparisons ignore case sensitivity, and the "\_c" suffix on field names is optional. For example, both "StartDate" and "startDate\_c" in Extended Information or Pricing Information will be considered a match for a Salesforce field named "StartDate\_c". If the map contains the same name both with and without the "\_c" suffix, the Salesforce will save the value of the field with the suffix.

If the same field names exist in both Extended Information and Pricing Information, the value in Extended Information is written to the custom field.

## Configuration line items

LGK\_\_ConfigurationLineItem\_\_c stores the product data \(bill of materials\) that comes out of a configuration. \(See below for a complete list of fields.\)

The record stores the unique CPQ configuration ID that ties the data back to a specific CPQ configuration session and can be referenced in other flows or triggers in Salesforce.

Quote line fields can be populated with information from a CPQ configuration using records of this object. For additional information, see the following video: [Populate Quote Line Custom Fields from Logik](https://drive.google.com/file/d/1aojT9Pv0BceH2fLbUtEDmBmesn40YSto/view?usp=share_link)

CPQ writes the configuration line item objects when a CPQ configuration is saved. The setting in CPQ Admin must be enabled.

**Note:** CPQ writes these records into Salesforce, but does not read them. Any changes made to these records will not affect a CPQ configuration.

![Configuration line items](../images/cpq-fields-and-relationships-1.png)

## Configuration field data

LGK\_\_ConfigurationFieldData\_\_c stores the field values set in a configuration and contains the unique CPQ configuration ID. \(See below for a complete list of fields.\)

Creates records for every field from a configuration, even if it has a blank or null value.

Writes the configuration Field Data objects when a CPQ configuration is saved. The setting in CPQ Admin also needs to be enabled.

**Note:** CPQ writes these records into Salesforce, but does not read them. Any changes made to these records will not affect a CPQ configuration.

![Configuration line items](../images/cpq-fields-and-relationships-2.png)

## Configuration tenant

LGK\_\_ConfigurationTenant\_\_c controls aspects of the CPQ integration with Salesforce.

![Tenant screen](../images/cpq-logik-tenant.png)

A single record for org-wide defaults should be created and populated with the Administration URL and Runtime Configuration URL values of your CPQ instance.

For security reasons, the Runtime Client Token field is deprecated. The Skip CPQ Post Install Script checkbox disables product updates that run while installing CPQ's CPQ extension package.

