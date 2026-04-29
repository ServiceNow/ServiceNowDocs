---
title: Configure the billing card variables
description: Configure the variables in the billing card.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure variables, Setup, Configure, Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Configure the billing card variables

Configure the variables in the billing card.

## Before you begin

Role required: sn\_telecom\_c360.admin

## Procedure

1.  Navigate to **All** &gt; **Telecom Customer 360** &gt; **Guided Setup** and select **Get Started**.

2.  Select **360 Cards** &gt; **Billings**.

3.  Modify the following variables.

    |Variable|Description|
    |--------|-----------|
    |Billing account table|The table from which the billing accounts are to be retrieved. The default is `sn_billing_account_billing_account`.|
    |Billing account table query|Query condition that filters the billing account table to accounts associated with the current context record.|
    |Billing account dropdown field|The field from the billing account table to use as the account label in the drop down filter.|
    |Invoice table|Based on the selected billing account, the table from which the invoices are to be retrieved.|
    |Invoice case table query|Query condition that filters the list of invoices for the selected billing account.|
    |Invoice header field|The field from the invoice table used to display the header label for each invoice row.|
    |Invoice fields|The fields to be displayed for each billing invoice. Default includes invoice number, invoice date, due date, and payment date.|
    |Invoice search field|The search criteria to be used to filter the list of billing accounts to be displayed.|


**Parent Topic:**[Configure the Telecommunications Customer 360 variables](../concept/c360-configure-variables.md)

**Related topics**  


[Billing card](../concept/c360-billing-card.md)

