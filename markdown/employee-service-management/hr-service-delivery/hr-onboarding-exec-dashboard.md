---
title: HR Onboarding Executive dashboard
description: This dashboard gives Human Resources executives insights into how smoothly new employees progress through onboarding activities. Real-time information gives them all the insights they need to measure and improve the influence of their team on providing a delightful employee experience.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-13"
reading_time_minutes: 3
breadcrumb: [HR Performance Analytics Dashboards, Performance Analytics for HR Service Delivery, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# HR Onboarding Executive dashboard

This dashboard gives Human Resources executives insights into how smoothly new employees progress through onboarding activities. Real-time information gives them all the insights they need to measure and improve the influence of their team on providing a delightful employee experience.

**Note:** Starting with the Xanadu release, HR onboarding executive dashboard is being prepared for future deprecation.

![Dashboard showing KPI that are relevant to an HR executive following new hires progress](../../../product/human-resources-global/image/hr-onboarding-exec-dashbrd.png "Overview tab")

![The HR Onboarding Executive dashboard Activities Analysis tab showing average number of onboarding activities](../../../product/human-resources-global/image/hr-onboarding-dashbrd-activity.png "Activity Analysis tab")

![HR Onboarding Executive dashboard showing cases, requests, and survey results](../../../product/human-resources-global/image/hr-onboarding-dashbrd-new-hire.png "New Hire Experience tab")

## End users and roles

|End user and goal|Required Performance Analytics role|
|-----------------|-----------------------------------|
|HR Executive: Needs clear visibility into employee experience|sn\_hr\_core.manager|

## HR Onboarding Executive indicators

-   **Number of employees leaving the company**

    Measures employee attrition. The **Employee Turnover** widget displays this value, broken down by department, employment type, or employment duration.

-   **Average number of onboarding activities per onboarding case**

    Measures how many activities are closed on average from the total number of closed onboarding cases, using the formula `[Number of Closed Onboarding Activities] / [Number of closed lifecycle events cases > HR Service = Request Onboarding]`

-   **Average new hire satisfaction survey score**

    Measures the average score of the new hire satisfaction survey which is sent to the employees after they have onboarded

-   **Average time taken for onboarding activities**

    Measures the time taken on an average to finish onboarding activities per onboarding case, using the formula `[Summed duration of onboarding activities] / [Number of closed lifecycle events cases > HR Service = Request Onboarding] / 24`

-   **Number of HR Cases logged in first 30 days of employment**

    Measures the number of non-onboarding HR cases that were logged by employees during the first 30 days of their employment

-   **Average number of onboarding activities per onboarding case - Fulfiller**

    Measures how many activities assigned to the fulfiller are closed on average from the total number of closed onboarding cases, using the formula `[Number of closed onboarding activities - Fulfiller] / [Number of closed lifecycle events cases > HR Service = Request Onboarding]`

-   **Average number of onboarding activities per onboarding case - Employee**

    Measures how many activities assigned to the employee are closed on average from the total number of closed onboarding cases, using the formula `[Number of closed onboarding activities - Employee] / [Number of closed lifecycle events cases > HR Service = Request Onboarding]`

-   **Average time taken for onboarding activities - Employee**

    Measures the time employees take on average to finish their onboarding activities as part of onboarding case, using the formula `[Summed duration of onboarding activities - Employee] / [Number of closed lifecycle events cases > HR Service = Request Onboarding] / 24`

-   **Average time taken for onboarding activities - Fulfillers**

    Measures the time fulfillers take on average to finish their onboarding activities as part of onboarding case, using the formula `[Summed duration of onboarding activities - Fulfiller] / [Number of closed lifecycle events cases > HR Service = Request Onboarding] / 24`

-   **Number of closed lifecycle events cases**

    Measures number of lifecycle events cases closed today

-   **Number of closed onboarding activities**

    Measures the number of all activities closed as part of a lifecyle case, using the formula `[Number of closed onboarding activities - Employee] + [Number of closed onboarding activities - Fulfiller]`

-   **Number of closed onboarding activities - Employee**

    Measures the number of closed activities assigned to the new hire

-   **Number of closed onboarding activities - Fulfiller**

    Measures the number of closed activities assigned to the fulfiller

-   **Number of IT Requests logged in first 30 days of employment**

    Measures the number of IT Requests that were logged by employees during the first 30 days of their employment

-   **Number of new lifecycle events cases**

    Measures number of lifecycle events cases opened today

-   **Number of open lifecycle events cases - Employees starting in next 7 days**

    Measures number of open cases for employees starting in the next 7 days

-   **Number of open lifecycle events cases - Post day 1**

    Measures number of open cases for employees who have already started

-   **Number of open lifecycle events cases - Pre day 1**

    Measures number of open cases for employees who have yet to start


## Breakdowns

-   Activity
-   Activity Set
-   Department
-   Employment duration
-   Employment Type
-   Location
-   Owner Group
-   Region

## Data visualizations

The dashboards include the following visualizations:

|Title|Type|
|-----|----|
|Overdue Activities - Employee|Single Score|
|Overdue Activities - Fulfiller|Single Score|

**Parent Topic:**[HR Performance Analytics Dashboards](human-resources-content-pack.md)

