---
title: View software model results
description: View compliance information for software model results from the Product Results list after reconciliation is run.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Software license usage, Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# View software model results

View compliance information for software model results from the Product Results list after reconciliation is run.

## Before you begin

Role required: sam\_user

## About this task

You can view License Metric Results, Remediation Options, Licensed Installs, Unlicensed Installs, and Removal Candidates related lists for a software model result from a Product Result record. When the [Procurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/procurement/c_Procurement.md) application \(com.snc.procurement\) is active, you can also create and view purchase orders directly from the Remediation Options form. More remediation options include automatically create and remove allocations, remove unallocated installs, and remove unlicensed installs.

For example, if the status of a product result shows that it isn’t compliant, you can drill down on the product result to view software model details. These details can include the number of unlicensed installs and the true-up cost to become compliant. Further, you can drill down on the software model result to view the license metric result, which is based on the entitlements for the product.

License metric result information includes rights owned and rights used as well as the license allocation breakdown so you can determine your options to become compliant. The Remediation Options related list shows the number of rights needed and calculates the cost of those rights for you, based on the license metric.

You can use the dashboard field action ![DashboardFieldAction](../image/SAMdashboardIcon.png) icon on the Software Model Results form to view the Rights Owned vs Rights Used chart to forecast when additional licenses are needed.

**Note:** Software model results \(SMRs\) aren’t generated for software models for Oracle Database options without associated software entitlements. However, you can set the system property **com.snc.samp.unlicensed\_smr\_creation** to **True** to create SMRs for these models even if there are no entitlements.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Reconciliation** &gt; **Historical Results** and select a reconciliation result.

2.  On the Reconciliation Result form, select a Product Results record to view the product result details.

3.  In the Software Model Results related list, open a record to view the software model result details.

<table id="table_bnb_zqv_pz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software model

</td><td>

Software model associated with the product. Drill down on the software model to see the software model result.The dashboard field action ![DashboardFieldAction](../image/SAMdashboardIcon.png) icon shows the Rights Owned vs Rights Used chart for the software model.

</td></tr><tr><td>

Product result

</td><td>

Unique product result number generated during the reconciliation process.

</td></tr><tr><td>

Group

</td><td>

Group specified on which to run reconciliation. Values include None, Country, Department, Company, Region, and Cost Center.

</td></tr><tr><td>

Subgroup

</td><td>

Subgroup specified on which to run reconciliation. Values include None, Country, Department, Company, Region, and Cost Center.

</td></tr><tr><td>

Latest

</td><td>

Indicates whether this software model result is from the most recent reconciliation run.

</td></tr><tr><td>

Status

</td><td>

Status of the software model.-   Compliant
-   Not Compliant


</td></tr><tr><td>

Agreement type

</td><td>

Agreement type is set on the software entitlement.-   Common: Generic, Enterprise License Agreement \(ELA\)
-   IBM: Generic, Enterprise License Agreement \(ELA\), International Program License Agreement \(IPLA\), IBM Customer Agreement \(ICA\), Unlimited Level Agreement \(ULA\)
-   Microsoft: Generic, Enterprise License Agreement \(ELA\)
-   Oracle: Generic, Unlimited Level Agreement \(ULA\)
-   VMware: Generic, Enterprise License Agreement \(ELA\), Enterprise Purchasing Program \(EPP\), Volume Purchasing Program \(VPP\)
 **Note:** If the agreement type is Enterprise Level Agreement or Unlimited Level Agreement, the **Status** is Compliant even if there are unlicensed installations or unlicensed subscriptions.

</td></tr><tr><td>

Unlicensed installs

</td><td>

Number of unlicensed software installations that aren’t covered by any entitlements.

</td></tr><tr><td>

True-up cost

</td><td>

Estimated cost of remediating unlicensed installations based on the lowest number of rights needed \(rights needed \* average price per right from entitlements\). The lowest cost from Purchase Rights remediation options.

</td></tr><tr><td>

Over-licensed amount

</td><td>

Estimated cost of rights not being used. The sum of the Over Licensed amount from the True-up value costs.

</td></tr><tr><td>

Potential savings

</td><td>

The cost that can be saved by acting on underutilized or incorrect consumption of licenses in related removal candidates.

</td></tr><tr><td class="sub-head" id="LicenseMetricResults" colspan="2">

License Metric Results

</td></tr><tr><td>

Display name

</td><td>

Name of the license metric that the software license is counted against when reconciliation runs.

 Select the **Display name** to open the corresponding License Metric Results record, where you can view more in-depth information about the license metric result. See [Software model results license metric results fields](../reference/license-metric-results-fields.md) for more details.

</td></tr><tr><td>

Rights owned

</td><td>

Sum of all active rights from entitlements that share a license metric.

</td></tr><tr><td>

Rights used

</td><td>

Sum of rights used during reconciliation \(allocated plus not allocated and installed\).

</td></tr><tr><td>

Rights available

</td><td>

Sum of rights not used during reconciliation \(rights owned minus rights used\).

</td></tr><tr><td>

Over-licensed amount

</td><td>

Estimated cost of unused rights.

</td></tr><tr><td>

Legacy license

</td><td>

Indicates licenses purchased before 1 Oct 2019.​ This field appears only when the environment has dedicated hosts on AWS or on Azure.**Note:** Microsoft has updated licensing rules for dedicated hosts based on the purchase date.

</td></tr><tr><td>

Allocated in use

</td><td>

Rights that are allocated and are used to license installations.

</td></tr><tr><td>

Not allocated in use

</td><td>

Number of rights that are used to license installations, but not allocated.

 When this value is greater than 0, two remediation options \(Create Allocations and Remove Unallocated Installs\) are automatically created for each unique license metric in the software model that meets this requirement, except User CAL and Device CAL.

</td></tr><tr><td>

Allocated not in use

</td><td>

Rights that are allocated but aren’t being used to license any installations.

 **Note:** **Allocated not in use** reflects rights that are wasted because the user or device for which these rights have been allocated don’t have the software installed.

 When this value is greater than 0, a Remove Allocations remediation option is automatically created for each unique license metric in the software model that meets this requirement.

</td></tr><tr><td>

Nontransferable rights

</td><td>

Remaining rights from a core pack that can’t be used to license any additional devices. Nontransferable rights are available only for Microsoft Per Core and Microsoft Per Core with \(CAL\).

</td></tr><tr><td>

Not allocated

</td><td>

Number of rights that haven’t been allocated \(rights owned minus allocated regardless of whether installed or not\).

</td></tr><tr><td>

Allocations needed

</td><td>

Number of allocations needed for compliance. Only used for Per Named User and Per Named Device license metrics.

</td></tr><tr><td>

Rights needed**Note:** This field is hidden by default. Select the personalize list icon ![Personalize list icon.](../image/gear-icon.png) to modify the fields that appear in the License Metric Results.

</td><td>

Number of rights that are required to cover unlicensed installations.

</td></tr><tr><td>

Unlicensed installs**Note:** This field is hidden by default. Select the personalize list icon ![Personalize list icon.](../image/gear-icon.png) to modify the fields that appear in the License Metric Results.

</td><td>

Number of unlicensed software installations that aren’t covered by any entitlements.

</td></tr><tr><td>

Unlicensed SAP users \(SAP only\)**Note:** This field is hidden by default. Select the personalize list icon ![Personalize list icon.](../image/gear-icon.png) to modify the fields that appear in the License Metric Results.

</td><td>

Number of unlicensed SAP users that aren’t covered by any entitlements.

</td></tr><tr><td>

Unlicensed options \(Oracle only\)**Note:** This field is hidden by default. Select the personalize list icon ![Personalize list icon.](../image/gear-icon.png) to modify the fields that appear in the License Metric Results.

</td><td>

Number of unlicensed Oracle database options that aren’t covered by any entitlements.

</td></tr><tr><td>

Unlicensed subscriptions**Note:** This field is hidden by default. Select the personalize list icon ![Personalize list icon.](../image/gear-icon.png) to modify the fields that appear in the License Metric Results.

</td><td>

Number of unlicensed software subscriptions that aren’t covered by any entitlements.

</td></tr><tr><td>

True-up cost**Note:** This field is hidden by default. Select the personalize list icon ![Personalize list icon.](../image/gear-icon.png) to modify the fields that appear in the License Metric Results.

</td><td>

Estimated cost of remediating unlicensed installations that are based on the lowest number of rights needed.

</td></tr><tr><td>

Potential savings**Note:** This field is hidden by default. Select the personalize list icon ![Personalize list icon.](../image/gear-icon.png) to modify the fields that appear in the License Metric Results.

</td><td>

Estimated cost saved by reclaiming removal candidates.

</td></tr><tr><td>

Downgrade rights**Note:** This field is hidden by default. Select the personalize list icon ![Personalize list icon.](../image/gear-icon.png) to modify the fields that appear in the License Metric Results.

</td><td>

Previous software versions that you can license using software entitlements for the latest software version.

</td></tr><tr><td class="sub-head" colspan="2">

Remediation Options

</td></tr><tr><td>

Remediation action

</td><td>

Action to take to for compliance.-   Purchase Rights
-   Remove Allocations
-   Create Allocations
-   Remove Unallocated Installs \(Not available for Oracle database options\)
-   Remove Unlicensed Installs \(Not available for Oracle database options\)
-   Remove Unlicensed Installs - Cloud \(available only if you have cloud installations\).
-   If the actionable rights value is 0, the **Remediation action** button will not appear.


</td></tr><tr><td>

Affects compliance

</td><td>

Specifies whether the remediation options affect compliance.

</td></tr><tr><td>

License metric

</td><td>

Specific license metric of the software model result.

</td></tr><tr><td>

Software model result

</td><td>

Specific software model result pertaining to the remediation option.

</td></tr><tr><td>

Status

</td><td>

Status of the remediation option.-   New \(blue\)
-   Complete \(green\)
-   Completed with Errors \(yellow\)
-   Void \(red\)
-   In Progress \(yellow\)

In Progress state indicates that the remediation action is in progress. If removal candidates are being created, the status changes to **completed** once the removal candidates are created.

</td></tr><tr><td>

Rights not in use

 Rights not allocated

 Rights needed

 Reclaimable rights

 Unlicensed rights

 \(Field shown is based on Remediation action type\)

</td><td>

-   **Remove Allocations** action shows **Rights not in use** field.
-   **Create Allocations** action shows **Rights not allocated** field.
-   **Purchase Rights** shows **Rights needed** field.
-   **Remove Unallocated Installs** action shows **Reclaimable rights** field.
-   **Remove Unlicensed Installs** action shows **Unlicensed rights** field.


</td></tr><tr><td>

Actionable rights

</td><td>

Total rights affected by the action.

</td></tr><tr><td>

Purchase order

</td><td>

Purchase order number associated with the remediation option, if a purchase order was created.

</td></tr><tr><td>

True-up cost

</td><td>

Estimated cost of remediating unlicensed installations based on the lowest number of rights needed.

</td></tr><tr><td class="sub-head" colspan="2">

Unlicensed Subscriptions**Note:** This related list is shown only for subscription-based software products.

</td></tr><tr><td>

Display name

</td><td>

Name of the unlicensed software subscription that is not covered by any entitlements.

</td></tr><tr><td>

User principal name

</td><td>

Name of the user that is associated with the unlicensed software subscription.

</td></tr><tr><td>

Software model

</td><td>

Software model that the unlicensed software subscription is associated with.

</td></tr><tr><td>

Subscription profile

</td><td>

Integration profile that the unlicensed software subscription is associated with.

</td></tr><tr><td>

Subscription type

</td><td>

Type of subscription.

</td></tr><tr><td class="sub-head" colspan="2">

Unlicensed Consumptions**Note:** This related list is shown only for consumption-based software models.

</td></tr><tr><td>

Software model

</td><td>

Software model that has unlicensed software consumptions.

</td></tr><tr><td>

Subscription profile

</td><td>

Integration profile that has unlicensed software consumptions.

</td></tr><tr><td>

Units consumed

</td><td>

Number of software units that your users have consumed.

</td></tr><tr><td>

Contract start

</td><td>

Start date of your licensing contract.

</td></tr><tr><td>

Contract end

</td><td>

End date of your licensing contract.

</td></tr><tr><td>

Actual monthly consumption

</td><td>

Actual number of software units that your users consume per month.

</td></tr><tr><td>

Expected monthly consumption

</td><td>

Number of software units that you expect your users to consume per month.

</td></tr><tr><td>

Cost Center

</td><td>

Business unit that has unlicensed software consumptions.

</td></tr><tr><td>

Department

</td><td>

Department that has unlicensed software consumptions.

</td></tr><tr><td>

Location

</td><td>

Geographic location in which there are unlicensed software consumptions.

</td></tr><tr><td>

Company

</td><td>

Name of the company that has unlicensed software consumptions.

</td></tr></tbody>
</table>    The Licensed Installs related list contains the [software installations](../concept/c_DiscoveryModels.md) that are licensed. To view more information about a licensed software installation, open the corresponding Software Installation record by selecting the **Display name**. Refer to [Software installation fields](../reference/software-installation-fields.md) for detailed descriptions of each field in the Software Installation record.

    The Unlicensed Installs related list contains the [software installations](../concept/c_DiscoveryModels.md) that are unlicensed. To view more information about an unlicensed software installation, open the corresponding Software Installation record by selecting the **Display name**. Refer to [Software installation fields](../reference/software-installation-fields.md) for detailed descriptions of each field in the Software Installation record.

    The Unlicensed Users related list contains the [SAP system users](../concept/sap-publisher-pack.md) that are unlicensed.

    **Note:** This related list is shown only for the SAP publisher.

    The Removal Candidates related list contains removal candidates related to software installations. For more information, see [Removal candidates](t_AddAReclCandidate.md).

4.  Execute remediation options for specific remediation actions by selecting an option from the Remediation Options related list and then selecting the applicable action.

<table id="table_hyf_fmh_2bb"><thead><tr><th>

Remediation option action

</th><th>

Action button

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Remove Unlicensed Installs

</td><td>

**Create All Removal Candidates**

</td><td>

When removal candidates are created for unlicensed installs, the status is set to Awaiting Revocation.

</td></tr><tr><td>

Remove Unallocated Installs

</td><td>

**Create All Removal Candidates**

</td><td>

When removal candidates are created for unallocated installs, the status is set to Ready.

</td></tr><tr><td>

Remove Allocations

</td><td>

**Remove All Allocations**

</td><td>

When allocations are removed, the number of allocations is adjusted.When you select this button, a message is displayed on the screen indicating that the action is in progress.

</td></tr><tr><td>

Create Allocations

</td><td>

**Create All Allocations**

</td><td>

When allocations are created, the status of Remove Unallocated Installs remediation options \(for the same license metric of the same software model result\) are then set to Void.When you select this button, a message is displayed on the screen indicating that the action is in progress.

</td></tr><tr><td>

Purchase Rights

</td><td>

**Create Purchase Order** **Note:** The **Create Purchase Order** button creates a [purchase order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/procurement/t_CreateAPurchaseOrderLineItem.md) but is only shown when rights needed is greater than 0, and Procurement is active.

The **Create Purchase Order** button remains active until the purchase order has finished processing. Therefore, to avoid the creating a duplicate purchase order for the same item, wait to run reconciliation again until after the purchase order has finished processing.

</td><td>

When a purchase order is created, the status of any Purchase Rights remediation options for the same software model result are then set to Void.Purchase order fields **Part number**, **Metric group**, **License metric**, and **Ordered quantity** are automatically populated with the content from the remediation option.

 **Metric group** and **License metric** fields are added to the purchase order form so the entitlement can be automatically created when the order is complete.

 A notification is shown if at least one active purchase order line item exists for the software model.

 Once a purchase order is created, the **Purchase order** field, containing the purchase order reference, is added to the remediation option.

</td></tr></tbody>
</table>    A confirmation message is shown and all applicable [removal candidates](t_AddAReclCandidate.md) are added to the Removal Candidates related list.


**Parent Topic:**[Software license usage](../concept/sam-license-workbench.md)

