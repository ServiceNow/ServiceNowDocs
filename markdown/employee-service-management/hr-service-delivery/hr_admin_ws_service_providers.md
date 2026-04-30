---
title: Admin Workspace for Service Providers overview
description: HR Admin Service Provider is a consolidated view of customers service usage and consumption, which gives service provider admins the opportunity to make data driven decisions.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-02-04"
reading_time_minutes: 3
breadcrumb: [HR Service Delivery, Employee Service Management]
---

# Admin Workspace for Service Providers overview

HR Admin Service Provider is a consolidated view of customers service usage and consumption, which gives service provider admins the opportunity to make data driven decisions.

SP admins can perform the following functions:

-   View different aspects of the service consumption such as the number of services consumed per customer and the ticket volume per service.
-   View customer details including the number of services and HR users.
-   Access quick links related to daily work tasks such as domain and customer creations, and user management.
-   Access quick links for specific domain on the customer details page.

    **Note:** SP Admin \(sn\_sp\_admin\_ws.admin\) can access workspace and see a consolidated view of the demand and consumption of services offered to customers. This enables data driven decision making and access to portfolio level links.


Admin Workspace for Service Providers gives SP admins a centralized workspace to see a consolidated view of the demands and consumption of services offered to customers using KPIs.

|Page|Description|
|----|-----------|
|Landing Page|Shows an overview of services, customer cases, customer details, breached SLAs, trends over time and includes customer data, KPIs and portfolio level useful links.|
|Client Details Page|Shows an overview of cases er service, breached SLAs, trends over time,. and includes client \(domain\) specific KPIs, contact details and useful links.|

**Note:** If HR service list doesn't show on the client details page , you might need to add read ACL on sn\_hr\_core\_service table for SP admin.

|Feature|Description|
|-------|-----------|
|Lexicon Taxonomy Name|Admin Workspace for Service Providers \(SPs\)|
|Release Vehicle|Store|
|PRB Management Group|Dev-App-HR|
|Does it support mobile interface|No|
|Plugin or scoped app|Scoped app|
|License requirement|Yes|
|On-Prem support|Yes|
|Link to troubleshooting|NA|
|Link to FAQ|NA|
|Domain seperation|Yes|

**Note:** To see the KPIs, trends across all domains in the workspace dashboard for SP admin need to be in global domain.

<table id="table_yp5_x3r_c1c"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application \(UI\) Issues

</td><td>

If application \(UI\) issues occur, you can start by checking the builder for SP admin workspace and 2 controllers in the MSP Dashboard and the MSP Client Page.

</td></tr><tr><td>

Data Frequency Changes

</td><td>

Some data visualization components such as KPIs, trends, and indicator scorecards are collecting current month data and some aren't, which might cause some data to change.**Note:** It's recommended that you run indicator jobs at the start of the month and collect data for previous months only, not for the current month.

</td></tr></tbody>
</table>|Table|Description|
|-----|-----------|
|Domain \(domain\)|Has all the data about the domain, which is to pull domains and customer data.|
|Company \(core\_company\)|Has all the data about the company and might have multiple companies associated with it. This pulls all points of contact in domain data.|
|HR Service \(sn\_hr\_core\_service\)|Has all the service data and shows services about domains on the client details page.|

**Note:** There is a plugin dependency on Domain Support - Domain Extensions Installer

|Role|Description|
|----|-----------|
|SP Admin \(sn\_sp\_admin\_ws.admin\)|SP Admins are scoped adminitrators for the application and can access workspace, dashboards, KPIs, indicators and portfolio level useful links.|

<table id="table_w12_wpr_c1c"><thead><tr><th>

ACLs

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Experience \(4 ACLs\)

</td><td>

-   2 ACLs for read/write for UX page access
-   2 ACLs for read/write for UX route access.

</td></tr><tr><td>

SP Admin Read \(4 ACLs\)

</td><td>

-   1 ACL for sn\_hr\_core\_service
-   1 ACL for report\_view
-   1 ACL for sn\_hr\_core\_case table
-   1 ACL for sp\_admin role.

</td></tr><tr><td>

Pa Tag Read \(2 ACLs\)

</td><td>

-   1 ACL for pa\_tag and pa\_m2m\_indicator\_tags table
-   1 ACL for pa\_indicators\_breakdowns m2m table.

</td></tr><tr><td>

Execute \(1 ACL\)

</td><td>

1 ACL for data broker sn\_sp\_admin\_ws.MSPUtil

</td></tr></tbody>
</table>**Note:** ACLs are enforced access levels and only SP admins can access the application, workspace, and modules.

|Page|Description|
|----|-----------|
|Service Provider|Primary controller that encapsulates all business logic for MSP dashboard features such as create or update KPI, data and links, which need to be shown on the MSP dashboard.|
|Service Provider Client|Controller that encapsulates all business logic for MSP dashboard client details page features such as create or update KPI, data and links, which need to be shown on the client details page.|

