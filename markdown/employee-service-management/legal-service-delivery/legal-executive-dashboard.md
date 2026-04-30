---
title: Legal Executive dashboard
description: With the Legal Executive dashboard, you can get an insight into how your team and business are performing for resolving Legal service requests.
locale: en-US
release: yokohama
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 17
breadcrumb: [Analytics and Reporting Solutions for Legal Service Delivery, Legal Service Delivery, Employee Service Management]
---

# Legal Executive dashboard

With the Legal Executive dashboard, you can get an insight into how your team and business are performing for resolving Legal service requests.

From a single place, you can track the status of legal requests and matters, analyze trends, and drill down into the details. You can view the details for top request categories, requests by user locations, practice area, and requesting department, SLA compliance of legal requests and legal matters, the average number of requests handled per attorney, and average time to close legal requests and legal matters over time.

**Note:** The classic version of Legal Executive Dashboard has been deprecated. If you open a saved URL to access the classic Legal Executive Dashboard, the Next Experience dashboard is automatically displayed. If you have customized the classic version, review and migrate your customizations to the Next Experience Legal Executive Dashboard.

For reports and metrics on legal requests and legal matters and the trend analysis, see [Legal Operations dashboard](legal-operations-dashboard.md).

![Legal Executive dashboard showing widgets and reports.](../image/legal-executive-dashboard.gif "Legal Executive dashboard")

**Important:** The tabs specific to practice areas are available on the Legal Executive dashboard depending on whether the corresponding application is installed. For example, the **Contracts** tab is available when you have installed the Legal Simple Contracts application. Also, you can add new tabs in the dashboard to view reports related to practice areas created by you.

## Required ServiceNow AI Platform roles

-   sn\_lg\_ops.legal\_report\_viewer, required to see the dashboard widgets and data.
-   sn\_lg\_ops.legal\_report\_publisher, required to edit the dashboard.

## Access the Legal Executive dashboard

To open the dashboard, navigate to **All** &gt; **Legal Request** &gt; **Legal Dashboards** and click **Legal Executive**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_axn_c3q_dsb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

General counsel

</td><td>

Make data-driven decisions through insights into legal operations with the following metrics:-   Total number of legal requests and legal matters for the current year with breakdown by geography, practice area, and requesting department
-   Backlog of open legal requests and legal matters with aging
-   Average time to resolve different types of legal requests and legal matters
-   Practice area-specific metrics:
    -   Contracts: Open backlog by deal size and aging; average time to close contract requests
    -   Privacy and Compliance: SLA Compliance; average time to close different request types such as Conflict of Interest and Privacy Assessment
    -   Digital Forensics: Breakdown of requested activities; backlog of requested activities with aging; average time to close by activities

</td></tr><tr><td>

Practice area lead

</td><td>

Make data-driven decisions through insights into legal operations with the following metrics:-   Average number of legal requests and legal matters handled per attorney
-   SLA compliance of legal requests and legal matters
-   Top practice area getting the highest number of requests
-   Average time to resolve different types of legal requests and legal matters

</td></tr></tbody>
</table>## Indicator groups

<table id="table_stm_ccz_gsb"><thead><tr><th>

Indicator group name

</th><th>

Description

</th><th>

Indicators

</th></tr></thead><tbody><tr><td>

Average requests per attorney

</td><td>

Average number of legal requests handled by each attorney where breakdowns are Practice area and Category.

</td><td>

-   Conflict of Interest
-   Content Review
-   Digital Forensics
-   General Legal Request
-   NDA Request
-   Privacy Assessment
-   Sales Contract Review
-   Stock Pre-Clearance
-   Third Party Contract Review

</td></tr><tr><td>

Average matters per attorney

</td><td>

Average number of legal matters handled by each attorney in a practice area.

</td><td>

-   Digital Forensics
-   General Legal Request
-   Privacy Assessment
-   Subpoena

</td></tr><tr><td>

Digital Forensics Open Backlog

</td><td>

Number of days that the activities have been open for digital forensics requests created this year to date. An activity's age is calculated from the time the legal matter task associated with the activity was created to the present day.

</td><td>

-   Collect
-   Preserve
-   Review
-   Present

</td></tr><tr><td>

Legal Contracts: Avg. Age

</td><td>

Average age of Contract requests of different deal sizes.

</td><td>

-   &lt;$500 K
-   $500 K - $1M
-   $1M - $5M
-   $5M

</td></tr><tr><td>

Open Backlog: Legal Requests

</td><td>

Number of open legal requests, as well as their age, which indicates how long they've been open.

</td><td>

-   Age 30–60 days
-   Age &lt;30 days
-   Age &gt;60 days

</td></tr><tr><td>

Open Backlog: Legal Matters

</td><td>

Number of open legal matters, as well as their age, which indicates how long they've been open.

</td><td>

-   Age 30–60 days
-   Age &lt;30 days
-   Age &gt;60 days

</td></tr><tr><td>

Privacy and Compliance Open Backlog

</td><td>

Age of open privacy and compliance requests that have been submitted. The age is calculated from the time the legal requests were created to the present day.

</td><td>

-   Conflict of Interest
-   Privacy Impact Assessment
-   Stock Preclearance

</td></tr></tbody>
</table>## Indicators

-   **$1M - $5M**

    Average age of Contract requests with a deal size of $1 million to $5 million.

-   **$500 K - $1M**

    Average age of Contract requests with a deal size of $500 K to $1 million.

-   **$5M**

    Average age of Contract requests with a deal size of $5 million or more.

-   **&lt;$500 K**

    Average age of Contract requests with a deal size of $500 K or less.

-   **Age 30–60 days \(applies to legal requests\)**

    Number of open legal requests created in the last 30–60 days.

-   **Age 30–60 days \(applies to legal matters\)**

    Number of open legal matters created in the last 30–60 days.

-   **Age &lt;30 days \(applies to legal requests\)**

    Number of open legal requests created in the last 30 days.

-   **Age &lt;30 days \(applies to legal matters\)**

    Number of open legal matters created in the last 30 days.

-   **Age &gt;60 days \(applies to legal requests\)**

    Number of open legal requests created more than 60 days ago.

-   **Age &gt;60 days \(applies to legal matters\)**

    Number of open legal matters created more than 60 days ago.

-   **Average activity completion time for digital forensics**

    Monthly trend of average completion time of various digital forensics activities by phase. The completion time is calculated from the time an activity task is created and until it is closed.

-   **Average matter completion time per practice area**

    Monthly trend of average completion time of legal matters by practice area. The completion time is calculated from the time a legal matter is created and until it is closed.

-   **Average matters per Attorney**

    Average number of legal matters handled by each attorney where breakdowns are Practice area and Category.

-   **Average request completion time for contracts**

    Monthly trend of the average completion time of contract requests by different contract types.

-   **Average request completion time for privacy and compliance**

    Monthly trend of the average completion time of various privacy and compliance requests.

-   **Average request completion time per practice area**

    Monthly trend of average completion time of legal requests by practice area.

-   **Average requests per Attorney**

    Average number of legal requests handled by each attorney where breakdowns are Practice area and Category.

-   **Collect**

    Number of days that the Collect activity has been open for digital forensics requests created this year to date. The activity's age is calculated from the time the legal matter task associated with the activity was created to the present day.

-   **Conflict of Interest**

    Age of open Conflict of Interest requests that have been submitted. The age is calculated from the time the legal requests were created to the present day.

-   **Count of members in Legal group**

    Number of users in a legal user group.

-   **MoM trend of Legal Matters**

    Monthly trend of number of legal matters created.

-   **MoM trend of Legal Requests**

    Monthly trend of number of legal requests created.

-   **Open Backlog Contract Requests**

    Number of open Contract requests, broken down by deal size, that have been created so far this year, as well as their age.

-   **Present**

    Number of days that the Present activity has been open for digital forensics requests created this year to date. The activity's age is calculated from the time the legal matter task associated with the activity was created to the present day.

-   **Preserve**

    Number of days that the Preserve activity has been open for digital forensics requests created this year to date. The activity's age is calculated from the time the legal matter task associated with the activity was created to the present day.

-   **Privacy Impact Assessment**

    Age of open Privacy Assessment requests that have been submitted. The age is calculated from the time the legal requests were created to the present day.

-   **Request Completed within SLA**

    Number of Privacy and Compliance requests closed on the day within SLA.

-   **Review**

    Number of days that the Review activity has been open for digital forensics requests created this year to date. The activity's age is calculated from the time the legal matter task associated with the activity was created to the present day.

-   **Stock Preclearance**

    Age of open Stock Preclearance requests that have been submitted. The age is calculated from the time the legal requests were created to the present day.

-   **Total Completed Legal Requests with SLA**

    Number of legal requests closed on the day within SLA.

-   **YTD Digital Forensics Request**

    Number of Digital Forensics requests that have been created so far this year.

-   **YTD Legal contracts**

    Number of Contract requests that have been created so far this year.

-   **YTD Legal matters**

    Number of legal matters that have been created so far this year.

-   **YTD Legal Privacy and Compliance Requests**

    Number of Privacy and Compliance requests that have been created so far this year.

-   **YTD Legal requests**

    Number of legal requests that have been created so far this year.

-   **% of privacy and compliance requests that met SLA**

    Percentage of privacy and compliance requests that were responded to within the defined SLA this year to date. The score is calculated according to this formula: \[Requests Completed within SLA\]/\[Total Completed Legal Requests with SLA\] \* 100

-   **Conflict of Interest**

    Average number of legal matters in the Conflict of Interest category handled by each attorney in the respective assignment group this year to date. The score is calculated according to this formula: \[Average requests per Attorney &gt; Category = Conflict of Interest\]/\[Count of members in Legal group &gt; Legal group = Legal - Ethics &amp; Compliance\]

-   **Content Review**

    Average number of legal requests in the Content Review category handled by each attorney in the respective assignment group this year to date. The score is calculated according to this formula: \[Average requests per Attorney &gt; Category = Content Review\]/\[Count of members in Legal group &gt; Legal group = Legal Department\]

-   **Digital Forensics \(applies to legal requests\)**

    Average number of legal requests in the Digital Forensics category handled by each attorney in the respective assignment group this year to date. The score is calculated according to this formula: \[Average requests per Attorney &gt; Category = Digital Forensics\]/\[Count of members in Legal group &gt; Legal group = Legal - Digital Forensics\]

-   **Digital Forensics \(applies to legal matters\)**

    Average number of legal matters in the Digital Forensics category handled by each attorney in the respective assignment group this year to date. The score is calculated according to this formula: \[Average matters per Attorney &gt; Category = Digital Forensics\]/\[Count of members in Legal group &gt; Legal group = Legal - Digital Forensics\]

-   **General Legal Request \(applies to legal requests\)**

    Average number of legal requests in the General Legal Request category handled by each attorney in the respective assignment group this year to date. The score is calculated according to this formula: \[Average requests per Attorney &gt; Category = General Legal Request\]/\[Count of members in Legal group &gt; Legal group = Legal Department\]

-   **General Legal Request \(applies to legal matters\)**

    Average number of legal matters in the General Legal Request category handled by each attorney in the respective assignment group this year to date. The score is calculated according to this formula: \[Average matters per Attorney &gt; Category = General Legal Request\]/\[Count of members in Legal group &gt; Legal group = Legal Department\]

-   **NDA Request**

    Average number of legal requests in the Non-disclosure Agreement category handled by each attorney in the respective assignment group this year to date. The score is calculated according to this formula: \[Average requests per Attorney &gt; Category = NDA Request\]/\[Count of members in Legal group &gt; Legal group = Legal Contracts Support\]

-   **Privacy Assessment**

    Average number of legal requests in the Privacy Assessment category handled by each attorney in the respective assignment group this year to date. The score is calculated according to this formula: \[Average requests per Attorney &gt; Category = Privacy Assessment\]/\[Count of members in Legal group &gt; Legal group = Legal Privacy\]

-   **Privacy Assessment**

    Average number of legal matters in the Privacy Assessment category handled by each attorney in the respective assignment group this year to date. The score is calculated according to this formula: \[Average matters per Attorney &gt; Category = Privacy Assessment\]/\[Count of members in Legal group &gt; Legal group = Legal Privacy\]

-   **Sales Contract Review**

    Average number of legal requests in the Sales Contract Review category handled by each attorney in the respective assignment group this year to date. The score is calculated according to this formula: \[Average requests per Attorney &gt; Category = Sales Contract Review\]/\[Count of members in Legal group &gt; Legal group = Legal Sales Contract\]

-   **Stock Pre-clearance**

    Average number of legal requests in the Stock Preclearance category handled by each attorney in the respective assignment group this year to date. The score is calculated according to this formula: \[Average requests per Attorney &gt; Category = Stock Pre-Clearance\]/\[Count of members in Legal group &gt; Legal group = Legal Stock Approvers\]

-   **Subpoena**

    Average number of legal matters in the Subpoena category handled by each attorney in the respective assignment group this year to date. The score is calculated according to this formula: \[Average matters per Attorney &gt; Category = Subpoena\]/\[Count of members in Legal group &gt; Legal group = Legal Employment\]

-   **Third Party Contract Review**

    Average number of legal requests in the Third Party Contract Review category handled by each attorney in the respective assignment group this year to date. The score is calculated according to this formula: \[Average requests per Attorney &gt; Category = Third Party Contract\]/\[Count of members in Legal group &gt; Legal group = Legal Contracts Support\]


## Breakdowns

-   **Common to Legal Service Delivery applications**
    -   Group
    -   Assigned To \(for all users in the system\)
    -   Assigned To \(for users in the Legal Privacy and Compliance groups\)
    -   Category
-   **Legal Request Management**
    -   Age
    -   Assigned To
    -   Category
    -   Practice area
    -   Priority
    -   State
    -   Subcategory
-   **Legal Matter Management**
    -   Matter Owner
    -   Priority
    -   State \(for legal matters\)
    -   State \(for legal matter tasks\)
-   **Legal Simple Contracts**
    -   Assigned To
    -   Category
    -   Deal Size
    -   Subcategory
-   **Legal Digital Forensics**
    -   Assigned To
    -   Requested Activities
    -   Subcategory

## Indicator visualizations

<table id="table_o13_byx_3sb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source indicator/indicator group

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="4">

Requests tab

</td></tr><tr><td>

Total requests \(YTD\)

</td><td>

Score![Score icon.](../../reporting/image/icon-single-score-report-p.png)

</td><td>

YTD Legal requests

</td><td>

Compares the number of requests received this year to date to the same period of the previous year.

</td></tr><tr><td>

Top 3 requests for this month

</td><td>

Scorecard![Scorecard icon.](../../reporting/image/icon-list-report-p.png)

</td><td>

MoM trend of Legal Requests

</td><td>

Provides insight into the top active areas where the internal business is seeking legal assistance.

</td></tr><tr><td>

Open requests by age

</td><td>

List![List icon.](../../reporting/image/icon-list-report-p.png)

</td><td>

Open Backlog: Legal Requests

</td><td>

Provides the number of open requests along with their age, which indicates how long the requests have been open.

</td></tr><tr><td>

Request stats \(YTD\)

</td><td>

Donut![Donut icon.](../../reporting/image/icon-donut-report-p.png)

</td><td>

Legal Request \[sn\_lg\_ops\_request\]

</td><td>

Number of legal requests received this year to date grouped by practice area or the requesting department.

</td></tr><tr><td>

Avg. requests per attorney by category

</td><td>

List![List icon.](../../reporting/image/icon-list-report-p.png)

</td><td>

Average requests per attorney

</td><td>

Displays the average number of legal requests handled by each attorney in a practice area.

</td></tr><tr><td>

Requests completion time

</td><td>

Line![Line icon.](../../reporting/image/icon-line-report-p.png)

</td><td>

Average request completion time per practice area

</td><td>

Displays the monthly trend of average completion time of legal requests by practice area. The completion time is calculated from the time a legal request is created and until it is closed.

</td></tr><tr><td class="sub-head" colspan="4">

Matters tab

</td></tr><tr><td>

Total matters \(YTD\)

</td><td>

Score![Score icon.](../../reporting/image/icon-single-score-report-p.png)

</td><td>

YTD Legal matters​

</td><td>

Compares the number of legal matters received this year to date to the same period of the previous year.

</td></tr><tr><td>

Top 3 matters for this month

</td><td>

Scorecard![Scorecard icon.](../../reporting/image/icon-list-report-p.png)

</td><td>

MoM trend of Legal Matters

</td><td>

Provides insights into the legal team's most active areas of work.

</td></tr><tr><td>

Open matters by age

</td><td>

List![List icon.](../../reporting/image/icon-list-report-p.png)

</td><td>

Open Backlog: Legal Matters

</td><td>

Provides the number of open matters along with their age, which indicates how long matters have been open.

</td></tr><tr><td>

Matter stats \(YTD\)

</td><td>

Donut![Donut icon.](../../reporting/image/icon-donut-report-p.png)

</td><td>

Legal Matter \[sn\_lg\_matter\_matter\]

</td><td>

Number of legal matters received this year to date grouped by practice area or the requesting department.

</td></tr><tr><td>

Avg. matters per attorney by category

</td><td>

List![List icon.](../../reporting/image/icon-list-report-p.png)

</td><td>

Average matters per attorney

</td><td>

Average number of legal matters handled by each attorney in a practice area.

</td></tr><tr><td>

Matters completion time

</td><td>

Line![Line icon.](../../reporting/image/icon-line-report-p.png)

</td><td>

Average matter completion time per practice area

</td><td>

Displays the monthly trend of average completion time of legal matters by practice area. The completion time is calculated from the time a legal matter is created and until it is closed.

</td></tr><tr><td class="sub-head" colspan="4">

Contracts tab

</td></tr><tr><td>

Total Contract requests \(YTD\)

</td><td>

Score![Score icon.](../../reporting/image/icon-single-score-report-p.png)

</td><td>

YTD Legal contracts

</td><td>

Compares the number of Contract requests received this year to date to the same period of the previous year.

</td></tr><tr><td>

Open Contract requests by deal size

</td><td>

Donut![Donut icon.](../../reporting/image/icon-donut-report-p.png)

</td><td>

Open Backlog Contract Requests

</td><td>

Displays how long the Contract requests have been open by deal size.

</td></tr><tr><td>

Open Contract requests by deal size and age

</td><td>

List![List icon.](../../reporting/image/icon-list-report-p.png)

</td><td>

Legal Contracts: Avg. Age

</td><td>

Displays the average age of Contract requests of different deal sizes.

</td></tr><tr><td>

Contract requests by contract type \(YTD\)

</td><td>

Donut![Donut icon.](../../reporting/image/icon-donut-report-p.png)

</td><td>

Legal Request \[sn\_lg\_ops\_request\]

</td><td>

Number of Contract requests created so far this year.

</td></tr><tr><td>

Contract completion time

</td><td>

Line![Line icon.](../../reporting/image/icon-line-report-p.png)

</td><td>

Average request completion time for contracts

</td><td>

Displays the monthly trend of average completion time of contract requests by different contract types. The completion time is calculated from the time a Contract request is created and until it is closed.

</td></tr><tr><td class="sub-head" colspan="4">

Privacy and Compliance tab

</td></tr><tr><td>

Total Privacy and Compliance requests \(YTD\)

</td><td>

Score![Score icon.](../../reporting/image/icon-single-score-report-p.png)

</td><td>

YTD Legal Privacy and Compliance Requests

</td><td>

Compares the number of privacy and compliance requests received this year to date to the same period of the previous year.

</td></tr><tr><td>

Open requests by category and age​

</td><td>

List![List icon.](../../reporting/image/icon-list-report-p.png)

</td><td>

Privacy and Compliance Open Backlog

</td><td>

Displays how long the privacy and compliance requests have been open by different request types.

</td></tr><tr><td>

Privacy and Compliance requests by category \(YTD\)

</td><td>

Donut![Donut icon.](../../reporting/image/icon-donut-report-p.png)

</td><td>

Legal Request \[sn\_lg\_ops\_request\]

</td><td>

Number of open legal requests in Privacy or Compliance practice areas.

</td></tr><tr><td>

% Requests responded within SLA \(YTD\)​

</td><td>

Score![Score icon.](../../reporting/image/icon-single-score-report-p.png)

</td><td>

% of privacy and compliance requests that met SLA

</td><td>

Displays the percentage of privacy and compliance requests that were completed within the defined SLA.

</td></tr><tr><td>

Request completion time​

</td><td>

Line![Line icon.](../../reporting/image/icon-line-report-p.png)

</td><td>

Average request completion time for privacy and compliance

</td><td>

Displays the monthly trend of average completion time of various privacy and compliance requests. The completion time is calculated from the time a request is assigned to an attorney until it is closed.

</td></tr><tr><td class="sub-head" colspan="4">

Digital Forensics tab

</td></tr><tr><td>

Total Digital Forensics requests \(YTD\)

</td><td>

Score![Score icon.](../../reporting/image/icon-single-score-report-p.png)

</td><td>

YTD Digital Forensics Request

</td><td>

Compares the number of digital forensics requests received this year to date to the same period of the previous year.

</td></tr><tr><td>

Open activities by age

</td><td>

List![List icon.](../../reporting/image/icon-list-report-p.png)

</td><td>

Digital Forensics Open Backlog

</td><td>

Displays how long the digital forensics requests’ activities have been open. An activity's age is calculated from the time the legal matter task associated with the activity was created to the present day.

</td></tr><tr><td>

Activities completion time

</td><td>

Line![Line icon.](../../reporting/image/icon-line-report-p.png)

</td><td>

Average activity completion time for digital forensics​

</td><td>

Displays the monthly trend of average completion time of various digital forensics activities. The completion time is calculated from the time an activity task is created and until it is closed.

</td></tr></tbody>
</table>## Data visualizations

<table id="table_fxn_c3q_dsb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Requests by geography \(YTD\)

</td><td>

Map![Map icon.](../../reporting/image/icon-map-report-p.png)

</td><td>

Legal Request \[sn\_lg\_ops\_request\]

</td><td>

Number of legal requests received from users in various regions so far this year is displayed on a map.

</td></tr><tr><td>

Requested activities \(YTD\)

</td><td>

Donut![Donut icon.](../../reporting/image/icon-donut-report-p.png)

</td><td>

Legal Matter Task \[sn\_lg\_matter\_task\]

</td><td>

Number of activities requested for the Digital Forensics requests so far this year.

</td></tr><tr><td>

Open requests by category

</td><td>

Donut![Donut icon.](../../reporting/image/icon-donut-report-p.png)

</td><td>

Legal Request \[sn\_lg\_ops\_request\]

</td><td>

Number of open legal requests in Stock Preclearance, Conflict of Interest, or Privacy Assessment categories.

</td></tr><tr><td>

Open activities

</td><td>

Donut![Donut icon.](../../reporting/image/icon-donut-report-p.png)

</td><td>

Legal Matter Task \[sn\_lg\_matter\_task\]

</td><td>

Number of open activities for all Digital Forensics requests as of date.

</td></tr><tr><td>

Matters by geography \(YTD\)

</td><td>

Map![Map icon.](../../reporting/image/icon-map-report-p.png)

</td><td>

Legal Matter \[sn\_lg\_matter\_matter\]

</td><td>

Number of legal matters created from legal fulfillers in various regions so far this year is displayed on a map.

</td></tr></tbody>
</table>**Parent Topic:**[Analytics and Reporting Solutions for Legal Service Delivery](../../application-content-packs/concept/legalsd-content-pack.md)

