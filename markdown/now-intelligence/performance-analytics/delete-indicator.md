---
title: Delete an indicator
description: Delete unwanted or unused indicators from your instance. Deleting indicators is risky, so there are several restrictions.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-03-17"
reading_time_minutes: 1
breadcrumb: [Performance Analytics indicators, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Delete an indicator

Delete unwanted or unused indicators from your instance. Deleting indicators is risky, so there are several restrictions.

## Before you begin

Besides roles, check that you meet the following requirements before trying to delete an indicator:

-   Your instance has an active entitlement to the subscription version of Performance Analytics. For more information, see [Activating your Performance Analytics subscription](../concept/c_PremiumPerformanceAnalytics.md#).
-   If your instance is domain-separated, you have visibility into the same domain as the indicator.
-   The indicator that you want to delete is not being used in a formula indicator. If it is so used, see whether you can delete those formula indicators first.
-   The indicator is not a benchmark indicator.

Role required: pa\_data\_collector \(requires that the indicator record is visible to this role; cannot delete external indicators\), pa\_power\_user, pa\_admin, or admin

## About this task

**Warning:** Deleting an indicator deletes all scores for that indicator. Consider the risk of creating a data gap before you delete an indicator.

## Procedure

1.  Use one of the following navigation paths:

    -   If you're on an instance that has not fully migrated to Platform Analytics, navigate to **All** &gt; **** &gt; **Performance Analytics** &gt; **Indicators** &gt; **\[type of indicator\]**, and locate the indicator you want to delete.
    -   If you're on an instance that has fully migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Indicators** &gt; **\[type of indicator\]**, and locate the indicator you want to delete.
2.  Open the indicator record.

3.  Make sure you are in the same application scope as the indicator.

4.  Select **Delete**.

    If you don't see a **Delete** button, check that you meet the requirements for deleting the indicator.

5.  Confirm.


