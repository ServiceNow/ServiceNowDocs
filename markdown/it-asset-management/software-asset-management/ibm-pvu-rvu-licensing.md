---
title: IBM processor value unit \(PVU\) and resource value unit \(RVU\) licenses
description: If you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program, you can track and manage IBM PVU and RVU licenses. Alternatively, you can track and manage these licenses when you integrate with the IBM License Metric Tool \(ILMT\) or BigFix Inventory using version 1 or 2 of the integration APIs.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Supported IBM license types, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# IBM processor value unit \(PVU\) and resource value unit \(RVU\) licenses

If you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program, you can track and manage IBM PVU and RVU licenses. Alternatively, you can track and manage these licenses when you integrate with the IBM License Metric Tool \(ILMT\) or BigFix Inventory using version 1 or 2 of the integration APIs.

With these integrations, the publisher pack adds the Processor Value Unit \(PVU\) and Resource Value Unit \(RVU\) license metrics for IBM so that you can calculate licensing for these license types. For more details on Authorized SAM Provider \(ASP\) integrations, see [Authorized SAM Provider \(ASP\) integrations for IBM](ibm-asp-integration.md). For more details on ILMT and BigFix Inventory integrations, see [IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations](ibm-ilmt-bigfix-inventory-integration.md).

**Note:** IBM PVU and RVU licensing is supported in both physical and virtualized environments.

## Processor value unit \(PVU\) licensing

A processor value unit \(PVU\) is a unit of measure that enables you to determine the licensing requirements for an IBM software product based on the processor technology that is used in your physical hardware environment. Each processor technology is assigned a PVUs per Core value based on the processor vendor, processor name, and model number. You can determine the number of rights that are required for a PVU license by multiplying the appropriate PVUs per Core value by the number of activated processor cores in the physical hardware environment that is available to or managed by your IBM software product.

The IBM publisher pack supports both full capacity and sub-capacity PVU licensing. If you are using a full capacity PVU license, you must account for all activated processor cores in the physical hardware environment that is available to or managed by the IBM software product. If you are using a sub-capacity PVU license, you must account for only the specific activated processor cores that are available to or managed by the IBM software product, as defined in [Virtualization Capacity License Counting Rules](https://www.ibm.com/software/passportadvantage/Counting_Software_licenses_using_specific_virtualization_technologies.html).

You can gain visibility into how your PVU licenses are applied to your devices by using the **Usage Type** field in the [license workbench](sam-license-workbench.md). Use this information to determine whether your PVU licenses are applied to the full capacity or sub-capacity of each device. Depending on the type of IBM integration that you are using, specify how a PVU license is applied to a device using one of the following options:

-   If you are integrating the IBM publisher pack with the IBM License Metric Tool \(ILMT\) or BigFix Inventory, navigate to **Integration - ILMT/BigFix Inventory** &gt; **Import Set Data** &gt; **IBM License Metric Peak Usage** to modify the value of the corresponding **Usage Type** field in the IBM Peak Consumption \[samp\_ilmt\_sw\_install\] table. By default, the **Usage Type** field for devices on the IBM Peak Consumption \[samp\_ilmt\_sw\_install\] table is automatically set to **Sub-capacity**. However, the **Usage Type** field for devices with allocations in your full capacity PVU entitlements is automatically set to **Full capacity** instead.

    For more details on ILMT and BigFix Inventory, see [IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations](ibm-ilmt-bigfix-inventory-integration.md).

-   If you are integrating the IBM publisher pack with an Authorized SAM Provider \(ASP\), navigate to **Workspaces** &gt; **Software Asset Workspace**. When the Software Asset Workspace launches, open the License operations view. From the left navigation menu of the License operations view, navigate to **IBM ASP Integration** &gt; **Device Settings** to modify the value of the corresponding **Usage Type** field. By default, the **Usage Type** field is automatically set to **Sub-capacity**. However, the **Usage Type** field for devices with allocations in your full capacity PVU entitlements is automatically set to **Full capacity** instead.

    For more details on the available device settings, see [Verify the meta data for your IBM hosts](../task/verify-ibm-device-meta-data.md).

    For more details on ASPs, see [Authorized SAM Provider \(ASP\) integrations for IBM](ibm-asp-integration.md).


Refer to [Processor Value Units \(PVU\)](https://www.ibm.com/software/passportadvantage/pvu_licensing_for_customers.html) for more information on IBM PVU licensing, including the complete list of supported processor technologies and corresponding PVUs per Core values.

## Resource value unit \(RVU\) licensing

A resource value unit \(RVU\) is a unit of measure that enables you to determine the licensing requirements for an IBM software product based on the number of activated processor cores that are available to or managed by that product. The number of activated processor cores corresponds directly with an RVU tier number and factor value.

|Number of Activated Processor Cores|Tier|Factor|
|-----------------------------------|----|------|
|0 to 2,500|1|1.00|
|2,501 to 10,000|2|0.80|
|10,001 to 50,000|3|0.60|
|50,001 to 150,000|4|0.40|
|150,001 and above|5|0.20|

You can determine the number of rights that are required for an RVU license by using a step function based on these RVU tiers. First, you must divide the total number of activated processor cores into tiers based on the [RVU tiers and factors table](ibm-pvu-rvu-licensing.md#table_owy_slv_4pb). Since RVU licensing is calculated at the product level and not the individual device level, you must account for all devices that the product is installed on when determining the total number of activated processor cores that must be licensed. Then, you must multiply the number of activated processor cores within each tier by the corresponding factor values. Finally, you must add the resulting numbers together to determine the total number of rights that are required for the RVU license.

**Important:** If you do not have enough rights to license all activated processor cores across all devices, none of the devices are licensed and the product is marked as Not Compliant.

For example, a product has access to a total of 150,000 activated processor cores across 100 devices. The total number of rights that are required for the RVU license is 72,500, based on the following calculations:

<table id="table_zbt_s4z_2qb"><thead><tr><th>

Tier

</th><th>

Number of Activated Processor Cores within the Tier

</th><th>

Factor

</th><th>

Number of Rights Required

</th></tr></thead><tbody><tr><td>

1 \(0 to 2,500 activated processor cores\)

</td><td>

2,500

</td><td>

1.00

</td><td>

2,500 x 1.00 = 2,500

</td></tr><tr><td>

2 \(2,501 to 10,000 activated processor cores\)

</td><td>

7,500

</td><td>

0.80

</td><td>

7,500 x 0.80 = 6,000

</td></tr><tr><td>

3 \(10,001 to 50,000 activated processor cores\)

</td><td>

40,000

</td><td>

0.60

</td><td>

40,000 x 0.60 = 24,000

</td></tr><tr><td>

4 \(50,001 to 150,000 activated processor cores\)

</td><td>

100,000

</td><td>

0.40

</td><td>

100,000 x 0.40 = 40,000

</td></tr><tr><td>

n/a

</td><td>

150,000 total

</td><td>

n/a

</td><td>

2,500 + 6,000 + 24,000 + 40,000 = 72,500 total

</td></tr></tbody>
</table>**Note:** The number of rights that are consumed for RVU licenses is reported differently from the number of rights that are consumed for PVU licenses. For PVU licenses, this number is reported at the individual device level. For RVU licenses, this number is reported at the product level.

Refer to [Resource value unit \(RVU MAPC\)](https://www.ibm.com/docs/en/license-metric-tool?topic=metrics-resource-value-unit-rvu-mapc) for more information on IBM RVU tiers.

The IBM publisher pack supports both full capacity and sub-capacity RVU licensing. If you are using a full capacity RVU license, you must account for all activated processor cores in the physical hardware environment that is available to or managed by the IBM software product. If you are using a sub-capacity RVU license, which is available only in virtualized environments, you must account for only the activated processor cores that are used by the virtual machines \(VMs\) on which the IBM software product is installed.

You can gain visibility into how your RVU licenses are applied to your devices by using the **Usage Type** field in the [license workbench](sam-license-workbench.md). Use this information to determine whether your RVU licenses are applied to the full capacity or sub-capacity of each device. Depending on the type of IBM integration that you are using, specify how an RVU license is applied to a device using one of the following options:

-   If you are integrating the IBM publisher pack with the IBM License Metric Tool \(ILMT\) or BigFix Inventory, navigate to **Integration - ILMT/BigFix Inventory** &gt; **Import Set Data** &gt; **IBM License Metric Peak Usage** to modify the value of the corresponding **Usage Type** field in the IBM Peak Consumption \[samp\_ilmt\_sw\_install\] table. By default, the **Usage Type** field for devices on the IBM Peak Consumption \[samp\_ilmt\_sw\_install\] table is automatically set to **Sub-capacity**.

    For more details on ILMT and BigFix Inventory, see [IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations](ibm-ilmt-bigfix-inventory-integration.md).

-   If you are integrating the IBM publisher pack with an Authorized SAM Provider \(ASP\), such as Anglepoint, navigate to **Workspaces** &gt; **Software Asset Workspace**. When the Software Asset Workspace launches, open the License operations view. From the left navigation menu of the License operations view, navigate to **IBM ASP Integration** &gt; **Device settings** to modify the value of the corresponding **Usage Type** field. By default, the **Usage Type** field is automatically set to **Sub-capacity**.

    For more details on the available device settings, see [Verify the meta data for your IBM hosts](../task/verify-ibm-device-meta-data.md).

    For more details on ASPs, see [Authorized SAM Provider \(ASP\) integrations for IBM](ibm-asp-integration.md).


**Parent Topic:**[Supported IBM license types](supported-ibm-license-types.md)

