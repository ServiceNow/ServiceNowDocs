---
title: Predict CI consumption for 2026 Packaging SKU
description: Forecast your licensing needs by comparing your current ITOM subscription unit usage against the predicted usage under 2026 Packaging SKUs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/generate-ci-consumption-predictions.html
release: australia
topic_type: task
last_updated: "2026-05-10"
reading_time_minutes: 1
keywords: [CI consumption, prediction, 2026 Packaging, 2026 Packaging SKU migration]
breadcrumb: [Use, ITOM/OT SU Licensing and subscriptions, IT Operations Management]
---

# Predict CI consumption for 2026 Packaging SKU

Forecast your licensing needs by comparing your current ITOM subscription unit usage against the predicted usage under 2026 Packaging SKUs.

## Before you begin

Check your entitlements to determine whether you have ITOM subscriptions.

Ensure that you installed the latest available version of the ITOM/OT SU Licensing from ServiceNow Store.

Role required: admin

## About this task

Before migrating to the 2026 Packaging SKUs, you can estimate post-migration consumption without requiring an active ITOM license. Predict SU consumption per category by applying SU ratios to the latest CI data in your environment. SU ratios represent the number of CIs in each category that correspond to one Subscription Unit, as set by your contract. Use this prediction to confirm your expectation of license consumption. If the measurement is higher than planned, either alter your usage of ITOM or increase your subscription.

## Procedure

1.  Navigate to **All** &gt; **ITOM License** &gt; **Report ITOM Licensable CIs**.

2.  Select the check box for the application for which you want to view licensed CIs and select **Show Licensable CIs**.

    After the **Usage count estimator** job completes, results are added to the ITOM Licensable CIs \[itom\_lu\_licensable\_cis\] table and are visible in the **Report ITOM Licensable CIs** view.

    \[Omitted image "ci-consumption-predictions.png"\] Alt text: License prediction report for SU consumption per each CI category.

    **Note:** **CI New Category** equals **true** if this category is not covered by your current license. It will be introduced as a new licensable category under the 2026 Packaging SKU.

3.  See only the prediction records and not production licensing records by setting the filter conditions to **Contains Estimate**.

4.  View the latest daily SU consumption prediction results per CI category created by usage count estimator jobs that run automatically on a daily basis.

    1.  Navigate to the ITOM Licensable CIs \[itom\_lu\_licensable\_cis\] table by typing the table name in the navigation filter.

    2.  See the latest daily prediction results per each CI category by setting the filter conditions to **Created-on-today**.


## What to do next

Compare the predicted SU consumption data to the estimate you had before this forecast.

