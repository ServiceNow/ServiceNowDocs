---
title: Add configurable products to a solution
description: Trigger a configurable product action in a session to add a child configuration to the solution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/add-configurable-products-solution.html
release: australia
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 1
keywords: [add configurable product, child configuration, solution, buyer]
breadcrumb: [Using CPQ, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Add configurable products to a solution

Trigger a configurable product action in a session to add a child configuration to the solution.

## Before you begin

You are in an active configuration session for a solution-enabled product. For more information, see [Launch a solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/launch-solution.md).

Role required: none

## Procedure

1.  In the active configuration session, interact with the fields or selections that trigger a configurable product action rule.

2.  Verify that the solution navigation sidebar updates to include the new child configuration.


## Result

A child configuration is created for the configurable product defined in the triggered action. The child configuration uses the blueprint specified in that action. Any field mappings defined for the action are applied when the child configuration is created.

If the child configuration does not appear in the solution navigation sidebar, verify that the configurable product has a deployed blueprint associated with it.

## What to do next

After adding a configurable product:

-   To move to the new child configuration and complete its configuration, see [Navigate within a solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/navigate-solution.md).
-   To remove a child configuration that is no longer needed, see [Remove a configurable product from a solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/remove-child-configuration.md).

**Parent Topic:**[Using CPQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-using.md)

**Related topics**  


[Create a configurable product action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-configurable-product-action.md)

[Define field mappings for a solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/define-field-mappings-sol-config.md)

[Solution configuration limits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

