---
title: Modify a non-disclosure agreement legal request
description: As a requester, modify the legal request for a non-disclosure agreement \(NDA\).
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Non-disclosure agreement requests, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Modify a non-disclosure agreement legal request

As a requester, modify the legal request for a non-disclosure agreement \(NDA\).

## Before you begin

Role required:

-   sn\_lg\_ops.legal\_user and sn\_cm\_core.contract\_user

## About this task

Note the following:

-   You can modify a request until it is in the Draft or Work in progress state.
-   You can’t modify the **Signature type** field.

## Procedure

1.  Open an NDA legal request.

<table id="choicetable_vvd_bng_hxb"><thead><tr><th align="left" id="d711782e105">

Method

</th><th align="left" id="d711782e108">

Actions

</th></tr></thead><tbody><tr><td id="d711782e114">

**__Employee Center__**

</td><td>

1.  Navigate to **All** &gt; **Employee Center**
2.  Select **My Requests** from the header.


</td></tr><tr><td id="d711782e144">

**__Legal Service Portal__**

</td><td>

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Service Portal**
2.  Select **My Requests** from the header.


</td></tr></tbody>
</table>2.  Select the request that you want to edit.

3.  On the request page, from the Actions menu, select **Edit Request**.

4.  Edit the fields that you want to modify.

5.  Select **Save** to update the record.


## Result

-   Based on the change in values in the request form, the contract document is updated as follows:
    -   The correct contract template is used based on contract template rules. For example, The contract template rules can be defined for specific countries. If a change is made in the Country value, the contract document is updated per the contract template defined for the updated value of the country.
    -   Metadata and signatory information is replaced with data from the modified request.
    -   Content is inserted in the clauses in the contract document per the clause variation rules.
-   A new document revision is created and the file name is appended with the version number.
-   The Contract status is marked as Ready revision.

**Parent Topic:**[Non-disclosure agreement requests](../concept/snlc-request-nda-1.md)

