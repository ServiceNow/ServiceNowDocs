---
title: Part requirement form
description: Create a part requirement to include fields for part model, required quantity, reserved quantity, and delivery status for a work order task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-part-requirement-form.html
release: australia
topic_type: reference
last_updated: "2026-04-20"
reading_time_minutes: 1
breadcrumb: [Quality issue management form, Reference, Manufacturing Commercial Operations]
---

# Part requirement form

Create a part requirement to include fields for part model, required quantity, reserved quantity, and delivery status for a work order task.

|Field|Description|
|-----|-----------|
|Number|Auto-generated number for the part requirement.|
|Service order task|Number assigned to the work order task.|
|Model|Description of the part model needed to complete the work order task.|
|Required by date|Date by which all parts should be delivered. The date is filled in automatically based on the task's expected travel start time. If necessary, change the date manually.|
|Required quantity|Total quantity necessary to complete the part requirement. This field becomes read-only when the full number of required parts has been sourced.|
|Reserved quantity|Total quantity that has been sourced already.|
|Sourced|Indicator for whether the required quantity for this part requirement has been reserved and transfer requested from one stockroom to another.|
|Delivered|Indicator for whether the transfer order lines under this part requirement have been delivered or not.|
|Short description|Contents of the Short description field from the parent work order. If the work order was created from an incident, problem, or change request, the short description of the part requirement is inherited from that record. If the work order was created automatically from a , the short description is from model template. This field is not visible by default.|
|Mandatory|Option to indicate if the part is mandatory to perform the work order task.|

**Parent Topic:**[Quality issue management form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-qim-form.md)

