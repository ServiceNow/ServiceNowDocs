---
title: Software Publisher Analytics dashboard for Citrix in Software Asset Management classic
description: View compliance analysis results for Citrix on the Software Publisher Analytics dashboard in the Software Asset Management classic application.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software Asset Management publisher pack for Citrix, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Software Publisher Analytics dashboard for Citrix in Software Asset Management classic

View compliance analysis results for Citrix on the Software Publisher Analytics dashboard in the Software Asset Management classic application.

Access the Software Publisher Analytics dashboard by navigating to **All** &gt; **Software Asset** &gt; **Publisher Overview**.

**Note:** The add-on Citrix publisher pack \(com.sn\_samp\_citrix\) [plugin](../task/t_RequSoftwareAssetMgmt.md) must be installed to view the Citrix dashboard tab.

A discovery process is required for Citrix data to be collected. For ServiceNow Discovery, a user with the admin role must create a [Discovery schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/t_CreateADiscoverySchedule.md) to run on the Citrix Delivery Controller for communication with the Citrix License Server.

The dashboard is updated whenever a new reconciliation result is available. You can save charts in PNG or JPG format.

![Software Publisher Analytics dashboard for Citrix.](../image/publisher-dashboard-citrix.png)

<table id="table_w2z_4dr_ycb"><thead><tr><th>

Report

</th><th>

Source list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

True-up Cost

</td><td>

Product Results

</td><td>

Cost to be compliant based on the average prices for entitlements for the rights.

</td></tr><tr><td>

Products out of Compliance

</td><td>

Product Results

</td><td>

Number of products that have at least one software model out of compliance.Select the report to view the results in the [License Workbench](../concept/sam-license-workbench.md).

</td></tr><tr><td>

Over-Licensed Amount

</td><td>

Product Results

</td><td>

Cost of licenses owned but not being used.

</td></tr><tr><td>

User Access to Products in Citrix Farm

</td><td>

Software Installations

</td><td>

Number of users with access to the Citrix farms.

</td></tr><tr><td>

Citrix Software Lifecycle Report

</td><td>

Software Lifecycle Report

</td><td>

Number of products in each software lifecycle phase, including End of Extended Support, End of Life, and End of Support.

</td></tr><tr><td>

User/Device Rights vs Usage Software Installs in Citrix Farm

</td><td>

Software Installations

</td><td>

Number of User/Device rights owned versus the number of rights being consumed.

</td></tr><tr><td>

Concurrent License Consumption Trend

</td><td>

License Consumption History

</td><td>

License consumption trends for your Citrix software products. Each data point represents the maximum in-use license count per day.

 Select a data point to view additional license consumption data for a specific Citrix software product.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management publisher pack for Citrix](../concept/citrix-publisher-pack.md)

