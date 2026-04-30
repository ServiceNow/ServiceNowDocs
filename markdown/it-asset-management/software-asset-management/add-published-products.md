---
title: Publish a specific set of your software products
description: Report only on the licensable software products that are part of the current implementation phase of Software Asset Management by publishing those software products. By publishing only a few software products initially, you can assess the initial progress and gradually increase the scope of the implementation.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage phase-wise Software Asset Management implementation, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Publish a specific set of your software products

Report only on the licensable software products that are part of the current implementation phase of Software Asset Management by publishing those software products. By publishing only a few software products initially, you can assess the initial progress and gradually increase the scope of the implementation.

## Before you begin

To be able to publish your software products, enable either the **com.snc.samp.manage.published.products** system property or the **com.snc.samp.manage.published.products** application property on your ServiceNow instance.

**Note:** The application property is domain-specific and available only on a ServiceNow instance that has domain separation activated for Software Asset Management. For more information, see [Domain separation and Software Asset Management](../concept/domain-separation-software-asset-management.md) and [Set the domain-specific property to publish your software products](set-domain-specific-publish.md).

Role required: sam\_admin

## About this task

**Note:** To view accurate data on the reports, you must [run software reconciliation](run-recon-workspace.md) whenever the following occur:

-   The system property **com.snc.samp.manage.published.products** is updated.
-   The software products are published or removed from the list of published software.

## Procedure

1.  Navigate to **All** &gt; **Software Asset Management Workspace** &gt; **License operations**.

2.  From the **SAM Implementation** list, select **Published products**.

3.  Select **Add**.

    **Note:** If the **Add** option isn’t available, make sure the **com.snc.samp.manage.published.products** property is enabled.

4.  In the **Add to published products** dialog box, select the licensable software products that you want to publish and select **Add**.

    **Note:**

    When you publish a software product that is part of a suite, messages with links that contain the details of the parent software suite and its child software components are shown. You can view the details and publish these software products if necessary.


## Result

-   The software products are added to the Published products list that is grouped by the publisher.
-   After you publish the products and run software reconciliation, you can view reports specific to only those published products in the License usage view and Software asset overview.

**Parent Topic:**[Manage phase-wise Software Asset Management implementation](../concept/manage-phasewise-imp-of-sam.md)

**Related topics**  


[Set the domain-specific property to publish your software products](set-domain-specific-publish.md)

[Remove published software products](remove-published-products.md)

