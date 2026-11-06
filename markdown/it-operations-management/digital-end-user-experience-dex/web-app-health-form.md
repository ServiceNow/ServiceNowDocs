---
title: Web application Performance page
description: The Performance page for a web application displays engagement metrics and performance metrics, such as sessions and page views, response time, page load time, and failed web requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/web-app-health-form.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Applications list, DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Operations Management]
---

# Web application Performance page

The Performance page for a web application displays engagement metrics and performance metrics, such as sessions and page views, response time, page load time, and failed web requests.

<table id="table_r4m_pkr_bgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Started Sessions

</td><td>

Total number of active user sessions for the application over the last 2 hours, specifically the latest 5 minutes.**Note:** Active user sessions information is vital for determining the server load. It also helps you to determine a suitable time for server maintenance.

</td></tr><tr><td>

Average session duration

</td><td>

Average amount of time spent according to user in the application over the last 2 hours, specifically the latest 5 minutes.It’s calculated by dividing total time spent across sessions by the total number of users.

</td></tr><tr><td>

Page views

</td><td>

Frequency with which the users access or view a specific page within the application. Each visit to a page is recorded as one page view, whether it is by a first-time visitor or a returning user.

</td></tr></tbody>
</table>**Note:** Web application performance metrics are available for the previous 2 hours, 24 hours, or 30 days. Select the required time window from the drop-down list to update the visualization.

<table id="table_mrg_fpf_4wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Average response time

</td><td>

Total time taken to respond during the selected time period.

</td></tr><tr><td>

Average page load time

</td><td>

Average amount of time it takes to load the page, from initiation to load completion during the selected time period.

</td></tr><tr><td>

Average DNS lookup

</td><td>

Average amount of time it takes for a Domain Name System \(DNS\) lookup to be completed during the selected time period.A lower average DNS lookup time is desirable because it contributes to faster web page loading and improved overall internet performance.

</td></tr><tr><td>

Failed web requests

</td><td>

Set of all requests that either return an error code or an HTTP 408 status code or fail to return a success code during the selected time period.

</td></tr><tr><td>

Successful web requests

</td><td>

Number of times the HTTP requests made by the client \(such as a web browser\) to a server that result in a positive and expected response.

</td></tr><tr><td>

Availability

</td><td>

Measure of the system's operational performance and its ability to be accessible and usable when needed. It’s typically expressed as a percentage, representing the proportion of time the application is functional and available for use.

</td></tr></tbody>
</table>**Parent Topic:**[Applications list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/application-form.md)

