---
title: Configurable workspaces
description: Use configurable workspaces for creating and managing medical and facility assets and models your specific industry or operational environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/medical-facility-workspaces.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Enterprise Asset Management, IT Asset Management]
---

# Configurable workspaces

Use configurable workspaces for creating and managing medical and facility assets and models your specific industry or operational environment.

## Overview of configurable workspaces for medical and facilities industries

Configurable workspace is available for the following applications:

-   Enterprise Asset Management for Healthcare
-   Enterprise Asset Management for Facilities
-   OT Asset Management
-   Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)

Configurable workspace gives you a personalized experience as you work on assets and models pertaining to your industry or operational environment.

|Application|Configurable workspace|Benefits|
|-----------|----------------------|--------|
|Enterprise Asset Management for Healthcare|Medical Asset Workspace|Create and manage medical assets and models.|
|Enterprise Asset Management for Facilities|Facility Asset Workspace|Create and manage facilities assets and models.|
|OT Asset Management|OT Asset Workspace|Create and manage operational technology and operational equipment assets and models.|
|Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)|Critical Environment Asset Workspace|Create and manage data center and network infrastructure assets, including facility-based enterprise assets and linear assets.|

**Note:** The normalization process only runs in the Enterprise Asset Workspace and doesn't run for medical models and facility models within their specific workspaces.

## Workspace roles

The workspace that you can access depends on the role with which you log in to your ServiceNow instance. You can only view and work in the workspaces for which you have an assigned role.

<table id="table_ck3_4kl_mbc"><thead><tr><th>

Workspace

</th><th>

Role needed

</th></tr></thead><tbody><tr><td>

Medical Asset Workspace

</td><td>

-   Medical asset manager \(sn\_eamhc.medical\_asset\_manager\)
-   Medical asset technician \(sn\_eamhc.medical\_asset\_technician\)
-   Enterprise admin \[sn\_eam.enterprise\_admin\]
-   System administrator \[sys\_admin\]

</td></tr><tr><td>

Facility Asset Workspace

</td><td>

-   Facility asset manager \(sn\_eamhc.facility\_asset\_manager\)
-   Facility asset technician \(sn\_eamhc.facility\_asset\_technician\)
-   Enterprise admin \(sn\_eam.enterprise\_admin\)
-   System administrator \(sys\_admin\)

</td></tr><tr><td>

OT Asset Workspace

</td><td>

-   OT asset manager \(sn\_otam.ot\_asset\_manager\)
-   OT asset technician \(sn\_otam.ot\_asset\_technician\)
-   Enterprise admin \(sn\_eam.enterprise\_admin\)
-   System administrator \(sys\_admin\)

</td></tr><tr><td>

Critical Environment Asset Workspace

</td><td>

-   DCNAM asset manager \(sn\_eam\_dcnam.dcnam\_asset\_manager\)
-   DCNAM asset technician \(sn\_eam\_dcnam.dcnam\_asset\_technician\)
-   Enterprise admin \(sn\_eam.enterprise\_admin\)
-   System administrator \(sys\_admin\)

</td></tr><tr><td>

All workspaces

</td><td>

-   Enterprise admin \(sn\_eam.enterprise\_admin\)
-   System administrator \(sys\_admin\)

</td></tr></tbody>
</table>## Role-based visibility in workspaces

When you log in with an industry-specific role, your workspace view is scoped to your industry by default. For example:

-   If you’re logged in as a medical asset manager or medical asset technician, you see only the medical asset category in the Medical asset estate view and the medical model category in the Medical model management view.
-   If you’re logged in as a facility asset manager or facility asset technician, you see only the facility asset category in the Facility asset estate view and the facility model category in the Facility model management view.
-   If you’re logged in as an OT asset manager or OT asset technician, you see only OT and OE asset and model categories in the OT asset estate view and OT model management view.

You may also see asset and model categories outside your industry if they were added by the Enterprise admin or System administrator. These categories are read-only — you can’t create or modify assets or models in them.

## Asset performance

You can evaluate how effectively your assets are functioning and being used through reports based on asset key performance indicators \(KPIs\) in the Asset performance tab of the Asset analytics view. The asset performance report is also available on the contextual sidebar of the asset record, displayed by selecting the Asset availability and related KPIs icon \[Omitted image "asset-kpi-icon.png"\] Alt text:. For details, see [Asset performance reports in the Enterprise Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/asset-performance-reports-eam.md).

## Unified receiving

You can receive assets from any workflow directly at the stockroom using the unified receiving functionality available in all industry-specific workspaces. You can receive assets in any of the following ways:

-   Receive a single asset
-   Receive multiple assets in a shipment
-   Import assets in bulk and receive them

For more details, see [Unified receiving](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/manage-stockroom-receive-eam.md).

## Inventory reports

You can manage supply and demand in your stockrooms effectively with inventory demand reports. Navigate to the Inventory insights tab in any stockroom to view the reports. For more details, see [Manage stockrooms with inventory reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/manage-stockroom-inventory-reports.md).

## Accessing the Admin center

Only the Enterprise admin role and the System administrator role can make configuration changes in the **Admin center** of any industry-specific workspace.

Industry-specific manager and technician roles can’t make changes in the Admin center except for the **Task rate card and Labor rate card** options under the **TCO configuration** list.

