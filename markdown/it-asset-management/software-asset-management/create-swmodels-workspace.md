---
title: Create a software model in the Software Asset Workspace
description: Create a software model in the Software Asset Workspace. Add product details that are used to connect software rights that you purchased with software installations that are discovered on your system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/create-swmodels-workspace.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create a software model in the Software Asset Workspace

Create a software model in the Software Asset Workspace. Add product details that are used to connect software rights that you purchased with software installations that are discovered on your system.

## Before you begin

Role required: sam\_user, sam\_admin, or model\_manager

## About this task

You can manually create a software model. However, you can leverage the Software Asset Management Content Service Library to automate the creation of software models through their relationship to software entitlements. While creating or importing a software entitlement, specifying a publisher part number automatically creates a software model \(if needed\) or links to an existing software model.

You must manually create a software model if a publisher part number isn’t available, or a publisher part number doesn’t exist in the Content Service Library, or if you are creating a software model for a custom product.

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace**.

2.  Select the **License operations** view.

3.  Under the Licensing section, select **software models**.

4.  Select **New**.

    \[Omitted image "create-sw-model-workspace.png"\] Alt text: Create a software model in workspace \[Omitted image ""\] Alt text:

5.  On the Create New Software Model page, fill in the details in the fields.

    See [Software model fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/software-model-fields.md).

6.  Select **Save**.

    After you save the software model, the **General**, **Suite Components**, **Suite Parents**, and the **Product Catalog** tabs appear on the page. You can now add details in these related tabs.

7.  Specify whether your software publisher is part of a suite.

    -   To designate your software model as a suite parent, select [Suite Parents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/software-model-fields.md) and add all software included with the suite.
    -   To designate your software model as a suite component, select [Suite Components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/software-model-fields.md) and add the parent suite.
    **Note:** If you have added a discovery map to your product details, predefined suites are used and suite components are created automatically for known suite parent.

8.  View all the product lifecycles associated with your software model by selecting [Software Product Lifecycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/software-model-fields.md).

    Select **New** to create a custom product life-cycle.

9.  View the override license cost for your entitlements by selecting [Override License Cost](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/software-model-fields.md).

10. Set the attribute value by selecting the [Metric Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/software-model-fields.md) and complete the form.

    When you add an attribute value, entitlements with this publisher information associated with them automatically have the **Metric Group** field populated. Based on the metric group, only license metrics related to the publisher are available.

11. Associate your software model with a vendor by selecting [Vendor Catalog Items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/t_CreateAVendorCatalogItem.md) and complete the form.

12. Specify the number of devices or users that are accessing the software by selecting [Client Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/software-model-fields.md) and complete the form.

13. To create a new record for the software downgrade rights, select [Downgrade Rights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/software-model-fields.md) and complete the form.

    **Note:** If your software model has a discovery map associated with it and the discovery map has downgrade rights, the downgrade rights are populated automatically. Downgraded versions of the software appear in a hierarchical list. For more information, see [Downgrade Rights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/downgrade-rights.md).

14. To allocate software licenses to all the members of an assignment group, select **Group Allocations** and complete the form.

    For more information about creating a group allocation record, see [Create group allocations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/create-group-allocations.md).

15. To enable self-service capabilities for the software that is associated with your software model, publish the software model to your service catalog.

    1.  Select **Publish to Software Catalog**.

        The Publish &lt;*software-model*&gt; to Software Catalog dialog box opens.

    2.  On the dialog box, set the **Category** field to **Software**.

    3.  Select **OK**.


**Parent Topic:**[Using Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/using-sam-workspace.md)

