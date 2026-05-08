---
title: Sustainable IT dashboard
description: The Sustainable IT dashboard displays a variety of information to easily gauge the sustainability impact of the IT assets of an organization.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Managing Sustainable IT, Explore, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Sustainable IT dashboard

The Sustainable IT dashboard displays a variety of information to easily gauge the sustainability impact of the IT assets of an organization.

The Sustainable IT dashboard displays data for Hardware assets, datacenters, and your organization's IT footprint on the world map. Datacenters refer to the facilities that house the IT infrastructure. All these tabs are explained in the following sections.

**Note:** To view the **Hardware assets** tab and the **Data centers** tab on the dashboard, you must activate the Hardware Asset Management \(sn\_hamp\) plugin. Additionally, to activate the **IT footprint map** tab, you must activate the Geo Map component \(sn\_geo\_map\) plugin. For more information on the required Geo Map component, see the [Understanding Google Maps APIs in geo-map component \[KB1588661\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1588661) article in the Now Support knowledge base.

## IT footprint map

The first tab on the Sustainable IT dashboard showcases a global map depicting the carbon footprint of your datacenters, office buildings, and so on, highlighting your most energy-efficient facilities. The data displayed is determined by the configuration that you configure on the map marker. For more information, refer to [Configure a map marker](../task/configure-map-markers.md). When you hover over the icons on the map, you can view the classification of the configured marker's efficiency, the metric name, the entity name, and the most recent metric data available. You can configure any of the metric definitions that are provided along with the Sustainable IT plugin. Only those metric definitions that are grouped under Sustainable IT are available for selection. For example, you can use the following the metric definitions:

-   **Carbon intensity for office locations**
-   **DCiE by data center**

    **Note:** DCiE stands for datacenter infrastructure efficiency.


For more information on how you can filter the metric definitions that are grouped under Sustainable IT, refer to [Filter Sustainable IT metric definitions](../task/filter-sustainable-it-metric-definitions.md).

When you move the cursor over the icon, a popover is displayed. On the popover, you can select the entity name and a side panel opens that shows the metrics related to the selected entity of the following metric definitions.

-   PUE by Data Center
-   WUE by Data Center
-   CUE by Data Center
-   CO2e emissions from energy usage
-   Total energy used
-   Hardware energy consumption by location
-   CO2e from hardware assets by location

You can select **Open link** to navigate to the metric record page for details. An entity class filter on the right side of the dashboard is available to select the data that you want to view.

## Hardware assets

**Overview**: In the overview section, you can see the Trend chart that displays the data for the following metric definitions:

-   Carbon emissions from hardware assets.
-   Hardware energy consumption.

You can select the chart to further explore or delve into more detailed information or data related to the chart. The fields from where the data is obtained are specified in the metric definition form. For more information, see [Create an automated metric definition](../../metrics/task/create-metric-definition.md).

**Energy consumption**: The energy consumption section displays the information in the subsequent formats:

-   Total energy consumption \(kWh\): This figure represents the total energy consumption for the **Hardware energy consumption by model category** metric definition. Hardware energy consumption by model category refers to the amount of energy or power consumed by different categories of hardware. Hardware model category refers to various types of devices, such as computers, servers, or other devices. The configuration of the metric definition includes specifying the model category column in the hardware table for the purpose of data collection.
-   Energy consumption by model category \(kWh\) or location: This horizontal bar graph displays the energy consumption data. You can filter the data either by the **Location** filter or the **Model category** filter. You have the option to sort the bar chart in either ascending or descending order using the available filters. If you drill down on this bar chart, a new page opens that displays further details about the assets that are in use and that consume maximum energy. By default, this new page shows all the assets of the first bar in the chart at the bottom and shows the top models by energy consumption on the right.
-   Energy star assets: The dial chart showcases the number of energy star-certified assets out of the total number of assets.

**Emissions**: Within the emissions section, the data is presented in the following format.

-   Total emission \(days\): You can view both the total emissions value and the variation in emissions when compared to the previous month.
-   Emissions by model category or by location \(days\): This horizontal bar graph displays the emissions data. You can filter the data either by the **Location** filter or the **Model category** filter. You have the option to sort the bar chart in either ascending or descending order using the available filters. If you drill down on this bar chart, a new page opens that displays further details about the assets that are in use and that generate maximum emissions. By default, this new page shows all the assets of the first bar in the chart at the bottom and shows the top models by emissions on the right. The data that is displayed depends on the selection you make in the filters, that is, whether you selected Location or Model category.

**E-waste reused, donated, or landfilled**: In this section, the data is presented in the following format:

-   Retired assets \(lbs\): The donut chart displays the number of assets reused, donated, and disposed.
-   Landfills \(lbs\): The pie chart in this section displays the weight of hardware assets, by model categories, that have been disposed. This weight is in pounds.

The data for this section is obtained from the Hardware asset table. Each chart is interactive, enabling you to select specific segments to access more detailed information.

## Data centers

**Overview**: In the overview section, you can view the Trend chart that displays the data for the following metric definitions:

-   Co2e from energy usage
-   Total energy used

You can select the chart to further explore or delve into detailed information about the energy use or emission for each data center. The overview section also displays the number of data centers from where the data for emissions and energy is sourced. You can also see the top three greenest data centers based on the DCiE where the data center with the highest DCiE is ranked at the top. Greenest data centers refer to data centers have the minimum amount of emissions.

**Data center efficiency**: In the data center efficiency section, the data is presented in the following formats:

-   Power usage effectiveness: Power Usage Effectiveness \(PUE\) is a metric used to assess the energy efficiency of a data center. It’s a ratio that quantifies the amount of energy consumed by a data center facility compared to the energy used by the IT equipment it houses.
-   Water usage effectiveness \(KgCO2e\): Water Usage Effectiveness \(WUE\) is a metric used to evaluate the water efficiency of a data center or a facility. Similar to Power Usage Effectiveness \(PUE\), which measures energy efficiency, WUE quantifies the amount of water consumed by a data center facility in relation to the water used by the IT equipment.
-   Carbon usage effectiveness \(KgCO2e/kWh\): Carbon Usage Effectiveness \(CUE\) is a metric used to assess the carbon efficiency and sustainability impact of a data center or facility. It quantifies the number of carbon dioxide emissions produced per unit of IT load or computing work performed by the data center.

**Energy consumption**: Within the energy consumption section, the information is displayed in the subsequent formats:

-   Total energy consumption \(kWh\): This figure represents the combined energy consumption of all the data centers. It provides an overview of the overall energy usage across all the data centers.
-   Total energy consumption by source: A donut chart is used to illustrate the distribution of energy consumption in kilowatt hours \(kWh\) from different energy sources. The energy sources are specified in the form of metric definitions. Each section of the semi donut chart is interactive, enabling you to select specific segments to access more detailed information.
-   Energy consumption by data centers \(kWh\): The bar chart showcases the energy consumption for each individual data center, considering all the active metric definitions. You have the option to sort the bar chart in either ascending or descending order using the available filters. This enables you to analyze and compare the energy usage of different data centers more effectively.

**Emissions**: In the emissions section, the data is presented in the following formats:

-   Total emissions \(KgCO2e\): This figure represents the total emissions for all the data centers.
-   Emissions by data center \(KgCO2e\): The bar chart showcases the emissions for each individual data center, considering all the active metric definitions. You can use the provided filters to sort the bar chart in either ascending or descending order. Additionally, each bar of the bar chart is interactive, enabling you to select specific segments to access more detailed information.

**Note:** The data is aggregated by using the summation method.

## Digital end-user experience

The Digital End-User Experience \(DEX\) tab on the Sustainable IT Dashboard integrates real-time energy consumption data from DEX into the dashboard. This integration enhances the accuracy and reliability of sustainability reporting for IT assets, particularly desktops and laptops. By leveraging real-time usage data from DEX, organizations can move beyond estimated hardware energy metrics and promote a more precise calculation of CO₂e emissions.

**Overview**: In the overview section, you can see the Trends chart that displays the data for the following metric definitions:

-   Real time CO2e Emissions by Models
-   Real-time Energy Consumption by Models

You can select the chart to further explore or delve into more detailed information or data related to the chart. The fields from where the data is obtained are specified in the metric definition form. For more information, see [Create an automated metric definition](../../metrics/task/create-metric-definition.md). In the overview section, you can also see the Asset coverage, which displays the number of assets from where the usage and consumption data is sourced. You can select the asset number to further explore or delve into more detailed information into the asset details.

**Energy consumption**: Within the energy consumption section, the information is displayed in the subsequent formats:

-   Total energy consumption \(kWh\): This figure represents the combined energy consumption of all the assets. It provides an overview of the overall energy usage across assets.
-   Energy consumption by models \(kWh\): The bar chart showcases the energy consumption for assets by brand model or location of that asset. Each bar of the bar chart is interactive, enabling you to select specific segments to access more detailed information. The available filters enable you to analyze and compare the energy usage of different models more effectively. You have the following filters available:
    -   Use the Group by filter to group data by asset location or asset models.
    -   Use the Sort by filter to sort the data in ascending or descending order.
    -   Use Filter by model to view data for only selected models.
-   Energy consumption breakdown: The dial chart displays the energy consumption breakdown by asset components, including central processing unit \(CPU\), network, energy loss, display, and others.

**Emissions**: In the emissions section, the data is presented in the following formats:

-   Total emissions \(KgCO2e\): This figure represents the total emissions for all the assets.
-   Emissions by models \(KgCO2e\): The bar chart showcases the emissions for assets by brand model or location of that asset. Each bar of the bar chart is interactive, enabling you to select specific segments to access more detailed information. You have the following filters available:
    -   Use the Group by filter to group data by asset location or asset models.
    -   After selecting the group as location, you can use filter by location to view data for only selected locations.
    -   Use the Sort by filter to sort the data in ascending or descending order.
    -   Use Filter by model to view data for only selected models.

For more information on DEX, see Digital End-User Experience.

**Parent Topic:**[Managing Sustainable IT](managing-sustainable-it.md)

