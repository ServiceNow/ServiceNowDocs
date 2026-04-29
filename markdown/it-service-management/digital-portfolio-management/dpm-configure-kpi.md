---
title: KPI groups in Digital Portfolio Management
description: Define and configure the key performance indicator \(KPI\) groups in DPM that matter most to you. When you associate KPI groups with your services and applications, you can analyze their performance in a centralized area.
locale: en-US
release: australia
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Explore, Digital Portfolio Management, IT Service Management]
---

# KPI groups in Digital Portfolio Management

Define and configure the key performance indicator \(KPI\) groups in DPM that matter most to you. When you associate KPI groups with your services and applications, you can analyze their performance in a centralized area.

Use KPI groups. 

With KPI groups, you can analyze the performance of each solution in several ways:

-   See a detailed description of a KPI indicator by selecting ![Description icon.](../../../reuse/icons/product-icons/circle-info-outline-24.svg) on the KPI indicator card.
-   Drill down to view trends and historical performance on vendors, a KPI group, or an individual KPI.
-   Select a supporting KPI to see its related record details.
-   View and drill down into the KPI spark lines to see more details. When you select a chart value, the result is filtered to display the details of the value that you selected. If you select the whole chart \(not a value\), then the KPI details page displays.
-   See the latest \(or last\) KPI score when the **Latest score** system property \(**sn\_dpm.kpi\_groups.show\_latest\_score**\) is enabled.

    View KPI group data in the way that most interests you. Admins can update the system property anytime so you can view KPI group data by the latest score or by the aggregate score. When an admin enables the Latest score system property, the following shows in the DPM:

    -   Last collected score for a KPI indicator in all KPI groups in DPM, without an aggregation layer \(by sum or by average\).
    -   Last collected scores for all values in each KPI breakdown grid.
    -   Last 30 days of scores for trends and time series visualizations. You can set different time rangers per KPI.
    -   The date the score was collected \(shows on each KPI indicator card\).
    **Note:** Starting with the June 2024 release of DPM, the latest score system property is set to true for new and zBoot customers. If not applicable, then the DPM admin can enable the latest score system property by navigating to **All** &gt; **Digital Portfolio Management** &gt; **Administration** &gt; **KPI groups properties**. For more admin information, see [Configure the Digital Portfolio Management experience](../task/dpm-configure-experience.md).

    When you access KPI drill down information in DPM, the system adds a timestamp at the end of the URL in the browser address field. The timestamp is in milliseconds and is based off epoch time.


The DPM base system comes with KPI groups that provide valuable indicators to evaluate overall performance and individual metrics for services and other solutions. You can also create your own KPI groups but you're encouraged to explore the base system options.

## KPI groups for enterprise portfolios

Two KPI groups enable flexible reporting on solutions in enterprise portfolios.

-   **Enterprise portfolio**

    The enterprise portfolio KPI group \[**Portfolio success metrics**\] enables you to map to any enterprise portfolio type to view its portfolio performance. You can track availability, mean time to resolve \(MMTR\), incidents caused by changes, and successful changes. You can see these performance metrics when you view the details of any enterprise portfolio.

-   **Business applications**

    The business application KPI group type \[**Business application performance**\] enables you to track the number of incidents, problems, and changes for a business application. You can see these performance metrics in the **Run** tab of a business application on the DPM Workspace.

    **Important:** You must map the business application performance KPI group to your business applications to show the data on the **Run** tab. For more information, see [Create KPI groups and mappings in Digital Portfolio Management](../task/dpm-create-kpi-groups.md).


**Note:** The business application performance KPI group replaces the metrics used prior to the Utah release. Since you can create and edit KPI groups and map them to business applications, it provides more flexibility to configure your reporting. You don't need to edit the page in UIB to change the metrics.

## KPI groups for service instances

KPI groups aren’t inherited for service instances, but you can do the following with the **Availability insights** KPI group for service instances:

-   View and assess the availability for service instances that you own or are responsible for.
-   Map the Availability insights KPI group to one-to-many applications services.
-   View availability commitments and commitment performance on the Run tab of your service instance.
-   View all commitments listed on the Info tab of the service instance.

**Parent Topic:**[Exploring Digital Portfolio Management](dpm-explore-cfw.md)

**Related topics**  


[Update KPIs in Digital Portfolio Management](../task/dpm-kpi-descriptions.md)

[Navigate portfolio types in Digital Portfolio Management](dpm-navigating-enterprise-portfolios.md)

[KPI groups installed with Digital Portfolio Management](../reference/dpm-kpi-groups-oob.md)

[Create KPI groups and mappings in Digital Portfolio Management](../task/dpm-create-kpi-groups.md)

[Configure KPIs in Digital Portfolio Management with service availability example](../task/dpm-configure-kpi-availability.md)

