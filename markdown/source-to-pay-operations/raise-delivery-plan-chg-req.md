---
title: Raise a delivery plan change request
description: Submit a request in the Supplier Collaboration Portal header to create a purchase order exception.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Submit delivery plan change, Delivery plan change, New exception record, Raise an issue, purchase order exception]
breadcrumb: [Reporting delivery plan issues, Use, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Raise a delivery plan change request

Submit a request in the Supplier Collaboration Portal header to create a purchase order exception.

## Before you begin

Verify that the supplier is also present in the Supplier Contact \[sn\_slm\_contact\_m2m\_supplier\] table. This table stores information about supplier contacts and suppliers linked to them.

Role required: sn\_slm.contact

## Procedure

1.  Navigate to Supplier Collaboration Portal home page by accessing your instance URL and adding a `/supplier` suffix.

    For example, `https://example.com/supplier`.

2.  From the My Company drop-down list of suppliers associated with your profile, select the supplier.

3.  In the portal header, select **Raise a request**.

4.  Under the General category, select the **Delivery plan change** catalog item.

5.  On the Delivery plan change form, fill in the fields.

    For a description of the field values, see [Delivery plan change form](../reference/create-delivery-plan-change.md).

6.  Select **Submit**.


## Result

The application creates an exception and assigns it to the operational buyer.

**Parent Topic:**[Reporting delivery plan issues](../concept/reporting-delivery-plan-issues.md)

