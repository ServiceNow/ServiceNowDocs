---
title: CI deletion strategies for pattern discovery
description: When you perform discovery with a pattern, you can choose what to do with configuration items \(CIs\) that are in the Configuration Management Database \(CMDB\) but Discovery can no longer find.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# CI deletion strategies for pattern discovery

When you perform discovery with a pattern, you can choose what to do with configuration items \(CIs\) that are in the Configuration Management Database \(CMDB\) but Discovery can no longer find.

**Note:** Deletion strategies are available only with patterns, not probes/sensors.

When you use a pattern to perform discovery, you identify a CI Type, which is the main CI you're trying to find, such as an IIS web server or Tomcat server. Discovery can also find related CIs and populate the CMDB accordingly. For example, after Discovery finds an IIS server with the IIS pattern, it can also find these related CIs:

-   The Windows machine that hosts the web server
-   The configuration files for the IIS server
-   The website that the IIS server hosts

The dependency map on the main CI also shows the related CIs, as illustrated by the following graphic:

![related CIs to an IIS server](../image/iis-server-related-cis.png "An example of an IIS server main CI and its related CIs")

After you discover the main CI and its related CIs for the first time using a pattern, you must manually configure an entry in the Related CI Types \[sa\_ci\_to\_pattern\] table for each relation between the main CI and a related CI type. These records are where you determine the deletion strategy for each related CI based on its type. Note that you cannot set a deletion strategy for the main CI for Infrastructure pattern type.

You can view a list of the relations as the following image illustrates:

![CIs related to an IIS server](../image/iis-server-related-cis-list.png "Example CIs related to an IIS server")

The deletion strategy on a related CI takes effect when both of these conditions occur:

-   After you run Discovery with the pattern again.
-   Discovery successfully finds the main CI but cannot find the related CI.

These deletion strategy options are available:

<table id="table_xl2_jwf_5z"><thead><tr><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Keep

</td><td>

Preserves the configuration file CI record and makes no other changes to the record. This option is the default setting.

</td></tr><tr><td>

Delete

</td><td>

Deletes the configuration file CI record from the CMDB, and the relationship to the main CI.

</td></tr><tr><td>

Mark as absent

</td><td>

Marks the **Status** \[install\_status\] field of the configuration file CI record as **Absent**, meaning that Discovery cannot find the tracked configuration file. This status does not instruct the system to delete the actual CI or the relationship.**Note:** There are two tables that do have their CIs deleted if marked as absent: cmdb\_ci\_network\_adapter and cmdb\_ci\_ip\_address.

</td></tr><tr><td>

Delete relations

</td><td>

Deletes only the CI relationships between the related CI and the main CI.

</td></tr><tr><td>

Mark as retired

</td><td>

Marks the **Status** \[install\_status\] field of the configuration file CI record as **Retired**, meaning that Discovery no longer uses this configuration file. This status does not instruct the system to delete the actual CI or the relationship.

</td></tr></tbody>
</table>**Note:** Deletion strategies are not available for related entries, which are rules that are based on related CIs. For more information, see [Related entries](https://www.servicenow.com/docs/access?context=c_IdentificationRules&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US#section_ftc_tg4_j1b).

-   **[Set a deletion strategy](../task/set-deletion-strategy.md)**  
Set a deletion strategy when you want to take action on a related configuration item \(CI\) that Discovery can no longer find through pattern discovery. You can delete the main CI only when it is an Application or Cloud Resource pattern type.

**Parent Topic:**[Advanced Discovery configuration](c_DiscoveryExtendedCapabilities.md)

