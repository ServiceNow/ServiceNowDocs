---
title: Using the Safe Workplace Dashboard
description: By using a map, you can review your organization's status regarding personnel and facility readiness to reopen.
locale: en-US
release: zurich
product: Safe Workplace Dashboard
classification: safe-workplace-dashboard
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Safe Workplace Dashboard, Safe Workplace, Health and Safety, Employee Service Management]
---

# Using the Safe Workplace Dashboard

By using a map, you can review your organization's status regarding personnel and facility readiness to reopen.

Focus on alert information regarding user readiness, personal protective equipment \(PPE\) inventory levels, health monitoring results, and active contact tracing cases created for affected users. View status data, by facility, to prepare the reopening of the facility and send invitations to users to return.

The Safe Workplace Dashboard presents data when the correlated Safe Workplace suite , ServiceNow® Contact Tracing, and ServiceNow® Emergency Response Management applications are installed. Verify that configuration is complete so that the application data is included when the ServiceNow® Performance Analytics data collection job runs.

**Note:** Assign Safe Workplace Dashboard users the pa\_viewer role. This role is required to view the dashboard content.

## COVID-19 Global Health Data Set

You can use the COVID-19 Global Health Data Set application at no extra charge. COVID-19 Global Health Data Set is installed with the Safe Workplace Dashboard. It appears as an application in the instance navigation menu, and displays global COVID-19 information on request in the Safe Workplace Dashboard.

![Safe Workplace Dashboard with the Covid-19 Cases switch toggled to show global pandemic data.](../image/swd-covid-toggled-on-28.png "Safe Workplace Dashboard with COVID-19 data")

Navigate to **COVID-19 Global Health Data Set** to view the collected data by date ranges, locations, state/provinces, and countries. Build reports or export the data to use for your own analysis.

|Data source|Description|
|-----------|-----------|
|European Centre for Disease Prevention and Control \(ECDC\)|COVID-19 metrics for the European Union and European Economic Area from the European Centre for Disease Prevention and Control. For more information on this data source, see the [European Centre for Disease Prevention and Control](https://www.ecdc.europa.eu/en/publications-data/download-todays-data-geographic-distribution-covid-19-cases-worldwide) website.|
|Government of Canada Public Health Infobase|COVID-19 metrics for Canada from the Canadian government. For more information on this data source, see the [Government of Canada Public Health Infobase](https://health-infobase.canada.ca/covid-19/) website.|
|Our World in Data \(OWID\)|Worldwide COVID-19 metrics from Our World in Data. For more information on this data source, see the [OWID GitHub](https://github.com/owid/covid-19-data) repository.|
|USA Facts|COVID-19 metrics for the United States from USA Facts. For more information on this data source, see the [USA Facts](https://usafacts.org/visualizations/coronavirus-covid-19-spread-map/) website.|

## Use the Safe Workplace Dashboard

Navigate to **Safe Workplace Dashboard** &gt; **Safe Workplace Dashboard** to open the dashboard in a new browser window.

Locations with alerts are listed on the left. Click the arrow on the card or the location icon to zoom in to the location and its alerts. Use the Region and Site lists at the top left to select specific regions and sites to review.

To add a favorite location, click **Manage Favorites** and search for the location. After you select it, the location name appears in the header \(**R1 S1** in the example image\). Click the location to open it directly. To remove a location from favorites, click **Manage Favorites** again and click the **\(x\)** on the location you want to remove.

**Note:** The Safe Workplace Dashboard shows only PPE inventory and health screening data associated with a Workplace Core campus or building. PPE stockrooms and health screenings must have a Workplace Core campus or building selected in the **Location** field to be displayed on the dashboard. For information about creating Workplace Core campuses and buildings, see [Providing your workplace data](../../workplace-safety-mgmt/concept/providing-your-workplace-data.md).

![Initial view of the Safe Workplace Dashboard pointing to one location that displays the pop-up details.](../image/swd-alerts-icons-popover-28.png "Safe Workplace Dashboard overview page")

Continue drilling down to a facility to see its recent statuses. The New Confirmed COVID-19 Cases widget provides data from the COVID-19 Global Health Data Set.It shows the number of new cases and deaths for the location, and can also show the number of new cases and deaths per 100,000 people if population data for the location is available. For locations in the United States, you can filter the New Confirmed COVID-19 Cases widget to show data at the state or county level. The **Populate OpenStreetMap data** scheduled job retrieves county data for campuses.

![Safe Workplace Dashboard status widgets from all applications.](../image/swd-dashboard-detail-n-28.png "Safe Workplace Dashboard")

Use the information to organize the reopening of the facility and reduce workplace transmission of infectious diseases, such as COVID-19.

-   Order PPE inventory if levels are low.
-   Send an outreach survey to reassess user readiness to return.
-   Verify that the workplace cleaning schedule is on track to reopen safely.
-   Encourage managers to have users make workspace reservations to return.
-   Create cases for affected users and tasks for the follow-up interviews with potentially impacted users.

## Review the Safe Workplace Dashboard Reopening page

View the Safe Workplace Dashboard Reopening page by clicking **Reopening**to see visualizations of reopening data across three widgets:

-   The Location Reopened Status displays what regions are open and shows how many are open by region.
-   Approved Worker Count vs. Avg Daily Check-Ins provides information to help determine whether too few or too many people are being checked in for the current week.
-   The Campus Status widget is a filterable view with an overview of campus locations and metrics such as the current phase, maximum daily occupancy percent, and number of approved workers. You can manually add or edit locations by selecting the campus or clicking **New**.

    **Note:** A location cannot have more than one campus status at a time.


![Safe Workplace Reopening page with reopening, check-in, and campus status metrics.](../image/safe-workplace-reopening-overview-30.png "Safe Workplace Dashboard Reopening page")

To populate the Safe Workplace Dashboard page, create Phase Definitions to track locations through their various phases. Otherwise, no data will display. Updates are performed daily at 23:00 instance time regardless of the number of campuses in your organization and their geographic location.

For each phase, navigate to **Safe Workplace Dashboard** &gt; **Phase Definitions** and click **New** to create customized phases for your organization. You can define their phases with the following information:

-   Names for the phases such as Phases 1, 2, and 3 or red, yellow, and green \(**Name**\)
-   The location the phase applies to \(**Location**\)
-   The maximum daily occupancy percentage \(**Max daily occupancy percent**\)
-   A description of the phase

You can determine your own criteria for what constitutes a check-in. Navigate to **Safe Workplace Dashboard** &gt; **Reopening Check-In Audience** and click **New** to open a new record. Administrators can use the condition builder to define the tables and fields to add to a check-in and mark the Check-In Audience as active.

## Review COVID-19 vaccination metrics in the Safe Workplace Dashboard

Organizations with the Vaccination Status application can use data from the application and public data from the COVID-19 Global Health Data Set to review COVID-19 vaccination metrics across the United States and worldwide. Organizations can then compare their vaccination numbers to public numbers to gain a better understanding of their organization's vaccination efforts.

This data is made available through the Safe Workplace Dashboard Vaccination Widget. The following metrics are available in the Safe Workplace Dashboard Vaccination Widget:

-   The number of people fully vaccinated per 100
-   The number of people vaccinated per 100
-   The number of total vaccination doses per 100

Users with the admin role can add the Safe Workplace Dashboard Vaccination Widget to the Safe Workplace Dashboard Site View. For more information, see [Add a vaccination widget to the Safe Workplace Dashboard](../task/swd-add-vaccination-widget.md).

**Important:** Users must have the sn\_imt\_dashboard.user and sn\_imt\_vaccine.vaccine\_profile\_reader roles to see any vaccination data in the dashboard.

![Safe Workplace Dashboard Vaccination Widget with COVID-19 vaccination data](../image/swd-covid-19-vaccine-widget.png "Safe Workplace Dashboard Vaccination Widget")

Vaccination data is pulled from the last 30 days and includes campus data based on the vaccine responses per location from the **Vaccination Status** application. The widget is scheduled to update automatically once the COVID-19 Global Health Data Set and **Vaccination Status** are installed. Updates are performed daily at midnight \(00:00\) instance time, regardless of the number of campuses in your organization and their geographic location.

**Note:** If data is unavailable or missing, the widget will not display data for that day \(even if available\) until the next day the scheduled jobs run successfully.

-   **[Add a vaccination widget to the Safe Workplace Dashboard](../task/swd-add-vaccination-widget.md)**  
As an admin, add the Safe Workplace Dashboard Vaccination widget to the Safe Workplace Dashboard Site View portal page.

**Parent Topic:**[Safe Workplace Dashboard](safe-workplace-dashboard.md)

