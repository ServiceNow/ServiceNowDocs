---
title: Generate CI consumption predictions for 2026 Container Packaging SKU migration
description: Forecast your licensing needs by comparing your current ITOM subscription unit usage against the predicted usage under 2026 Container Packaging SKUs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/generate-ci-consumption-predictions.html
release: zurich
topic_type: task
last_updated: "2026-05-10"
reading_time_minutes: 1
keywords: [CI consumption, prediction, 2026 Container Packaging, 2026 Container Packaging SKU migration]
breadcrumb: [Using ITOM/OT SU Licensing, ITOM/OT SU Licensing and subscriptions, IT Operations Management]
---

# Generate CI consumption predictions for 2026 Container Packaging SKU migration

Forecast your licensing needs by comparing your current ITOM subscription unit usage against the predicted usage under 2026 Container Packaging SKUs.

## Before you begin

Check your entitlements to determine whether you have ITOM subscriptions.

Ensure that you installed the latest available version of the ITOM/OT SU Licensing from ServiceNow Store.

Role required: admin

## About this task

Forecast your licensing needs before migrating to the 2026 Container Packaging SKUs by estimating post-migration consumption without requiring an active ITOM license. Predict SU consumption per category by applying SU ratios to the latest CI data in your environment. SU ratios represent the number of CIs in each category that correspond to one Subscription Unit, as set by your contract. Then you can upgrade your subscription or adjust your consumption according to the prescription. You can use it to confirm your expectation of license consumption, and if the measurement is higher than planned, either alter your usage of ITOM or increase your subscription.

## Procedure

1.  Navigate to **All** &gt; **ITOM License** &gt; **Report ITOM Licensable CIs**.

2.  Select the check box for the application for which you want to view licensed CIs and select **Show LIcensable CIs**.

    After the **Usage count estimator** job completes, results are added to the ITOM Licensable CIs \[itom\_lu\_licensable\_cis\] table and are visible in the **Report ITOM Licensable CIs** view.

    \[Omitted image "ci\_consumption\_prediction\_list\_daily.png"\] Alt text: License prediction report for daily SU consumption per each CI category.

    **Note:** **CI New Category** equals **true** if this category is not covered by your current license. It will be introduced as a new licensable category under the 2026 Container.

3.  See only the prediction records and not production licensing records by setting the filter conditions to **Contains Estimate**.

4.  View the latest daily SU consumption prediction results per CI category created by usage count estimator jobs that run automatically on a daily basis.

    1.  Navigate to the ITOM Licensable CIs \[itom\_lu\_licensable\_cis\] table by typing the table name in the navigation filter.

    2.  See the latest daily prediction results per each CI category by setting the filter conditions to **Created-on-today**.


## What to do next

Compare the predicted SU consumption data to the estimate you had before this forecast.

