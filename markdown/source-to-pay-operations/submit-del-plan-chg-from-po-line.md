---
title: Submit a delivery plan change request from a purchase order line
description: Submit a delivery plan change request directly from a purchase order line in the Supplier Collaboration Portal.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Submit delivery plan change, Delivery plan change, New exception record, Raise an issue, Purchase order exception, Purchase order exception from PO line]
breadcrumb: [Reporting delivery plan issues, Use, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Submit a delivery plan change request from a purchase order line

Submit a delivery plan change request directly from a purchase order line in the Supplier Collaboration Portal.

## Before you begin

Verify that the supplier is also present in the Supplier Contact \[sn\_slm\_contact\_m2m\_supplier\] table. This table stores information about supplier contacts and suppliers linked to them.

Role required: sn\_slm.contact

## Procedure

1.  Navigate to Supplier Collaboration Portal home page by accessing your instance URL and adding a `/supplier` suffix.

    For example, `https://example.com/supplier`.

2.  From the My Company drop-down list of suppliers associated with your profile, select the supplier.

3.  From the My Active items list, select the purchase order lines count link.

4.  From the list of purchase order lines, select a line.

5.  On the purchase order line form, select **Raise an issue**.

    You can raise an exception only for your assigned purchase order line items that have a requested delivery date in the future, and where the state isn’t Closed.

6.  Select **Delivery plan change** as the exception type, and select **Submit**.

7.  On the Delivery plan change form, fill in the fields.

    For a description of the field values, see [Delivery plan change form](../reference/create-delivery-plan-change.md).

8.  Select **Submit**.


## Result

The application creates an exception and assigns it to the operational buyer.

**Parent Topic:**[Reporting delivery plan issues](../concept/reporting-delivery-plan-issues.md)

