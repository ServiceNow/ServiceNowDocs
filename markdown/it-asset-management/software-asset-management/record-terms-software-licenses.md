---
title: Create software models in Software Asset Management classic
description: Create a software model to add product details that are used to connect software rights you purchased with software installations discovered on your system.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Create software models in Software Asset Management classic

Create a software model to add product details that are used to connect software rights you purchased with software installations discovered on your system.

## Before you begin

Role required: sam\_user or model\_manager

## About this task

You can manually create a software model. However, you can leverage the Software Asset Management Content Service Library to automate the creation of software models through their relationship to software entitlements. While creating or importing a software entitlement, specifying a publisher part number automatically creates a software model \(if needed\) or links to an existing software model. You need to manually create a software model if a publisher part number is not available, a publisher part number does not exist in the Content Service Library, or if you are creating a software model for a custom product.

**Note:** If you have the model\_manager role, you can navigate to **Product Catalog** &gt; **Product Models** &gt; **Software Models** but cannot administer all aspects of software models.

View and track life cycle information of your product versions \(licensable, minor or build\) via product life cycles. Product life cycles are associated to software models. Product life cycles are based on attributes such as publisher, product, edition, edition condition, version, and version condition. The life cycle information is maintained in the Product Lifecycle \[sam\_sw\_product\_lifecycle\] and Custom Product Lifecycle \[sam\_custom\_sw\_product\_lifecycle\] tables.

You can view a detailed product life cycle report in the Software Asset Analytics dashboard and drill-down to the software installations. You can also manually create product life cycles and view product life cycles associated to a software model in the [Software Product Lifecycle related list](../reference/software-model-fields.md#section_uvx_mbq_l3b) in the Software Model form layout.

**Note:** Duplicate product life cycles can be created but in different domains.

You can view the life cycles for all the versions of the product on the software model form layout by clicking the **Show Product Lifecycles for all Versions** related link.

If you've installed the SAP publisher pack, see [Record publisher details for SAP](add-software-model-sap.md).

## Procedure

1.  Navigate to **Software Asset** &gt; **Licensing** &gt; **Software Models**.

2.  Select **New**.

3.  On the Software Model form, [fill in the details](../reference/software-model-fields.md) about the software publisher.

4.  Right-click the form header and select **Save**.

5.  Specify whether your software publisher is part of a suite.

    -   To designate your software model as a suite parent, select the [Suite Parents related list](../reference/software-model-fields.md#section_ln4_wyp_l3b) and add all software included with the suite.
    -   To designate your software model as a suite component, select the [Suite Components related list](../reference/software-model-fields.md#section_bdp_kmc_xhb) and add the parent suite.
    **Note:** If you've added a discovery map to your product details, predefined suites are used and suite components are created automatically for known suite parent.

6.  To enable self-service capabilities for the software that is associated with your software model, publish the software model to your service catalog.

    1.  Select the **Publish to Software Catalog** related link.

        The Publish &lt;*software-model*&gt; to Software Catalog dialog box opens.

    2.  On the dialog box, set the **Category** field to **Software**.

    3.  Select **OK**.

7.  To see discovery maps that have the match the software publisher and product fields of the software model, select the **Show Matching Discovery Models** related link.

8.  To view all the product lifecycles associated with your software model, select the [Software Product Lifecycles](../reference/software-model-fields.md#section_uvx_mbq_l3b).

    Select **New** to create a custom product life-cycle.

9.  To set the attribute value, select the [Metric Attributes related list](../reference/software-model-fields.md#section_zcb_j4z_4hb) and complete the form.

    When you add an attribute value, entitlements with this publisher information associated with them automatically have the **Metric Group** field populated. Based on the metric group, only license metrics related to the publisher are available.

10. To associate your software model with a vendor, select the [Vendor Catalog Item related list](https://www.servicenow.com/docs/access?context=t_CreateAVendorCatalogItem&version=australia&pubname=australia-it-service-management&ft:locale=en-US) and complete the form.

11. To specify the number of devices or users that are accessing the software, select the [Client Access related list](../reference/software-model-fields.md#section_yhc_y3q_l3b) and complete the form.

12. To create a new record for the software downgrade rights, select the [Downgrade Rights related list](../reference/software-model-fields.md#section_x5s_j4z_4hb) and complete the form.

    **Note:** If your software model has a discovery map associated with it and the discovery map has downgrade rights, the downgrade rights are populated automatically. Downgraded versions of the software appear in a hierarchical list. For more information, see [Downgrade Rights](../concept/downgrade-rights.md).

13. Select **Update**.


**Parent Topic:**[Using Software Asset Management classic](../concept/using-sam-classic.md)

**Related topics**  


[Supported software publisher licenses](../concept/sam-publisher-packs.md)

[Software models and Software entitlements](../concept/software-models-and-entitlements.md)

[Software model fields](../reference/software-model-fields.md)

