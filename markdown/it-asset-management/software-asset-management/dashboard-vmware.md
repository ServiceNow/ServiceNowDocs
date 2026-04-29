---
title: Software Publisher Analytics dashboard for VMware in Software Asset Management classic
description: View compliance analysis results related to VMware on the Software Publisher Analytics dashboard in the Software Asset Management classic application.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software Asset Management publisher pack for VMware, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Software Publisher Analytics dashboard for VMware in Software Asset Management classic

View compliance analysis results related to VMware on the Software Publisher Analytics dashboard in the Software Asset Management classic application.

Access the Software Publisher Analytics dashboard by navigating to **All** &gt; **Software Asset** &gt; **Publisher Overview**.

**Note:** The add-on VMware publisher pack \(com.sn\_samp\_vmware\) plugin must be installed to view the VMware dashboard tab.

The dashboard is updated whenever a new reconciliation result is available. You can save charts in PNG or JPG format.

## VMware dashboard

Information from VMware vCenter software is discovered and used for VMware reconciliation. Discovery uses these probes and populates these tables:

-   [vCenter probe](https://www.servicenow.com/docs/access?context=vcenter-probes&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) VMware — vCenter ESX Hosts License
-   VMware Discovered License Key \[samp\_vmware\_license\_key\] and VMware Discovered License Key Consumption \[samp\_vmware\_license\_key\_usage\] tables

**Note:** The add-on VMware publisher pack \(com.sn\_samp\_vmware\) plugin must be installed to view the VMware dashboard tab.

![Software Publisher Analytics dashboard for VMware.](../image/publisher-dashboard-vmware.png)

<table id="table_gqs_l5c_fbb"><thead><tr><th>

Report

</th><th>

Source list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Products out of Compliance

</td><td>

Product Results

</td><td>

Number of products that have at least one software model out of compliance.Select the report to view the results in the [Software license usage](../concept/sam-license-workbench.md).

</td></tr><tr><td>

Over-licensed Amount

</td><td>

Product Results

</td><td>

Cost of licenses owned but not being used.

</td></tr><tr><td>

True-up Cost

</td><td>

Product Results

</td><td>

Cost to be compliant based on the average prices for entitlements for the rights.

</td></tr><tr><td>

Top 5 Installed Products

</td><td>

Software Installations

</td><td>

Count of top 5 VMware products installed.

</td></tr><tr><td>

vSphere Territorial Non-compliance

</td><td>

VMware Discovered License Key Consumptions

</td><td>

Compliance of VMware vCenter deployments. Drill down on the location to filter.

</td></tr><tr><td>

ESX Servers by Region

</td><td>

ESX Servers

</td><td>

Location, ESX count, CPU count, and cores count.

</td></tr><tr><td>

Audit View

</td><td>

VMware Discovered License Key Consumptions

</td><td>

VMware vSphere deployments: Product, License Key, Used By, Assigned To, Location, CPU core count, CPU count, vCenter reference, evaluation expiration date, and software install.

</td></tr><tr><td>

VMware Software Lifecycle Report

</td><td>

Software Lifecycle Report

</td><td>

Number of products in each software lifecycle phase, including End of Extended Support, End of Life, and End of Support.

</td></tr></tbody>
</table>The **vSphere Deployment** related link shows the VMware Discovered License Key Consumptions list.

**Parent Topic:**[Software Asset Management publisher pack for VMware](../concept/vmware-publisher-pack.md)

