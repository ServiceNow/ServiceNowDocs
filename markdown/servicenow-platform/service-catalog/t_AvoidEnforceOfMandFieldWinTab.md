---
title: Avoid enforcement of a mandatory field
description: You can avoid enforcing a mandatory field within tabs.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Order guides, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Avoid enforcement of a mandatory field

You can avoid enforcing a mandatory field within tabs.

## Before you begin

Role required: admin

## About this task

By default, mandatory fields must be filled in before switching tabs in the **Choose Options** section of order guides.

In this example, if the customer attempts to select another tab without filling in the Street Address field, a warning prompt appears. The customer cannot switch tabs without entering this information.

To avoid this enforcement in all order guides:

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Properties**.

2.  Locate the property Validate mandatory fields when switching tabs in 'Choose Options' section of Order Guides \(glide.sc.guide.tab.validate\).

3.  Clear the Yes check box.

    If you make this change, mandatory fields are still mandatory, but the customer can switch between tabs before filling in the mandatory fields. Enforcement is then checked when the customer chooses to proceed to the next step.

    To avoid enforcement of mandatory fields altogether, use the Ignore Mandatory Evaluation check box within the relevant order guide rule.


**Parent Topic:**[Order guides](../concept/c_ServiceCatalogOrderGuides.md)

