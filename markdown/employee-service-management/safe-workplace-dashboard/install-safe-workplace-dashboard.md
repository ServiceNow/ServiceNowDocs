---
title: Install the Safe Workplace Dashboard
description: Install the Safe Workplace Dashboard application. You can install this application If you have the admin role.Components are installed with the Safe Workplace Dashboard, including user roles, scheduled jobs, and tables.Set up Safe Workplace Dashboard properties to add your Mapbox API token and configure how indicators are displayed across timezones.The Safe Workplace Dashboard comprises ServiceNow Service Portal widgets that are populated by Performance Analytics widgets.
locale: en-US
release: australia
product: Safe Workplace Dashboard
classification: safe-workplace-dashboard
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Safe Workplace Dashboard, Safe Workplace, Health and Safety, Employee Service Management]
---

# Install the Safe Workplace Dashboard

Install the Safe Workplace Dashboard application. You can install this application If you have the admin role.

## Before you begin

Ensure that the application and all of its associated ServiceNow® Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

The Map existing campus with locations fix script creates the initial mapping entries between the Campus \[sn\_wsd\_core\_campus\] table and the Location \[cmn\_location\] table.

**Note:** Check that all existing campuses have sites and regions populated before running this script.

Use the default setting **active=false** to avoid incorrect mappings in the Campus \[sn\_wsd\_core\_campus\] table.

Run this script after activating the Safe Workplace Dashboard \(sn\_imt\_dashboard\) plugin and ensuring that your existing campuses have sites and regions populated.

After running the Map existing campus with locations fix script, validate that all campuses and locations are accurate. For inaccurate data, remove entries and see [Manually map a location and campus](man-create-campus.md) for more information.

Role required: admin

<table id="table_kxr_yz3_blb"><thead><tr><th>

Type

</th><th>

Instructions

</th></tr></thead><tbody><tr><td>

Commercial on-premise

</td><td>

Visit the ServiceNow® Store to download and install the application.

</td></tr><tr><td>

Federal hosted

</td><td>

See the [Federal downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030260\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030260) article in the Store Help Center for more information.

</td></tr><tr><td>

Federal on-premise

</td><td>

If you are a federal on-premise customer and you would like to install this application, reach out to your sales representative or open a Now Support or HIWAVE ticket. In the ticket, request to be routed to the SHOT team.

 See the [Federal downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030260\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030260) article in the Store Help Center for more information.

</td></tr><tr><td>

On-premise

</td><td>

See the [Commercial downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030258\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030258) article in the Store Help Center for more information.

</td></tr></tbody>
</table>The Safe Workplace Dashboard application requires the ServiceNow® Performance Analytics - Premium application. If you're not already subscribed to Performance Analytics - Premium, you must install it before installing Safe Workplace Dashboard.

If you've subscribed to the Safe Workplace suite and you already have some of the apps installed, refer to the following order of installation for the remaining apps.

-   Emergency Outreach \(sn\_imt\_checkin\)
-   Employee Health Screening \(sn\_imt\_monitoring\)
-   Workplace PPE Inventory Management \(sn\_imt\_ppe\)
-   Employee Readiness Surveys \(sn\_imt\_readiness\)
-   COVID-19 Global Health Data Set \(sn\_imt\_c19datafeed\)
-   Contact Tracing \(sn\_imt\_tracing\)
-   Emergency Self Report \(sn\_imt\_quarantine\)
-   Workplace Core \(sn\_wsd\_core\)
-   Safe Workplace Dashboard \(sn\_imt\_dashboard\)
-   Emergency Response Management for Now Mobile \(sn\_imt\_mobile\)
-   Employee Travel Safety \(sn\_imt\_travel\)
-   Health and Safety Testing \(sn\_imt\_health\_test\)
-   Vaccination Status \(sn\_imt\_vaccine\)

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search field.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release note information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    If your application requires other applications, install them first if they're not already installed.

    Installing your application also automatically installs the dependent applications or plugins if they're not already installed.

5.  If demo data is available and you want to install it, click **Load demo data**.

    Some applications include demo data, which are sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Note:** If you don't load the demo data for a store application during installation, it's not available to load later.

6.  Click **Install**.

7.  When the installation is complete, click **Close**.


**Parent Topic:**[Safe Workplace Dashboard](../concept/safe-workplace-dashboard.md)

## Components installed with the Safe Workplace Dashboard

Components are installed with the Safe Workplace Dashboard, including user roles, scheduled jobs, and tables.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

### Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Safe Workplace Dashboard user\[sn\_imt\_dashboard.user\]

</td><td>

View the dashboard information and drill into locations.

</td><td>

pa\_viewer

</td></tr><tr><td>

Safe Workplace Dashboard administrator\[sn\_imt\_dashboard.admin\]

</td><td>

Manage alert types and set system properties.

</td><td>

sn\_imt\_dashboard.user

</td></tr></tbody>
</table>### Scheduled Safe Workplace Dashboard data collector jobs installed

The data collector jobs installed with the Safe Workplace Dashboard are set to run daily and collect data for use in the dashboard and its widgets.

|Scheduled job|Description|
|-------------|-----------|
|\[PA Workplace Service Delivery\] Daily Data Collection|Collects metrics from Safe Workplace suite apps starting from the previous day to the current day. A user with the pa\_data\_collector role can change the parameters.|
|Aggregate campus status data|Collects data from check-ins and campus statuses to populate the Reopening Check-In Count \[sn\_imt\_dashboard\_reopening\_checkin\_count\] table. Runs daily at 23:00 instance time.|

### Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Alerts\[sn\_imt\_dashboard\_alerts\]

</td><td>

Alerts by campus, generated from active alert types.

</td></tr><tr><td>

Alert Types\[sn\_imt\_dashboard\_alert\_types\]

</td><td>

Alert types are PA thresholds below which an alert is generated and displayed on the Safe Workplace Dashboard.

</td></tr><tr><td>

Breakdown All Time Values \[sn\_imt\_dashboard\_campus\_all\_time\_values\]

</td><td>

PA breakdown values, stored by campus.

</td></tr><tr><td>

Phase Definitions\[sn\_sw\_planner\_phase\]

</td><td>

Definitions of phases and their assigned locations. Used to categorize what phase of reopening a location is in. A location can be in only one phase at a time. A phase has a name, location, description, and allowed maximum occupancy percentage that is allowed during the phase. Phase definitions are required for information to populate widgets in the Safe Workplace Dashboard Reopening page.

</td></tr><tr><td>

Campus Statuses\[sn\_sw\_planner\_campus\_status\]

</td><td>

Primary table containing data that determines the current status of each location in the reopening page and widgets of the Safe Workplace Dashboard.

</td></tr><tr><td>

Reopening Check-In Audience\[sn\_imt\_dashboard\_reopening\_checkin\_audience\]

</td><td>

Table containing check-in audiences and their criteria based on the organization's configurations. Administrators can create Check-In Audiences using the condition builder to create users. Users are uniquely counted across tables even if they have the same user ID. Check-In Audiences are required to provide information to populate widgets in the Safe Workplace Dashboard Reopening page.

</td></tr><tr><td>

Reopening Check-In Count\[sn\_imt\_dashboard\_reopening\_checkin\_count\]

</td><td>

The Aggregate campus status data scheduled job automatically populates the table with the dates and locations of all check-ins.

</td></tr><tr><td>

Campus Status Log\[sn\_imt\_dashboard\_reopening\_campus\_status\_log\]

</td><td>

Tracks campus statuses and how a location's status changes through each phase.

</td></tr></tbody>
</table>## Safe Workplace Dashboard properties

Set up Safe Workplace Dashboard properties to add your Mapbox API tokenand configure how indicators are displayed across timezones.

You can obtain a token from Mapbox to add features to the Safe Workplace Dashboard map. The base system map is from OpenStreetMap, a collaborative, open source map application.

Mapbox requires a subscription, and their documentation site describes how to obtain an API token to add the extra features. For more information, open the [Mapbox](https://www.mapbox.com/) web site and select **Documentation** in the header.

To set properties , navigate to **Safe Workplace Dashboard** &gt; **Properties**.

<table id="table_ksz_ys4_wlb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enter your Mapbox API Token to enable additional Mapbox features. Obtain an API token from https://www.mapbox.com/.\[sn\_imt\_dashboard.Mapbox Token\]

</td><td>

Obtain a Mapbox token to add display features to the Safe Workplace Dashboard. This setting is optional.-   Type: **text**
-   Default value: **none**
-   Location: **Safe Workplace Dashboard** &gt; **Properties**
-   Learn more: Read the documentation on the Mapbox website.

</td></tr><tr><td>

Use Indicator PA job timezone\[sn\_imt\_dashboard.Use Indicator Job Timezone\]

</td><td>

When enabled, the Performance Analytics \(PA\) indicators shown on the Safe Workplace Dashboard are displayed using the time zone of the indicator's data collection job. If the indicator job time zone is not set, the instance time zone is used instead. The indicators are displayed identically for all users viewing the dashboard, regardless of the user's time zone.When not enabled, the PA indicators are displayed based on the user's time zone. The indicators may show different daily data to users in different time zones. For example, an event occurs in the evening in Seattle, which is the next day's morning in Berlin. A user in Seattle sees the event in the data for October 5, while a user in Berlin sees the event in the data for October 6.

</td></tr></tbody>
</table>## Safe Workplace Dashboard widgets

The Safe Workplace Dashboard comprises ServiceNow® Service Portal widgets that are populated by Performance Analytics widgets.

### Service Portal widgets in the Safe Workplace Dashboard

-   Active Contact Tracing Cases
-   Safe Workplace Dashboard Announcement
-   Safe Workplace Dashboard Survey Sentiment
-   Safe Workplace Dashboard Favorite Location
-   Safe Workplace Dashboard Filter
-   Safe Workplace Dashboard Employee Health
-   Safe Workplace Dashboard Main Summary
-   Safe Workplace Dashboard Site Details
-   Safe Workplace Dashboard Main
-   Safe Workplace Dashboard Overview Maps
-   Safe Workplace Dashboard Site Details Ba
-   Safe Workplace Dashboard PA
-   Safe Workplace Dashboard Survey Donut
-   Safe Workplace Dashboard Alerts
-   Safe Workplace Dashboard Menu
-   Safe Workplace Dashboard Vaccination Widget

For information about customizing Service Portal widgets, see [Service Portal widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/service-portal-widgets.md) and the [Widget developer guide](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/widget-dev-guide.md).

### Performance Analytics widgets

-   Active Cases
-   Number of Workplace Reservable Spaces
-   Employees Rejected % Change from Prior Day
-   Number of Employees Ready to Return
-   Number of Employees Not Ready to Return
-   Number of employees rejected
-   % of Employees That Want To Return To Work
-   Reserved Spaces
-   Number of employees surveyed for readiness return
-   PPE Inventory \(time series\)
-   PPE Inventory \(score\)
-   Number of Workplace Spaces
-   Reservable vs Reserved Spaces
-   Number of employees admitted Workplace Reservations
-   Reservable Spaces
-   Employees Admitted
-   Employee Entry Health Monitoring
-   Employees Rejected
-   Number of Workplace Reserved Spaces
-   PPE Inventory % Change from Prior Day

For information about using Performance Analytics, see [Performance Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/pa-overview.md).

