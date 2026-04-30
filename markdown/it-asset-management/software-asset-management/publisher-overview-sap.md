---
title: Publisher overview for SAP in the Software Asset Workspace
description: View license usage information related to SAP in the publisher overview for SAP in the Software Asset Workspace.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Publisher overview for SAP in the Software Asset Workspace

View license usage information related to SAP in the publisher overview for SAP in the Software Asset Workspace.

From the Software Asset Workspace, access the SAP publisher overview by navigating to **License usage** &gt; **Publishers** and then selecting **SAP** from the list of available software publishers.

Results are updated whenever a new reconciliation result is available.

![SAP publisher overview.](../image/publisher-overview-sap.png)

You can view a summary of your license usage information in the Summary section of the SAP publisher overview.

<table id="table_amj_kvh_rpb"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

True-up cost

</td><td>

Cost to be compliant based on the average price of rights in your SAP software entitlements.

</td></tr><tr><td>

Potential savings

</td><td>

Potential cost savings for your SAP licenses.

</td></tr><tr><td>

Actual savings

</td><td>

Actual cost savings for your SAP licenses.

</td></tr><tr><td>

Unlicensed entities

</td><td>

Summary of your unlicensed entities.This summary includes the following information:

-   **Unlicensed client access**: Total number of unlicensed SAP client access records. Select the number to view the complete list of unlicensed SAP client access records.
-   **Unlicensed engines**: Total number of unlicensed SAP engines. Select the number to view the complete list of unlicensed SAP engines.
-   **Unlicensed users**: Total number of unlicensed SAP users. Select the number to view the complete list of unlicensed SAP users.

</td></tr><tr><td>

Progress indicators

</td><td>

Summary of your license compliance progress.This summary includes the **Removal candidates** indicator, which displays the total number of SAP removal candidates. Select the number to view the list of all software removal candidates.

</td></tr><tr><td>

Engines usage reached 90% and above

</td><td>

Total number of SAP engines that have reached 90% usage or higher.

</td></tr><tr><td>

Potential indirect access \(user activity\)

</td><td>

Total number of SAP users that have indirect access to the SAP system.Users are given a score based on total CPU time, peak count, and steps.

</td></tr><tr><td>

Potential indirect access \(transaction activity\)

</td><td>

Total number of SAP users with indirect access to the SAP system based on user transaction activity.Users are given a score based on the amount of data received or sent by each connection.

</td></tr></tbody>
</table>For more details on the license usage information that is provided in the publisher overview, see [License usage publisher fields in workspace](workbench-publisherfields-workspace.md).

**Parent Topic:**[Software Asset Management publisher pack for SAP](../concept/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack](../concept/component-installed-sap-plugin.md)

[Deploy the ABAP program for SAP](../task/import-abap-program-sap.md)

[Establish an SAP connection](../task/add-sap-connection.md)

[Create entitlements for SAP](../task/create-entitlement-sap.md)

[Create software models for SAP](../task/add-software-model-sap.md)

[Create a custom SAP named user type](../task/create-named-user.md)

[Map a role to a named user type](../task/create-named-user-type-role-mapping.md)

[Create custom SAP price lists](../task/create-sap-pricelist.md)

[Import custom SAP named user types](../task/import-custom-sap-named-user-type.md)

[Import custom SAP price lists](../task/import-custom-sap-price-list.md)

[SAP USMM-based optimization](../concept/usmm-optimization.md)

[User transaction activity for named user types](../concept/sap-named-user-transaction-activity.md)

[Self-declaring SAP engine license usage](../concept/self-declaring-sap-engine-usage.md)

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic](dashboard-sap.md)

