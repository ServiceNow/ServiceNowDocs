---
title: Use the Admin Center in Digital Portfolio Management
description: The Admin Center in Digital Portfolio Management \(DPM\) provides administrators a guided walk-through to set up and configure the DPM Workspace for the organization. The provided information and configuration prompts enable visibility into the end-to-end service and application life-cycle.
locale: en-US
release: xanadu
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configuring Digital Portfolio Management, Digital Portfolio Management, IT Service Management]
---

# Use the Admin Center in Digital Portfolio Management

The Admin Center in Digital Portfolio Management \(DPM\) provides administrators a guided walk-through to set up and configure the DPM Workspace for the organization. The provided information and configuration prompts enable visibility into the end-to-end service and application life-cycle.

With a DPM admin role \[sn\_dpm.dpm\_admin\], access the DPM Admin Center to set up and configure the DPM experience for the organization. The Admin Center provides easy to follow setup steps and includes tooltips and links to resources, plugins, and configuration tables.

**Note:** An administrator \[admin\] must install plugins.

## Access the DPM Admin Center

To access the DPM Admin Center, you must have the DPM Admin role \[sn\_dpm.dpm\_admin\].

**Note:** Demo data users that come with the base system have been assigned the Admin role \[sn\_dpm.dpm\_admin\]. You can impersonate one of the demo data users to test the Admin Center.

Navigate to **All** &gt; **Digital Portfolio Management** &gt; **DPM Admin Center**.

The Admin Center has two tabs: **Overview** and **Settings**.

## Overview tab

![DPM Admin Center Overview tab](../image/dpm-admin-center-overview.png)

The **Overview** tab enables you to do the following:

-   Follow the guided setup to configure services with offerings, business applications, and application services.
-   Configure key performance indicator \(KPI\) groups.
-   Explore the settings.
-   Create and review service portfolios.
-   Create and review business application portfolios.
-   Access helpful resources for more information.

## Navigate the configuration steps

-   Select **Configure** on a solution card from the **Overview** tab.
-   Follow the guided walk-though. Each step has its own prompts, instructions, and conditions to set up your data in the DPM Workspace.

    **Note:** When you see the information icon \(![Information icon.](../../../administer/on-call-scheduling/image/icon-information.png)\) next to a step heading, select it to view more information about that step.

<table id="table_o4d_thj_1dc"><thead><tr><th>

Services with offerings

</th><th>

Business applications

</th><th>

Application services

</th></tr></thead><tbody><tr><td>

1.  Identify solutions
2.  Identify portfolios
3.  Assess planning items
4.  Assess build metrics
5.  Map KPI groups
6.  Next steps


</td><td>

1.  Identify solutions
2.  Identify portfolios
3.  Assess planning items
4.  Assess build metrics
5.  Map KPI groups
6.  Assess risk metrics
7.  Next steps


</td><td>

1.  Identify solutions
2.  Identify portfolios
3.  Map KPI groups
4.  Assess risk metrics
5.  Next steps


</td></tr></tbody>
</table>-   Navigate through the setup steps in one of two ways.
    1.  Select the step number and title to perform the configuration for that step.

        A completed step shows a check mark instead of a number.

    2.  Select **Next** to move to the next step and **Back** to return to the previous step.

![Example DPM Admin Center navigation using the business applications setup.](../image/dpm-admin-center-nav.png "Example DPM Admin Center navigation using the business applications configuration steps")

You can navigate to any step at any time to update the configuration settings.

**Important:** If you see an empty screen while configuring, you most likely don't have access for that action. To resolve access issues, contact your administrator.

## Settings tab

![DPM Admin Center Settings tab](../image/dpm-admin-center-settings.png)

The **Settings** tab enables you to do the following for solutions \(services, service offerings, business applications, and application services\):

-   Configure the following for each solution page.
    -   Personal portfolio solution cards
    -   Header fields
    -   Plan fields
    -   Build fields
    -   Run fields
    -   Risk fields
    -   Portfolio properties
    -   General information fields on the Info tab
    -   KPI group properties
    -   DevOps properties
-   Show or hide the Plan, Build, Run and Info tabs.
-   Show or hide fields from each of the main tabs.
-   Access resources for additional help.

## Troubleshoot tab

![DPM Admin Center Troubleshoot tab](../image/dpm-admin-center-troubleshoot.png)

The **Troubleshoot** tab enables you to recalculate availability results and indicators for service offerings.

1.  Select the services and offerings that you'd like to recalculate availability.
2.  Set the start and end dates for the recalculation period.
3.  Select **Recalculate availability** to generate the results.

There’s no limit to how many times you can run the recalculation. You can also check the recalculation progress by selecting **Check status in the event log**.

## More options in the DPM Admin Center

-   **[Configure page headers in the DPM Admin Center](../task/dpm-configure-page-headers.md)**  
Configure the page header fields for your solutions in the DPM Admin Center. Your configuration determines how the header fields are displayed in the DPM Workspace.
-   **[Configure the Info tab in the DPM Admin Center](../task/dpm-configure-info-tab.md)**  
Configure the general information fields for your solutions in the DPM Admin Center. Your configuration determines how the fields are displayed in the **General info** section of the **Info** tab in the DPM Workspace.
-   **[Configure personal portfolio solution cards in the DPM Admin Center](../task/dpm-configure-solution-cards.md)**  
Configure the fields that display on the personal portfolio solution cards in the DPM Admin Center. Your configuration determines the fields that display on each solution card in the DPM Workspace.
-   **[View relationships of business applications and application services in the DPM Admin Center](dpm-view-related-records.md)**  
In the DPM Admin Center, you can see a comprehensive view of your business applications and application services. You can see incidents, problems, and changes that are related to your business applications and incidents and changes that are related to your application services.

**Parent Topic:**[Configuring Digital Portfolio Management](dpm-configure-cfw.md)

