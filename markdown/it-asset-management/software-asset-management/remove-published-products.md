---
title: Remove published software products
description: Remove published software products that you no longer manage or report on as part of your Software Asset Management implementation.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage phase-wise Software Asset Management implementation, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Remove published software products

Remove published software products that you no longer manage or report on as part of your Software Asset Management implementation.

## Before you begin

To be able to remove software products from the list of published software products, make sure that either the **com.snc.samp.manage.published.products** system property or the **com.snc.samp.manage.published.products** application property is enabled on your ServiceNow instance.

**Note:** The application property is domain-specific and available only on a ServiceNow instance that has domain separation activated for Software Asset Management. For more information, see [Domain separation and Software Asset Management](../concept/domain-separation-software-asset-management.md) and [Set the domain-specific property to publish your software products](set-domain-specific-publish.md).

Role required: sam\_admin

## Procedure

1.  Navigate to **All** &gt; **Software Asset Workspace** &gt; **License operations**.

2.  From the **SAM Implementation** list, select **Published products**.

3.  Select the published software products that you want to remove from the list.

4.  Select **Remove**.


## Result

The software products that you removed are no longer shown in the Published products list.

**Parent Topic:**[Manage phase-wise Software Asset Management implementation](../concept/manage-phasewise-imp-of-sam.md)

**Related topics**  


[Set the domain-specific property to publish your software products](set-domain-specific-publish.md)

[Publish a specific set of your software products](add-published-products.md)

