---
title: Security Incident Response Overview dashboard
description: The Security Incident Response Overview dashboard provides an executive view into security incident activity, providing trends and reports, and drill-downs into specific data.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Visual representation of Security Incident Response reporting, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response Overview dashboard

The Security Incident Response Overview dashboard provides an executive view into security incident activity, providing trends and reports, and drill-downs into specific data.

The Overview module displays security incident information that is tailored to the role of the user. You can point to any part of a chart \(bar, pie, data point, heatmap, and so on\) to view general data specific to that part. See the following image. If you click any part of a report, a list opens to provide detailed information.

![Sample report from Security Incident Manager Overview](../image/TrendAllSecIncidents.png "Trend of All Security Incidents")

## Security Incident Manager Overview

Users with the Security Incident Administrator and Security Incident Manager roles view the Security Incident Manager Overview. It contains the following reports in the base system.

|Name|Visual|Description|
|----|------|-----------|
|Team Critical Security Incidents|Single score|The number of critical security incidents assigned to the team.|
|Team High Security Incidents|Single score|The number of high security incidents assigned to the team.|
|SLAs expiring within 24 hours|Single score|The number of SLAs that expire within the next 24 hours.|
|Risk vs Severity|Heatmap|The distribution of security incidents assigned to the team by risk and severity.|
|Security Incidents by CI Class, last 3 months|Bar chart|The count of security incidents assigned to the team by configuration item class.|
|Trend of All Security Incidents|Trend|Plots the count of the number of security incidents received by category or priority.|
|Unauthorized Access Security Incidents|Bar chart|Displays the types of security incident categories received over time.|
|Average Time to Contain|Single score|The average time it takes to contain all security incidents.|
|Average Time to Contain Critical|Single score|The average time it takes to contain all critical security incidents.|
|Average Time to Identity|Single score|The average time it takes to identify all security incidents.|

## Security Analyst Overview

Users with the Security Incident Analyst role view the Security Analyst Overview. It contains the following reports in the base system.

|Name|Visual|Description|
|----|------|-----------|
|My Critical Priority Work|Single score|The number of critical security incidents assigned to me.|
|My High Priority Work|Single score|The number of high security incidents assigned to me.|
|My SLAs expiring within 24 hours|Single score|The number of SLAs assigned to me that expire within the next 24 hours.|
|Security Incidents assigned to me|Bar chart|Security Incidents assigned to me by incident state or category.|
|Work assigned to me by Type|Bar chart|Security tasks \(incidents, tasks, or requests\) assigned to me by type or priority.|
|Security Incidents, Requests, Tasks assigned to me|List|A list of all security incidents, security requests, and tasks assigned to me.|
|Security Incident Location|Map|Regional location of the security incidents.|
|Count|Map|Number of security incidents per region.|
|Min/Max Count|Color Spectrum Bar|The minimum and maximum numbers of security incidents per region represented by a color spectrum bar.|
|Percentage of Count|Map|Percentage of the total incident count per region.|

## Security Incident CISO Overview with Security Incident Analytics activated

When the Security Incident Analytics plugin is activated, users with the Security Incident CISO and System Administrator roles view the Security Incident CISO Overview. The following CISO reports are provided in the base system.

|Name|Visual|Description|
|----|------|-----------|
|New Security Incidents This Week|Single score|The number of new security incidents received in the current week.|
|Security Incidents Closed This Week|Single score|The number of security incidents closed in the current week.|
|New Security Incidents \(Running 7 Days\)|Single score|The number of security incidents opened within the last 7 days.|
|Security Incidents Closed \(Running 7 Days\)|Single score|The number of security incidents closed within the last 7 days.|
|Daily New Security Incidents vs Closed Security Incidents|Trend|New and Closed security incident counts over time by day.|
|Weekly New Security Incidents vs Closed Security Incidents|Trend|New and Closed security incidents over time by week.|
|Security Incident Close Code|Trend|Full count of closure codes over time.|
|Security Incident Business Impact|Treemap|Business services with security incidents with available groupings by business criticality.|
|Average Time to Contain \(Weekly\)|Trend|The 7-day average time it takes to contain a security incident over time.|
|Average Time to Eradicate \(Weekly\)|Trend|The 7-day average time it takes to eradicate a security incident over time.|
|Average Time to Identity \(Weekly\)|Trend|The 7-day average time it takes to identify a security incident over time.|
|Security Incident Location|Map|Regional location of the security incidents.|
|Count|Map|Number of security incidents per region.|
|Min/Max Count|Color Spectrum Bar|The minimum and maximum numbers of security incidents per region represented by a color spectrum bar.|
|Percentage of Count|Map|Percentage of the total incident count per region.|

## Security Incident CISO Overview without Security Incident Analytics activated

When the Security Incident Analytics plugin is not activated, users with the Security Incident CISO and System Administrator roles view the Security Incident CISO Reporting Overview. The following CISO reports are provided in the base system.

|Name|Visual|Description|
|----|------|-----------|
|New Security Incidents This Week|Single score|The number of new security incidents opened in the current week.|
|Security Incidents Closed This Week|Single score|The number of security incidents closed in the current week.|
|New Security Incidents \(Running 7 Days\)|Single score|The number of security incidents opened within the last 7 days.|
|Security Incidents Closed \(Running 7 Days\)|Single score|The number of security incidents closed within the last 7 days.|
|Weekly New Security Incidents|Trend|The new security incidents opened on a weekly basis.|
|Weekly Closed Security Incidents|Trend|The security incidents closed on a weekly basis.|
|Security Incident Close Codes|Trend|Security incident close codes over time.|
|Business Services with Security Incidents - Business Impact|Treemap|Business services with security incidents with available groupings by business criticality.|
|Average Time to Contain|Single score|The average time it takes to contain all security incidents.|
|Average Time to Contain Critical|Single score|The average time it takes to contain all critical security incidents.|
|Average Time to Identity|Single score|The average time it takes to identify all security incidents.|

**Note:** The Security Incident Response base system includes Performance Analytics Solutions for displaying preconfigured best practice dashboards. The dashboards present important metrics for analyzing your Security Incident Response process, such as new security incidents or the average age of open security incidents. For more information and installation instructions, see [Security Incident Response Platform Analytics Solutions](../../../use/dashboards/application-content-packs/security-incident-content-pack.md).

-   **[Access Security Incident Response Explorer](../task/access-sec-in-resp-explorer.md)**  
You can access the Security Incident Response Explorer dashboard to view security incident activity in order to instantly pinpoint areas of concern and quickly resolve issues.
-   **[Security incident map](c_SecurityIncidentGeoHeatmap.md)**  
The security incident map provides data by geographical location. The world map is highlighted in every area in which an incident occurs. When the Security Incident Analytics plugin is activated, you can add the security incident map to the Security Incident Response overview. After it has been added, you can configure the map by modifying the map filters.
-   **[Security incident treemaps](c_ConfigureTreemaps.md)**  
When the Security Incident Analytics plugin is activated, you can add the security incident - service impact and security incident - real-time treemaps to the Security Incident Response overview. After they have been added, you can configure the treemaps by modifying treemap categories and indicators.
-   **[Add vulnerability significance charts to an overview](../task/t_AddVulnSignTreemaps.md)**  
If the Vulnerability Response plugin is activated, you can add vulnerability significance definition charts and other visualizations to the Overview.

**Parent Topic:**[Visual representation of Security Incident Response reporting](c_SIRHomepage.md)

