---
title: Goal Framework for SPM release notes
description: The ServiceNow Goal Framework for Strategic Portfolio Management \(SPM\) application enables you to automate the actual value of your targets for goals that are defined using the ServiceNow Goal Framework application. Goal Framework for SPM was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
---

# Goal Framework for SPM release notes

The ServiceNow® Goal Framework for Strategic Portfolio Management \(SPM\) application enables you to automate the actual value of your targets for goals that are defined using the ServiceNow® Goal Framework application. Goal Framework for SPM was enhanced and updated in the Xanadu release.

## Goal Framework for SPM highlights for the Xanadu release

Use the enhanced target breakdown feature to update actuals and track the progress of your targets in daily, weekly, monthly, quarterly, or yearly intervals.

See [Goal Framework for SPM](https://www.servicenow.com/docs/access?context=goal-framework&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US) for more information.

**Important:** Goal Framework for SPM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Goal Framework for SPM to Xanadu

After upgrading to Goal Framework for SPM v2.3.0, run the **Migrate BreakdownInterval To Checkinfrequency** scheduled job. This scheduled job migrates the existing values in the **Review frequency** and **Breakdown interval** fields to the **Check-in frequency** field in the target records. For more information on how these values are migrated for targets with different values, see [Target breakdowns migration](https://www.servicenow.com/docs/access?context=target-breakdowns-migration&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

## New in the Xanadu release

-   **[Enhanced target breakdowns](https://www.servicenow.com/docs/access?context=target-breakdowns-gf&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    Create Daily, Weekly, or Monthly target breakdowns according to how often you want to update and track the progress of the target. The target breakdowns are created based on the value selected in the **Check-in frequency** field. For example, if you select **Monthly** in the **Check-in frequency** field for a target spanning a year, then 12 monthly target breakdowns are created.


## UI changes

-   **[Changes to Target form](https://www.servicenow.com/docs/access?context=target-form&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    On the Target form, the **Cumulative target** field has been replaced with **Target value distribution field**. The field has two values that describe the target distribution: Spread linearly across the time period \(cumulative\) and Split equally across the time period \(non-cumulative\).


## Changed in this release

-   **[Changes to Target form](https://www.servicenow.com/docs/access?context=target-form&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    On the Target form, the **Breakdown interval** and **Cumulative target** fields have been removed, and the **Review frequency** field has been renamed to **Check-in frequency**.


## Activation information

Install Goal Framework for SPM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Strategic Planning](https://www.servicenow.com/docs/access?context=goal-management-in-alignment-planner-workspace&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    Use the Goal Framework for SPM application in the ServiceNow® Strategic Planning application to visualize the progress of your targets graphically and update the target actuals with ease.

-   **[Goal Framework](https://www.servicenow.com/docs/access?context=goal-framework&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    The ServiceNow® Goal Framework application helps you create goals, set targets for them, and evaluate the progress of the goals and targets to accomplish your organizational plans and drive business outcomes.

    The Goal Framework for SPM application is an extension to the Goal Framework application. When you install Goal Framework for SPM, you get all the features of Goal Framework along with the target automation feature.


**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)

