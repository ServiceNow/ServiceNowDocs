---
title: Pre-authorization job details form
description: The pre-authorization job form enables you to enter the warranty, labor, and part details.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Repair form, Reference, Manufacturing Commercial Operations]
---

# Pre-authorization job details form

The pre-authorization job form enables you to enter the warranty, labor, and part details.

<table id="table_dhw_nkd_bhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="subhead" colspan="2">

Warranty

</td></tr><tr><td colspan="2">

**Note:** Fields under the Warranty section are displayed when you select the Warranty claim option type under Add claim jobs.

</td></tr><tr><td>

Casual part

</td><td>

Part number of the product that is repaired.

</td></tr><tr><td>

Repair action

</td><td>

Repair action type. Options are:-   Repair
-   Replacement
-   Software update

</td></tr><tr><td>

Issue description

</td><td>

Name of the product that has the issue.

</td></tr><tr><td>

Proposed repair details

</td><td>

Short description of the repair details.

</td></tr><tr><td class="subhead" colspan="2">

Parts

</td></tr><tr><td>

Part number

</td><td>

Part number that is repaired, replaced, or upgraded. It’s fetched from the product model.

</td></tr><tr><td>

Casual part replacement

</td><td>

Casual part replacement is enabled only if you select repair action as replacement or if remedy type contains replacement for recall claim job.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of assets that are repaired. Unit of measure is configurable. Available options are:-   Case
-   Pack
-   Carton
-   Kit
-   Each
-   Bundle
-   Box

</td></tr><tr><td>

Base amount

</td><td>

Base amount of the part. It is without tax.

</td></tr><tr><td>

Tax rate

</td><td>

Tax rate.

</td></tr><tr><td>

Claimed amount

</td><td>

Claimed amount. This amount is calculated based on the base amount, quantity, and tax rate.For example: `base amount * quantity + tax rate`.

</td></tr><tr><td class="subhead" colspan="2">

Labor

</td></tr><tr><td>

Labor code

</td><td>

Labor code. It’s the main data for implementation.

</td></tr><tr><td>

Duration

</td><td>

Time required to repair or replace the part or product. Unit of measure includes:-   Year
-   Hours
-   Month
-   Days

</td></tr><tr><td>

Base amount

</td><td>

Base amount of the labor work performed. It is without tax.

</td></tr><tr><td>

Tax rate

</td><td>

Tax rate.

</td></tr><tr><td>

Claimed amount

</td><td>

Claimed amount.This amount is calculated based on the base amount, quantity, and tax rate. For example: `base amount * quantity + tax rate`.

</td></tr><tr><td class="subhead" colspan="2">

External services

</td></tr><tr><td>

Description

</td><td>

Details of the external services taken for the repair or replacement of the part.

</td></tr><tr><td>

Base amount

</td><td>

Base amount of the external service taken. It is without tax.

</td></tr><tr><td>

Tax rate

</td><td>

The tax rate.

</td></tr><tr><td>

Claimed amount

</td><td>

Claimed amount. This amount is calculated based on the base amount, quantity, and tax rate. For example: `base amount * quantity + tax rate`.

</td></tr><tr><td class="Subhead" colspan="2">

Miscellaneous

</td></tr><tr><td>

Description

</td><td>

Details of the miscellaneous services.

</td></tr><tr><td>

Base amount

</td><td>

Base amount for any miscellaneous services.

</td></tr><tr><td>

Tax rate

</td><td>

Tax rate.

</td></tr><tr><td>

Claimed amount

</td><td>

Claimed amount. This amount is calculated based on the base amount, quantity, and tax rate. For example: `base amount * quantity + tax rate`.

</td></tr><tr><td>

Claimed amount

</td><td>

Total amount claimed for this job. It includes:-   Parts claimed amount
-   Labor claimed amount
-   External services claimed amount
-   Miscellaneous claimed amount

</td></tr><tr><td>

Attachments

</td><td>

Attachments that support your claims.

</td></tr><tr><td>

Pre-approval requested amount

</td><td>

Total amount claimed includes parts, labor, external services, and miscellaneous items.

</td></tr></tbody>
</table>**Parent Topic:**[Repair form](repair-form.md)

**Related topics**  


[Create a pre-authorization request](../task/mco-agents-create-pre-auth-request.md)

