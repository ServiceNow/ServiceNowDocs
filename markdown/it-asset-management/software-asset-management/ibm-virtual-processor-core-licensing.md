---
title: IBM virtual processor core \(VPC\) licenses
description: If you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program, you can track and manage IBM VPC licenses. Alternatively, you can track and manage these licenses when you integrate with the IBM License Metric Tool \(ILMT\) or BigFix Inventory using version 2 of the integration APIs.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Supported IBM license types, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# IBM virtual processor core \(VPC\) licenses

If you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program, you can track and manage IBM VPC licenses. Alternatively, you can track and manage these licenses when you integrate with the IBM License Metric Tool \(ILMT\) or BigFix Inventory using version 2 of the integration APIs.

With these integrations, the publisher pack adds the Virtual Processor Core \(VPC\) license metric for IBM so that you can calculate licensing for this license type. For more details on Authorized SAM Provider \(ASP\) integrations, see [Authorized SAM Provider \(ASP\) integrations for IBM](ibm-asp-integration.md). For more details on ILMT and BigFix Inventory integrations, see [IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations](ibm-ilmt-bigfix-inventory-integration.md).

A virtual processor core \(VPC\) is a unit of measure that enables you to determine the licensing requirements for an IBM software product based on the number of cores that are available to or managed by that product. If you are licensing a virtual machine \(VM\), VPC is based on the number of virtual cores that are assigned to the VM. If you are licensing a physical host that is not partitioned for VMs, VPC is based on the number of processor cores on the host. Each VPC license requires one right for every core that is available to or managed by the associated IBM software product.

If you are integrating the IBM publisher pack with an ASP, the publisher pack supports both full capacity and sub-capacity VPC licensing. If you are integrating with ILMT or BigFix Inventory, the publisher pack supports only sub-capacity VPC licensing. With a full capacity VPC license, you must account for all processor cores on the physical host that is available to or managed by the IBM software product. With a sub-capacity VPC license, which is available only in virtual environments, you must account for only the virtual cores that are assigned to the VMs on which the IBM software product is installed and running.

You can gain visibility into how your VPC licenses are applied to your devices by using the **Usage Type** field in the [license workbench](sam-license-workbench.md). Use this information to determine whether your VPC licenses are applied to the full capacity or sub-capacity of each device. If you are integrating with an ASP, you can specify how a VPC license is applied to a device by navigating to **Workspaces** &gt; **Software Asset Workspace**. When the Software Asset Workspace launches, open the License operations view. From the left navigation menu of the License operations view, navigate to **IBM ASP Integration** &gt; **Device Settings** to modify the value of the corresponding **Usage Type** field. By default, the **Usage Type** field is automatically set to **Sub-capacity**.

For more details on the available device settings, see [Verify the meta data for your IBM hosts](../task/verify-ibm-device-meta-data.md).

**Parent Topic:**[Supported IBM license types](supported-ibm-license-types.md)

