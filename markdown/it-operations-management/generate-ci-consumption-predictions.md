---
title: Generate CI consumption predictions for 2026 Packaging SKU migration
description: Use the CI consumption prediction to compare your current ITOM subscription unit usage against the predicted usage under 2026 Packaging SKUs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/generate-ci-consumption-predictions.html
release: yokohama
product: IT Operations Management
classification: it-operations-management
topic_type: task
last_updated: "2026-05-10"
reading_time_minutes: 1
keywords: [CI consumption, prediction, 2026 Packaging, 2026 Packaging SKU migration]
breadcrumb: [Using ITOM/OT SU Licensing, ITOM/OT SU Licensing and subscriptions, IT Operations Management]
---

# Generate CI consumption predictions for 2026 Packaging SKU migration

Use the CI consumption prediction to compare your current ITOM subscription unit usage against the predicted usage under 2026 Packaging SKUs.

## Before you begin

Ensure that your organization has purchased ITOM subscriptions. You cannot view the information in the **ITOM License** module without subscriptions.

Ensure that you installed the latest available version of the ITOM/OT SU Licensing from ServiceNow Store.

Role required: admin

## About this task

Forecast your licensing needs before migrating to the new 2026 Packaging SKUs by estimating post-migration consumption, without requiring an active ITOM license. You can run the **Usage count estimator** job directly from the **Report ITOM Licensable CIs** view and predict SU consumption per category by applying SU ratios to the latest CI data in your environment. SU ratios represent the number of CIs in each category that correspond to one Subscription Unit, as set by your contract.

## Procedure

1.  Navigate to **All** &gt; **ITOM License** &gt; **Report ITOM Licensable CIs**.

    The **Report ITOM Licensable CIs** view appears.

2.  Filter the list by application for which you want to view licensed CIs and select **Run**.

    After the Usage count estimator job completes, results are added to the \[itom\_lu\_licensable\_cis\] table and are visible in the **Report ITOM Licensable CIs** view.

    \[Omitted image "ci\_consumption\_prediction\_list\_daily.png"\] Alt text: License prediction report for daily SU consumption per each CI category.

    **Note:** **CI New Category** equals **true** if this category is not covered by your current license. It will be introduced as a new licensable category under the 2026 Packaging SKU.

3.  Filter the list by **Contains estimate** to see only the prediction records and not production licensing records.

4.  Navigate to the \[itom\_lu\_licensable\_cis\] table by typing the table name in the navigation filter.

5.  Filter the table by **Created-on-today** to see the latest daily prediction results per each CI category.

    **Note:** Usage count estimator jobs also run automatically on a daily basis.


## What to do next

Compare the predicted SU consumption data to the estimate you had before this forecast.

