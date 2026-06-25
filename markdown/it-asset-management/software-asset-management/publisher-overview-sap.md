---
title: Publisher overview for SAP in the Software Asset Workspace
description: View license usage information related to SAP in the publisher overview for SAP in the Software Asset Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/publisher-overview-sap.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Publisher overview for SAP in the Software Asset Workspace

View license usage information related to SAP in the publisher overview for SAP in the Software Asset Workspace.

From the Software Asset Workspace, access the SAP publisher overview by navigating to **License usage** &gt; **Publishers** and then selecting **SAP** from the list of available software publishers.

Results are updated whenever a new reconciliation result is available.

\[Omitted image "publisher-overview-sap.png"\] Alt text: SAP publisher overview.

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
</table>For more details on the license usage information that is provided in the publisher overview, see [License usage publisher fields in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/workbench-publisherfields-workspace.md).

**Parent Topic:**[Software Asset Management publisher pack for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack]()

[Set up SAP integration to establish a connection with SAP]()

[Establish an SAP connection using basic authentication]()

[Establish an SAP connection using OAuth 2.0]()

[Create entitlements for SAP]()

[Create software models for SAP]()

[Create a custom SAP named user type]()

[Map a role to a named user type]()

[Create custom SAP price lists]()

[Import custom SAP named user types]()

[Import custom SAP price lists]()

[SAP USMM-based optimization]()

[User transaction activity for named user types]()

[Self-declaring SAP engine license usage]()

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic]()

