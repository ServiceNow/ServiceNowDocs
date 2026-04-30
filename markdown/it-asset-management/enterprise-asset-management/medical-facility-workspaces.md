---
title: Personalized workspaces for medical and facility industries
description: Use personalized workspaces for creating and managing medical and facility assets and models.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Personalized workspaces for medical and facility industries

Use personalized workspaces for creating and managing medical and facility assets and models.

## Overview

Personalized workspaces help you to work on specific industry functional areas where the asset and model tabs are configured based on your industry.

Use the following workspaces tailored for the medical and facility industries:

-   Medical Asset Workspace: Create and manage your medical assets and models.
-   Facility Asset Workspace: Create and manage your facility assets and models.

**Note:** The normalization process only runs in the Enterprise Asset Workspace and doesn't run for medical models and facility models within their specific workspaces.

If you’re logged in as a medical asset manager or a medical asset technician, by default you only get to see the medical asset category in the **Medical asset estate** view and the medical model category in the **Medical model management** view. Similarly if you’re logged in as a facility asset manager or a facility asset technician, you only get to see the facility asset category in the **Facility asset estate** view and the facility model category in the **Facility model management** view.

If you’re logged in to a specific workspace, you may see other assets and model categories that aren’t specific to your industry and have been added by the Enterprise admin or the system administrator role. As an example, if you’re logged in as a medical asset manager or a medical asset technician, you may see other assets and model categories such as construction, transportation, or facilities. However, you can't create or modify anything in these categories as these are read only.

You can evaluate how effectively your assets are functioning and being used through the reports based on asset key performance indicators in the **Asset performance** tab of the **Asset analytics** view. The asset performance report is also available on the contextual sidebar of the asset record, displayed by selecting the **Asset availability and related KPIs** icon \[![Asset KPI icon](../image/asset-kpi-icon.png)\].

You can receive assets from any workﬂow directly at the stockroom using the unified receiving functionality in the Medical Asset Workspace and Facility Asset Workspace. You can receive assets in any of the following ways:

-   Receive a single asset
-   Receive multiple assets in the shipments
-   Import assets in bulk and receive them

You can also manage supply and demand in your stockrooms effectively with inventory demand reports. To view the reports, follow these steps

1.  Navigate to the **Inventory** view.
2.  Select the **All stockrooms** tab.
3.  Select a stockroom for which you want to view the inventory reports.
4.  Select the **Inventory insights** tab.

## Workspace roles

The workspace that you can access depends on the role with which you log in to your ServiceNow instance. You can only view the workspace for which you have access.

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

Medical Asset Workspace and Facility Asset Workspace

</td><td>

-   Medical asset manager \(sn\_eamhc.medical\_asset\_manager\) and facility asset manager \(sn\_eamhc.facility\_asset\_manager\)
-   Medical asset technician \(sn\_eamhc.medical\_asset\_technician\) and facility asset technician \(sn\_eamhc.facility\_asset\_technician\)
-   Enterprise admin \(sn\_eam.enterprise\_admin\)
-   System administrator \(sys\_admin\)

</td></tr><tr><td>

Medical Asset Workspace, Facility Asset Workspace, and Enterprise Asset Workspace

</td><td>

-   Enterprise admin \(sn\_eam.enterprise\_admin\)
-   System administrator \(sys\_admin\)

</td></tr></tbody>
</table>## Accessing the Admin center

Only the Enterprise admin role and the system administrator role can make configuration changes in the Admin center of the Medical Asset Workspace and the Facility Asset Workspace.

The Medical asset manager, Medical asset technician, Facility asset manager, or Facility asset technician can't make any changes in the Admin center except for the Task rate card and the Labor rate card options under the **TCO configuration** list.

