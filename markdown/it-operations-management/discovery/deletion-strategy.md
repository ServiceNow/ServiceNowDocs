---
title: CI deletion strategies for pattern discovery
description: When you perform discovery with a pattern, you can choose what to do with configuration items \(CIs\) that are in the Configuration Management Database \(CMDB\) but Discovery can no longer find.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/deletion-strategy.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-11-16"
reading_time_minutes: 2
breadcrumb: [Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# CI deletion strategies for pattern discovery

When you perform discovery with a pattern, you can choose what to do with configuration items \(CIs\) that are in the Configuration Management Database \(CMDB\) but Discovery can no longer find.

**Note:** Deletion strategies are available only with patterns, not with probe-based or sensor-based discovery.

When you use a pattern to perform discovery, you identify a CI Type, which is the main CI you're trying to find, such as an IIS web server or Tomcat server. Discovery can also find related CIs and populate the CMDB accordingly. For example, after Discovery finds an IIS server with the IIS pattern, it can also find these related CIs:

-   The Windows machine that hosts the web server
-   The configuration files for the IIS server
-   The IIS virtual directories
-   The website that the IIS server hosts

The dependency map on the main CI also shows the related CIs, as illustrated by the following graphic:

\[Omitted image "iis-server-related-cis.png"\] Alt text: related CIs to an IIS server

The Related CI Types \[sa\_ci\_to\_pattern\] table contains a record for each CI type that a pattern finds. Each record determines the deletion strategy for CIs of that type. You can set a deletion strategy for the main CI only when the pattern type is Application or Cloud Resource. You can't set one for the main CI in an Infrastructure pattern. To change a strategy, see [Set a deletion strategy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/set-deletion-strategy.md).

You can view the list of CI types for the pattern as the following image illustrates:

\[Omitted image "iis-server-related-cis-list.png"\] Alt text: CIs related to an IIS server

A deletion strategy takes effect each time you run Discovery with the pattern. Discovery compares the results with what was found before and applies the strategy to a CI that it can no longer find. The first run has nothing to compare with, so no strategy applies.

These deletion strategy options are available:

<table id="table_xl2_jwf_5z"><thead><tr><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Keep

</td><td>

Preserves the CI record and makes no other changes to it. This option is the default setting.

</td></tr><tr><td>

Delete

</td><td>

Deletes the CI record from the CMDB, together with its relationships.

</td></tr><tr><td>

Mark as absent

</td><td>

Marks the **Status** \[install\_status\] field of the CI record as **Absent**, meaning that Discovery can't find the CI. This status doesn't instruct the system to delete the CI or or its relationships.**Note:** There are two exceptions. Discovery deletes CIs in the cmdb\_ci\_network\_adapter and cmdb\_ci\_ip\_address tables when it marks them as absent.

</td></tr><tr><td>

Delete relations

</td><td>

Deletes only the CI relationships between the related CI and the main CI.

</td></tr><tr><td>

Mark as retired

</td><td>

Marks the **Status** \[install\_status\] field of the CI record as **Retired**, meaning that Discovery no longer uses this CI. This status doesn't instruct the system to delete the CI or its relationship.

</td></tr></tbody>
</table>**Note:** Deletion strategies aren't available for related entries, which are identification rules that are based on related CIs. For more information, see [Related entries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_IdentificationRules.md#section_ftc_tg4_j1b).

-   **[Set a deletion strategy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/set-deletion-strategy.md)**  
Set a deletion strategy when you want to take action on a configuration item \(CI\) that Discovery can no longer find through pattern discovery.

**Parent Topic:**[Advanced Discovery configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/c_DiscoveryExtendedCapabilities.md)

