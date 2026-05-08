---
title: Set up View as Direct Reports
description: Set up View as Direct reports to help managers guide their team members by viewing articles as seen by their direct reports on the Manager Hub.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Manager Hub, HR Service Delivery, Employee Service Management]
---

# Set up View as Direct Reports

Set up View as Direct reports to help managers guide their team members by viewing articles as seen by their direct reports on the Manager Hub.

## Before you begin

Role required: admin

**Note:**

-   Change the **glide.knowman.enable\_view\_as\_user** default value to **True** for the View as feature to work. The default value for this system property is **False**.
-   Update the portal system ID for **ec\_portal\_viewas\_association** system property, in case you have a customized portal. Unless the default portal ID is changed to your customized ID, the feature does not work.
-   The feature works with Tokyo and later family releases.

## About this task

View as Direct report feature is useful for managers who have direct reports. Often, managers do not have access to certain location-specific or designation-specific Knowledge Base articles. Therefore, to help their respective team members, the managers can view the Knowledge Base articles as their respective direct reports.

Use the following procedure to customize the View as experience for your employees with direct reports.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  From the **Your team** drop-down list, select **Team members**.

3.  To change the page view to **Primary** or **Secondary** depending on your preference, right-click on the page and select the **Instance options**.

4.  To get a search engine experience, select **Primary** and select **Save**.

    ![Primary view as provides a search bar along with the name of the direct report on top on the View articles as page.](../images/p-v-view-as.jpg "Primary view option on View articles as page")

5.  To get a compact user experience, select **Secondary** and select **Save**.

    ![Secondary view option has the search bar beside the chosen direct report list view on the View articles as page.](../images/s-v-view-as.jpg "Secondary View option on View articles as page")

6.  Manage the number of Knowledge Base articles visible as a search result or add **Pagination** through the Search results **Instance options**.

    The default result is 15 articles.

    ![The knowledge base search widget shows a number of articles on the View as page.](../images/search-results-view-as.jpg "Search results for View as feature")


## Result

Set up the View as page experience, add pagination, and tweak the number of articles displayed as a search result to provide optimal user experience for a manager searching for Knowledge articles using the feature.

**Parent Topic:**[Configure Manager Hub](../../human-resources/task/set-up-managerhub.md)

**Related topics**  


[RCA approvals for Manager Hub](../../human-resources/task/run-rca-mh.md)

[Activate a scheduled job](../../human-resources/reference/activate-sj-mh.md)

[Configure important dates](../../human-resources/task/configure-imp-dates.md)

[Configure team requests](../../human-resources/task/configure-team-requests.md)

[Configure team data](../../human-resources/task/configure-team-data.md)

[Configure team column data](../../human-resources/task/configure-team-columndata.md)

[Configure team filters](../../human-resources/task/configure-team-filter.md)

[Configure daily stats](../../human-resources/task/configure-daily-stats.md)

[Configure to do mappings](../../human-resources/task/use-to-do-map.md)

[Configure widgets](../../human-resources/task/configure-team-insights.md)

