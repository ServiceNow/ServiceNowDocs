---
title: Validate product offerings and specifications
description: Move a product offering or specification through the In Test and Staged statuses to validate it before you publish it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/move-offering-spec-states.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Validating product offerings, Specifications and product offerings, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Validate product offerings and specifications

Move a product offering or specification through the In Test and Staged statuses to validate it before you publish it.

## Before you begin

Extended life cycle states must be turned on. For more information, see [Enable extended life cycle states for product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/enable-extended-lifecycle-states.md).

Role required: sn\_prd\_pm.product\_catalog\_admin

## About this task

Only the actions available for a record's current status appear on the record.

## Procedure

1.  Navigate to **Workspaces** &gt; **CRM Workspace**.

2.  Select the List icon \[Omitted image "list-outline-24.svg"\] Alt text:.

3.  Navigate to the module you want to test.

    -   **Specifications** &gt; **Product Specification**
    -   **Specifications** &gt; **Service Specification**
    -   **Specifications** &gt; **Resource Specification**
    -   **Offerings** &gt; **Product Offerings**
4.  Select the product offering or specification record you want to test.

5.  Select the action for the status change that you want to make.

    |Action|Result|
    |------|------|
    |**__Ready for Test__**|Moves a Draft record to In Test. The record becomes read-only.|
    |**__Return to Draft__**|Moves an In Test record back to Draft so you can edit it again. This option is unavailable for records in the Staged state.|
    |**__Ready for Staging__**|Moves an In Test record to Staged. Blocked if anything in the record's hierarchy has a rejected approval.|
    |**__Publish__**|Moves the staged record to Published state.|
    |**__Retire__**|Retires a staged or published record. A staged record can be retired directly without publishing it first. This action is irreversible.|


**Parent Topic:**[Validating product offerings before publishing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/extended-product-lifecycle-states.md)

**Related topics**  


[b03a1337caec0f2c07d23b948e7198add0b33a29.dita](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/channel-specific-availability.md)

