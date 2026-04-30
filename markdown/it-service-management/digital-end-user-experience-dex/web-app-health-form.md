---
title: Web application — Performance page
description: Monitor the application performance to enable proactive detection and resolution of issues, maintain optimal performance, improve user experience, troubleshoot the performance issues, and confirm that the application meets its intended purpose.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Applications list, DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Web application — Performance page

Monitor the application performance to enable proactive detection and resolution of issues, maintain optimal performance, improve user experience, troubleshoot the performance issues, and confirm that the application meets its intended purpose.

<table id="table_r4m_pkr_bgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Started Sessions

</td><td>

Total number of active user sessions for the application over the last 2 hours, specifically the latest 5 minutes.**Note:** Active user sessions information is vital for determining the server load. It also helps you to determine the perfect time for server maintenance.

</td></tr><tr><td>

Average session duration

</td><td>

Average amount of time spent according to user in the application over the last 2 hours, specifically the latest 5 minutes.It’s calculated by dividing total time spent across sessions by the total number of users.

</td></tr><tr><td>

Page views

</td><td>

Frequency with which the users access or view a specific page within the application. Each visit to a page is recorded as one page view, whether it is by a first-time visitor or a returning user.

</td></tr></tbody>
</table><table id="table_mrg_fpf_4wb"><thead><tr><th>

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

Average amount of time it takes for a Domain Name System \(DNS\) lookup to be completed during the selected time period.A lower average DNS lookup time is desirable, as it contributes to faster web page loading and improved overall internet performance.

</td></tr><tr><td>

Failed web requests

</td><td>

Set of all requests that either return an Error Code or an HTTP 408 status code or fail to return a Success Code during the selected time period.

</td></tr><tr><td>

Successful web requests

</td><td>

Number of times the HTTP requests made by the client \(such as a web browser\) to a server that result in a positive and expected response.

</td></tr><tr><td>

Availability

</td><td>

Measure of the system's operational performance and its ability to be accessible and usable when needed. It’s typically expressed as a percentage, representing the proportion of time the application is functional and available for use.

</td></tr></tbody>
</table>**Note:** If you set up a page-level monitoring for specific application pages, you can see the collected metrics in the Metrics analyzer. Select one or more pages under **Pages** and narrow down your data by location, OS, or date range.

**Parent Topic:**[Applications list](application-form.md)

