---
title: Remove a configurable product from a solution
description: Remove a child configuration from a solution by changing the condition of its configurable product action to false.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/remove-child-configuration.html
release: australia
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 1
keywords: [remove configurable product, remove child configuration, solution, buyer]
breadcrumb: [Using CPQ, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Remove a configurable product from a solution

Remove a child configuration from a solution by changing the condition of its configurable product action to false.

## Before you begin

You are in an active solution session with at least one child configuration.

Role required: none

## Procedure

1.  Navigate to the parent configuration that contains the configurable product action you want to deactivate.

    For steps on navigating between configurations, see [Navigate within a solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/navigate-solution.md).

2.  Change the field values or selections so that the condition for the configurable product action evaluates to false.

3.  Verify that the child configuration no longer appears in the solution navigation sidebar.


## Result

The child configuration is removed from the session, along with all field values, products, and any nested child configurations within it. Removing a child configuration is permanent within the session. All changes made in that configuration — including nested children — are discarded.

## What to do next

After removing a child configuration:

-   To confirm that the products from that configuration are no longer in the BOM, see [View the solution bill of materials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-solution-bom.md).
-   To add a different child configuration in its place, trigger the appropriate configurable product action. See [Add configurable products to a solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/add-configurable-products-solution.md).

**Parent Topic:**[Using CPQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-using.md)

**Related topics**  


[Navigate within a solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/navigate-solution.md)

[View the solution bill of materials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-solution-bom.md)

