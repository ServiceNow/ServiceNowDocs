---
title: Fetch and view EcoVadis scores
description: Retrieve current scores and scorecards from EcoVadis on demand or at a set frequency of time using Third-party Risk Management. Customizing settings for the EcoVadis Fetch Score Scheduler can help you get the latest scores when you need them.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [TPRM with EcoVadis, Integrate, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Fetch and view EcoVadis scores

Retrieve current scores and scorecards from EcoVadis on demand or at a set frequency of time using Third-party Risk Management. Customizing settings for the EcoVadis Fetch Score Scheduler can help you get the latest scores when you need them.

## Before you begin

Role required: admin

## About this task

EcoVadis ratings can help you can gain detailed insights into the environmental, ethical, and social practices of your third parties. Fetching these scores regularly helps you stay updated on their compliance and performance.

**Note:** Confirm that all third parties that you would like to assess are using EcoVadis has a website listed as part of their third-party record. EcoVadis confirms that a third party is registered by referencing the website URL.

## Procedure

1.  **All** &gt; **Ecovadis for third-party Risk Management** &gt; **Scheduled Job**

2.  Select **EcoVadis fetch Score Scheduler**.

3.  Fetch a score on demand or at a scheduled time.

    -   Select **Execute Now** to get the latest scores.
    -   Select the Active option, set the following fields, and select **Update** to fetch scores at a specific frequency.

<table id="table_i1x_crs_fcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run

</td><td>

The frequency or set dates EcoVadis scores are fetched.-   Daily
-   Weekly
-   Monthly
-   Periodically
-   Once
-   On Demand
-   Business Calendar: Entry Start/Finish


</td></tr><tr><td>

Time zone

</td><td>

Time zone that applies to the time selected to fetch the scores.

</td></tr><tr><td>

Time

</td><td>

Time the scores are fetched.

</td></tr></tbody>
</table>    **Note:** A scheduled job will run once per day.

4.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Third Parties** &gt; **All Third Parties** and select the third party you want.

5.  Select the Risk intelligence scores related list.

6.  View a score by selecting the date and time from the **Score generated on** column.

    **Note:** You can view all scores including EcoVadis theme scores and scorecards when your score record is in the EcoVadis view.


## Result

You can view EcoVadis third-party theme scores in the EcoVadis Theme Scores related list and access the EcoVadis scorecard by selecting the URL in the **Scorecard** field.

Scores are mapped to the Risk Intelligence Provider and Provider Service for EcoVadis.

**Note:** You can verify that scores are being fetched by navigating to **All** &gt; **EcoVadis for third-party Risk Management** &gt; **Application Logs**.

**Parent Topic:**[Integrating EcoVadis with Third-party Risk Management](../concept/tprm-integrating-ecovadis.md)

