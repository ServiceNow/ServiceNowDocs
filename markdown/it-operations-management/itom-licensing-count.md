---
title: View CIs consuming ITOM subscription units
description: Generate a list of currently countable CIs for each of the ITOM applications: ITOM Visibility, Discovery, ITOM AIOps, Health Log Analytics, ITOM Cloud Accelerate, and ITOM Optimization.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using ITOM/OT SU Licensing, ITOM/OT SU Licensing and subscriptions, IT Operations Management]
---

# View CIs consuming ITOM subscription units

Generate a list of currently countable CIs for each of the ITOM applications: ITOM Visibility, Discovery, ITOM AIOps, Health Log Analytics, ITOM Cloud Accelerate, and ITOM Optimization.

## Before you begin

Ensure that your organization has purchased ITOM subscriptions. You cannot view the information in the **ITOM License** module without subscriptions.

Role required: sn\_itom\_license.reader

## About this task

The generated CI list is closely correlated to the latest daily CI count. At the same time, the number of CIs on the generated CI list may be slightly different from the latest daily CI count, if changes occurred since the last daily count.

## Procedure

1.  Navigate to **All** &gt; **ITOM License** &gt; **Report ITOM Licensable CIs**.

    The **Report ITOM Licensable CIs** page appears.

2.  Select the application for which you want to view licensed CIs:

    -   Discovery
    -   Optimization
    -   Visibility
    -   HLA
    -   Governance
    -   Health
3.  To create a report for the selected application, select **Populate licensable CIs**.

4.  To accept the confirmation message and generate the report, select **Yes**.

    The new report replaces the data in the previously generated report. You can cancel the report by selecting the application and then selecting **Cancel Job**.

5.  Wait for several minutes and then refresh the page.

    The **Status** of the application appears **Completed** when the report is complete.

6.  Select the application and then select **Show licensable CIs**.

    The ITOM Licensable CIs page displays the list of CIs with a license.


