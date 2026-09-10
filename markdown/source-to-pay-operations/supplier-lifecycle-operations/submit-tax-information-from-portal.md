---
title: Update tax information using the supplier catalog
description: Suppliers can submit tax information change requests through the supplier portal to update or add tax details for their organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/supplier-lifecycle-operations/submit-tax-information-from-portal.html
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 2
keywords: [supplier portal, tax information, supplier self-service]
breadcrumb: [Raising requests, Using Supplier Collaboration Portal, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Update tax information using the supplier catalog

Suppliers can submit tax information change requests through the supplier portal to update or add tax details for their organization.

## Before you begin

Role required: sn\_slm.contact

## About this task

Suppliers can add new tax information or update existing tax details. The system validates that only one tax record exists per country for each supplier.

## Procedure

1.  Navigate to the Supplier Collaboration Portal home page by accessing your instance URL and adding a /supplier suffix.

    For example, `https://example.com/supplier`.

2.  In the portal header, select **Raise a request**.

3.  Select **Update tax details**.

4.  To add new tax information, fill in the form.

    |Field|Description|
    |-----|-----------|
    |Supplier|Automatically populated with your supplier organization|
    |New or existing supplier tax ID|Whether tax details have to be added or updated for new or existing Tax ID|
    |Existing tax ID|Existing tax identification number \(appears only if Add new tax ID option is selected|
    |Supplier tax ID|Tax identification number to be updated|
    |Supplier tax type|Type of tax identifier|
    |Country|Country for which the tax information applies|
    |Active|Whether the Tax ID is active by default|

5.  Select the tax record from the displayed list to update existing tax information, and modify the required fields.

6.  Select **Submit**.

    The system validates that a tax record does not already exist for the same supplier and country combination. If a duplicate is detected, an error message appears prompting you to change the values.


## Result

After successful validation, a case is created and assigned to a supplier manager for review.

**Parent Topic:**[Raising requests from the Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/supp-catalog-req.md)

**Related topics**  


[Add or remove a supplier location using the supplier catalog]()

[Add a supplier contact using the supplier catalog]()

[Remove a supplier contact using the supplier catalog]()

[Ask a question using the supplier catalog]()

[Submit an idea using the supplier catalog]()

[Submit an issue using the supplier catalog]()

[Update banking details using the supplier catalog]()

[Update company profile using the supplier catalog]()

[Request elevated access]()

[Update default supplier]()

[Request something else using the supplier catalog]()

