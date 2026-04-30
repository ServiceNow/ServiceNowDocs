---
title: Create software models in workspace
description: Create a software model in the Software Asset Workspace to add product details that are used to connect software rights you purchased with software installations discovered on your system.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create software models in workspace

Create a software model in the Software Asset Workspace to add product details that are used to connect software rights you purchased with software installations discovered on your system.

## Before you begin

Role required: sam\_user, sam\_admin, or model\_manager

## About this task

You can manually create a software model. However, you can leverage the Software Asset Management Content Service Library to automate the creation of software models through their relationship to software entitlements. While creating or importing a software entitlement, specifying a publisher part number automatically creates a software model \(if needed\) or links to an existing software model. You need to manually create a software model if a publisher part number is not available, a publisher part number does not exist in the Content Service Library, or if you are creating a software model for a custom product.

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace**.

2.  Select **License operations** view on the left hand bar.

3.  Under **Licensing**, select **software models**.

4.  Select **New**.

    ![Create a software model in workspace](../image/create-sw-model-workspace.png) ![]()

5.  On the Create New Software Model page, fill in the details in the fields.

    See [Software model fields](../reference/software-model-fields.md).

6.  Select **Save**.

    After you save the software model, the **General**, **Suite Components**, **Suite Parents**, and the **Product Catalog** tabs appear on the page. You can now add details in these related tabs.

7.  Specify whether your software publisher is part of a suite.

    -   To designate your software model as a suite parent, click [Suite Parents](../reference/software-model-fields.md#section_ln4_wyp_l3b) and add all software included with the suite.
    -   To designate your software model as a suite component, click [Suite Components](../reference/software-model-fields.md#section_bdp_kmc_xhb) and add the parent suite.
    **Note:** If you've added a discovery map to your product details, predefined suites are used and suite components are created automatically for known suite parent.

8.  To view all the product lifecycles associated with your software model, select [Software Product Lifecycle](../reference/software-model-fields.md#section_uvx_mbq_l3b).

    Select **New** to create a custom product life-cycle.

9.  To view the override license cost for your entitlements, select [Override License Cost](../reference/software-model-fields.md#section_acq_cgl_4jb).

10. To set the attribute value, select the [Metric Attributes](../reference/software-model-fields.md#section_zcb_j4z_4hb) and complete the form.

    When you add an attribute value, entitlements with this publisher information associated with them automatically have the **Metric Group** field populated. Based on the metric group, only license metrics related to the publisher are available.

11. To associate your software model with a vendor, select [Vendor Catalog Items](https://www.servicenow.com/docs/access?context=t_CreateAVendorCatalogItem&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) and complete the form.

12. To specify the number of devices or users that are accessing the software, select [Client Access](../reference/software-model-fields.md#section_yhc_y3q_l3b) and complete the form.

13. To create a new record for the software downgrade rights, click [Downgrade Rights](../reference/software-model-fields.md#section_x5s_j4z_4hb) and complete the form.

    **Note:** If your software model has a discovery map associated with it and the discovery map has downgrade rights, the downgrade rights are populated automatically. Downgraded versions of the software appear in a hierarchical list. For more information, see [Downgrade Rights](../concept/downgrade-rights.md).

14. To enable self-service capabilities for the software that is associated with your software model, publish the software model to your service catalog.

    1.  Select **Publish to Software Catalog**.

        The Publish &lt;*software-model*&gt; to Software Catalog dialog box opens.

    2.  On the dialog box, set the **Category** field to **Software**.

    3.  Select **OK**.


**Parent Topic:**[Configuring Software Asset Workspace](../concept/Config-sam-workspace.md)

