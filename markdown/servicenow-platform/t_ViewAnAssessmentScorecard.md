---
title: View an assessment scorecard
description: The Assessments application prepares printable scorecards. A scorecard displays easy-to-interpret assessment results, in which the current calculated ratings for an assessable record are compared to previous ratings or to the ratings of other records.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# View an assessment scorecard

The Assessments application prepares printable scorecards. A scorecard displays easy-to-interpret assessment results, in which the current calculated ratings for an assessable record are compared to previous ratings or to the ratings of other records.

## Before you begin

Role required: assessment\_admin or admin

## About this task

Users can examine ratings over time, compare ratings for one assessable record with all assessable records in a table, or compare the ratings of two assessable records. All ratings are averages for the time range selected. The system dynamically updates a scorecard each time you view it, so the ratings reflect recently completed assessments and scripted metrics.

Administrators can display a scorecard for any table by creating a **Related Link** on assessable records. The system provides this link on the Company form by default when Vendor Performance is active.

The Vendor Performance application provides an enhanced scorecard view for vendors.

See Vendor Performance in . [Project Portfolio Suite](https://www.servicenow.com/docs/access?context=c_ProjectPortfolioSuite&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Assessable Records**.

2.  Open a record.

3.  Under **Related Links**, click **View Scorecard**.


-   **[Create a link to a scorecard](t_CreateALinkToAScorecard.md)**  
Users with the admin role can create UI actions that allow users to view scorecards from tables.
-   **[Assessment scorecard averages](../reference/r_Averages.md)**  
The Averages view compares the current ratings for an assessable record in each metric category with the average, minimum, and maximum values from all assessable records in the filter. All ratings are from assessments generated over the trailing twelve months \(TTM\).
-   **[Assessment scorecard categories](../reference/r_Categories.md)**  
The Categories view displays a bar chart showing the average ratings for each category in the selected time interval.
-   **[Assessment scorecard category metrics](../reference/r_CategoryMetrics.md)**  
The Category Metrics view displays the weighted average results for each metric within a category. Use this view to learn how individual metrics affect the overall rating for the category.
-   **[Assessment scorecard head-to-head compare view](../reference/r_HeadToHeadCompare.md)**  
The Head to Head Compare view allows you to compare the ratings of two assessable records of the same type. Select an assessable record from the choice list to compare against the current record's trailing twelve month \(TTM\) ratings.
-   **[Assessment scorecard history](../reference/r_History.md)**  
The History view compares the current ratings for each category with ratings from the previous three years or four quarters.
-   **[Live feed view of assessable records](../reference/r_LiveFeed.md)**  
The Live Feed view displays Live Feed conversations that apply to the assessable record. Users can view the group feed, including tagged comments, and add comments of their own.
-   **[Assessment scorecard ratings](../reference/r_Ratings.md)**  
The scorecard ratings section displays various ratings for the assessable record.

**Parent Topic:**[Assessment administrator tasks](../concept/c_AssessmentProcess.md)

