---
title: Create a purchase order confirmation in Supplier Collaboration Portal
description: Create purchase order confirmations to accept PO lines without modifications and assure the buyer of timely order fulfillment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/create-po-confirmation-in-supplier-portal.html
release: australia
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Managing purchase order confirmations, Use, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Create a purchase order confirmation in Supplier Collaboration Portal

Create purchase order confirmations to accept PO lines without modifications and assure the buyer of timely order fulfillment.

## Before you begin

Verify that the supplier is also present in the Supplier Contact \[sn\_slm\_contact\_m2m\_supplier\] table. This table stores information about supplier contacts and suppliers linked to them.

Role required: sn\_slm.contact

## Procedure

1.  Navigate to Supplier Collaboration Portal home page by accessing your instance URL and adding a `/supplier` suffix.

    For example, `https://example.com/supplier`.

2.  From the My Company drop-down list of suppliers associated with your profile, select the supplier.

3.  From the My Active items list, select the purchase orders count link.

4.  From the list of purchase orders, select one.

5.  On the purchase order form, select **Respond to lines**.

    All lines related to a PO are displayed, except those with active PO exceptions or those already confirmed.

6.  Select the lines you want to confirm and select **Continue to confirmation**.

7.  Review the lines and select **Submit confirmation**.


## Result

The status of each purchase order line changes from Draft to Confirmed after submission. Once a confirmation is submitted, it can't be edited or canceled and is also visible to the operational buyer.

**Parent Topic:**[Managing purchase order confirmations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/managing-po-confirmations.md)

